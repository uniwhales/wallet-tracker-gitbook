# Chains

### Supported chains

The live list of supported chains comes from `GET /api/v1/chains` (free, 0 credits). Its values are the ones the `chains` parameter accepts on the feed and other endpoints, and in WebSocket filters — anything else is rejected with `400`.

```bash
curl -s "https://api.cielo.finance/api/v1/chains" -H "X-API-KEY: YOUR_API_KEY"
```

Cielo covers EVM chains (Ethereum, Base, BNB Chain, Arbitrum, Optimism, Polygon, HyperEVM, Robinhood and more) and non-EVM chains (Solana, Hyperliquid, Sui, Tron, Bitcoin). Prefer the endpoint over a hard-coded list: new chains appear there first.

### Chain IDs

The wallet tracking endpoints (`/api/v1/tracked-wallets`, `/api/v2/tracked-wallets`) take numeric chain IDs in alert filters:

| Chain       | ID |
| ----------- | -- |
| Ethereum    | 1  |
| BNB         | 2  |
| Polygon     | 3  |
| Arbitrum    | 5  |
| Avalanche   | 6  |
| Aurora      | 9  |
| Optimism    | 10 |
| Gnosis      | 13 |
| zkSync      | 15 |
| PulseChain  | 16 |
| Mantle      | 18 |
| Base        | 19 |
| Scroll      | 21 |
| Linea       | 22 |
| Blast       | 23 |
| Solana      | 24 |
| Bitcoin     | 28 |
| Tron        | 29 |
| Sui         | 30 |
| Sonic       | 31 |
| Abstract    | 32 |
| Berachain   | 33 |
| Unichain    | 34 |
| Story       | 35 |
| HyperEVM    | 36 |
| Hyperliquid | 37 |
| Ink         | 38 |
| Monad       | 40 |
| MegaETH     | 41 |
| Tempo       | 42 |
| Robinhood   | 43 |
