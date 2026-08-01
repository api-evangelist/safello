---
name: Place a Safello sell order
description: Check sell compliance, quote fees, create a sell order, and poll it to completion, paying out to the customer's bank account.
api: openapi/safello-institutional-openapi.json
operations: [verifySellOrderCompliance, getFees, getBankAccounts, createSellOrder, checkOrderStatus]
---

# Place a Safello sell order

Sell cryptocurrency for fiat and pay out to the customer's registered bank account.

## Prerequisites
- A customer access token with `order` and `account.bank-account:read` scopes.
- `source-ip-address` and `source-user-agent` headers on every call.

## Steps
1. **Verify compliance** — `verifySellOrderCompliance` (`POST /v2/compliance/verify/orders/sell`).
2. **Confirm payout account** — `getBankAccounts` (`GET /v2/account/bank-account`) to ensure a payout destination exists.
3. **Quote fees** — `getFees` (`GET /v2/orders/fees`).
4. **Create the order** — `createSellOrder` (`POST /v2/orders/sell`) with the crypto amount to sell (`SellOrderInput`).
5. **Track status** — `checkOrderStatus` (`GET /v2/orders/{orderId}`) until terminal.

## Rules
- If no bank account is present, register one with `addBankAccount` (`PUT /v2/account/bank-account`) — requires the `account.bank-account` (write) scope.
- No idempotency support — reconcile with `checkOrderStatus` rather than resubmitting.
