---
name: Place a Safello buy order
description: Check buy compliance, quote fees, create a buy order, and poll it to completion for an onboarded customer.
api: openapi/safello-institutional-openapi.json
operations: [verifyBuyOrderCompliance, getFees, createBuyOrder, checkOrderStatus]
---

# Place a Safello buy order

Buy cryptocurrency with fiat on behalf of an onboarded, KYC-complete customer.

## Prerequisites
- A customer access token with the `order` scope (see the onboarding skill).
- `source-ip-address` and `source-user-agent` headers on every call.

## Steps
1. **Verify compliance** — `verifyBuyOrderCompliance` (`POST /v2/compliance/verify/orders/buy`) to confirm the customer may buy the intended amount/asset before charging.
2. **Quote fees** — `getFees` (`GET /v2/orders/fees`) to show the customer the fee for the trade.
3. **Create the order** — `createBuyOrder` (`POST /v2/orders/buy`) with the fiat amount and target crypto (`BuyOrderInput`).
4. **Track status** — `checkOrderStatus` (`GET /v2/orders/{orderId}`) until it reaches a terminal `EOrderStatus`.

## Rules
- Always verify compliance first; a `ORDER_CUSTOMER_FROZEN` or `ORDER_SAFE_ENVIRONMENT` error means the customer cannot trade right now.
- No idempotency key is supported — do not blindly retry `createBuyOrder`; re-read order state with `checkOrderStatus` before retrying.
- `ORDER_PAYMENT_ERROR` indicates a payment-leg failure; surface it to the customer.
