---
name: Onboard a Safello customer with BankID
description: Authenticate an end customer via Swedish BankID, verify their email, capture terms acceptance, and complete the KYC questionnaire so they can trade.
api: openapi/safello-institutional-openapi.json
operations: [startAuth, obtainToken, getUser, sendVerificationEmail, verifyEmail, acceptTerms, requireKyc, kycQuestions, answerKyc]
---

# Onboard a Safello customer with BankID

Bring a new end customer to a trade-ready state on the Safello Institutional API.

## Prerequisites
- Institutional OAuth2 client credentials (client_id / client_secret).
- Base URL `https://api.safello.com` (staging: `https://api.s4f3.io`, add header `Test: true` to bypass real BankID).
- Every customer-scoped call must include the `source-ip-address` and `source-user-agent` headers identifying the end user.

## Steps
1. **Start BankID** — `startAuth` (`POST /oauth2/bankid`) with the customer's Swedish personal number. Returns `request_id`, `auto_start_token`, a polling interval, and a 120s expiry.
2. **Poll for the token** — `obtainToken` (`POST /oauth2/token`) with `grant_type=urn:safello:params:oauth:grant-type:bankid` and the `request_id`. Responses return `error: authorization_pending` until the customer completes BankID, then an access token (JWT, 5-min TTL) + refresh token. Request the scopes you need (`account.base`, `order`, `wallet`, ...).
3. **Read the user** — `getUser` (`GET /v2/account/user`) to inspect email-verification and onboarding status.
4. **Verify email if needed** — `sendVerificationEmail` (`POST /v2/account/email`), then `verifyEmail` (`PUT /v2/account/email`) with the emailed code.
5. **Accept terms** — `acceptTerms` (`PUT /v2/account/terms`) after the customer actively accepts the latest T&C.
6. **KYC** — `requireKyc` (`GET /v2/account/kyc`); if required, fetch `kycQuestions` (`GET /v2/account/kyc-questions`) and submit every outstanding answer with `answerKyc` (`POST /v2/account/kyc-questions`).

## Rules
- Access tokens expire after 5 minutes — refresh ~5s early via `grant_type=refresh_token`. Refresh tokens are single-use; reusing one invalidates the session.
- Answer ALL outstanding KYC questions in one submission.
- On `400`, read the Safello error code (see `errors/safello-error-codes.yml`), e.g. `ACCOUNT_EMAIL_INVALID_CODE`, `ACCOUNT_KYC_INVALID_ANSWERS`.
