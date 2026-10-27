# Credits and plans

### Plans

|           | Free                  | Builder             | Architect           |
| --------- | --------------------- | ------------------- | ------------------- |
| Price     | Free                  | 89 USD / month\*    | 188 USD / month\*   |
| Credits   | 5,000                 | 100,000             | 250,000             |
| Rate      | 10 credits / second   | 25 credits / second | 75 credits / second |
| Endpoints | `/feed` and `/chains` | All endpoints       | All endpoints       |
| WebSocket | —                     | ✅                   | ✅                   |
| Support   | Community             | Community           | Priority            |

\*10% off with annual billing.

Sign in to the [plans page](https://build.cielo.finance/my-dashboard/plans) to subscribe. For an enterprise plan, [contact us](https://docs.google.com/forms/d/1L4u5ssMdjpaLQYVOr3E5FkB6lHGwST3eOjPxs9NS8Lw/).

### How credits work

Each call spends credits from your plan's balance. The cost depends on the endpoint and, for the feed, on the query.

* Only successful (`200`) responses spend credits. Errors are free.
* When the balance runs out, calls return `429` until the quota resets or you upgrade.
* The WebSocket spends 1 credit per 10 delivered transactions.

### Endpoint costs

Paths are relative to `https://api.cielo.finance`.

#### Free and paid plans

| Endpoint             | Credits                                                   |
| -------------------- | --------------------------------------------------------- |
| `GET /api/v1/feed`   | 5 — see [feed pricing](credits-and-plans.md#feed-pricing) |
| `GET /api/v1/chains` | 0                                                         |

#### Paid plans

| Endpoint                                                                                         | Credits |
| ------------------------------------------------------------------------------------------------ | ------- |
| **Wallet PnL & stats**                                                                           |         |
| `GET /api/v1/{wallet}/pnl/tokens`                                                                | 5       |
| `GET /api/v1/{wallet}/pnl/nfts`                                                                  | 5       |
| `GET /api/v1/{wallet}/pnl/total-stats`                                                           | 20      |
| `GET /api/v1/{wallet}/pnl/tokens-chart`                                                          | 15      |
| `GET /api/v1/{wallet}/pnl/month`                                                                 | 5       |
| `GET /api/v1/{wallet}/trading-stats`                                                             | 30      |
| `GET /api/v1/{wallet}/enhanced-stats/aggregated`                                                 | 20      |
| `GET /api/v1/{wallet}/enhanced-stats/profitability-performance`                                  | 20      |
| `GET /api/v2/enhanced-stats/aggregated`                                                          | 25      |
| `GET /api/v1/{wallet}/portfolio`                                                                 | 20      |
| `GET /api/v1/{wallet}/token-balance`                                                             | 3       |
| `GET /api/v1/wallet/positions`                                                                   | 3       |
| `GET /api/v1/{wallet}/related-wallets`                                                           | 10      |
| `GET /api/v2/token-flows`                                                                        | 5       |
| `GET /api/v2/new-token-flows`                                                                    | 5       |
| **Tags**                                                                                         |         |
| `GET /api/v1/{wallet}/tags` (deprecated)                                                         | 5       |
| `GET /api/v1/tags`                                                                               | 5       |
| `GET /api/v1/tags/wallets`                                                                       | 10      |
| **Token**                                                                                        |         |
| `GET /api/v1/token/metadata`                                                                     | 2       |
| `GET /api/v1/token/price`                                                                        | 2       |
| `GET /api/v1/token/stats`                                                                        | 10      |
| `GET /api/v1/token/stats-liquidity`                                                              | 10      |
| `GET /api/v1/token/checklist`                                                                    | 10      |
| `GET /api/v1/trending-tokens`                                                                    | 20      |
| **Wallet tracking**                                                                              |         |
| `GET /api/v1/tracked-wallets`                                                                    | 5       |
| `POST /api/v1/tracked-wallets`                                                                   | 5       |
| `DELETE /api/v1/tracked-wallets`                                                                 | 5       |
| `PUT /api/v1/tracked-wallets/{wallet_id}`                                                        | 5       |
| `PUT /api/v2/tracked-wallets/{wallet}`                                                           | 5       |
| `GET /api/v1/tracked-wallets/address/{wallet}`                                                   | 5       |
| `GET /api/v1/tracked-wallets/telegram-bots`                                                      | 5       |
| `GET /api/v1/lists/all`                                                                          | 5       |
| `GET /api/v1/lists`                                                                              | 5       |
| `POST /api/v1/lists`                                                                             | 5       |
| `PUT /api/v1/lists/{list_id}`                                                                    | 5       |
| `DELETE /api/v1/lists/{list_id}`                                                                 | 5       |
| `PUT /api/v1/lists/{list_id}/toggle-follow`                                                      | 5       |
| **Trading** (trading via API must be enabled at [app.cielo.finance](https://app.cielo.finance/)) |         |
| `GET /api/trading/wallets`                                                                       | 5       |
| `GET /api/trading/wallets/default`                                                               | 5       |
| `PUT /api/trading/wallets/{wallet_id}/default`                                                   | 2       |
| `PUT /api/trading/wallets/{wallet_id}/name`                                                      | 2       |
| `GET /api/trading/solana/v2/quote`                                                               | 5       |
| `GET /api/trading/base/v2/quote`                                                                 | 5       |
| `POST /api/trading/base/v2/swap`                                                                 | 1       |
| `POST /api/trading/wallets`                                                                      | 10      |

#### Feed pricing

`GET /api/v1/feed` costs 5 credits. A narrow query costs 3: one that filters by `chains` or `txTypes` and has exactly one wallet, one chain or one transaction type. `includeMarketCap=true` doubles the price.

| Query                                              | Credits |
| -------------------------------------------------- | ------- |
| `/api/v1/feed`                                     | 5       |
| `/api/v1/feed?chains=solana`                       | 3       |
| `/api/v1/feed?txTypes=swap&chains=solana,base`     | 3       |
| `/api/v1/feed?wallet=…&txTypes=swap`               | 3       |
| `/api/v1/feed?chains=solana&includeMarketCap=true` | 6       |
| `/api/v1/feed?includeMarketCap=true`               | 10      |
