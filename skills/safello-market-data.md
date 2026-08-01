---
name: Read Safello market data
description: Discover tradable symbols and pairs, then pull live prices, tickers, and historical candlesticks using only client-credentials auth.
api: openapi/safello-institutional-openapi.json
operations: [listCryptoSymbols, listFiatSymbols, listTradingPairs, getPrices, getTradePairTicker, getMarketCandlestickData]
---

# Read Safello market data

Fetch public market data. This flow needs no customer — only an app token.

## Prerequisites
- An access token from `grant_type=client_credentials` (only the `market` scope is granted to this flow).

## Steps
1. **List symbols** — `listCryptoSymbols` (`GET /v2/market/symbols/crypto`) and `listFiatSymbols` (`GET /v2/market/symbols/fiat`).
2. **List pairs** — `listTradingPairs` (`GET /v2/market/symbols/pairs`).
3. **Live prices** — `getPrices` (`GET /v2/market/prices/rates`) or a single ticker with `getTradePairTicker` (`GET /v2/market/ticker/{pair}`).
4. **History** — `getMarketCandlestickData` (`GET /v2/market/ohlcv`) for OHLCV candles.

## Rules
- The client-credentials flow is scoped to `market` only; customer/account/order/wallet endpoints require the BankID or authorization-code flows.
- Access tokens expire after 5 minutes.
