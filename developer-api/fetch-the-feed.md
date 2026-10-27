# Fetch the feed

`GET /api/v1/feed` returns a feed of decoded on-chain transactions — swaps, transfers, LP, lending, NFT trades and more — across EVM chains, Solana and other supported networks. Without filters it returns the transactions of the wallets you track in [Cielo](https://app.cielo.finance/); with `wallet` or `list` it returns those wallets instead.

### Parameters

All parameters are optional query parameters. List values are comma-separated.

| Parameter                       | Type        | Description                                                                                                 |
| ------------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------- |
| `wallet`                        | string      | Only these wallets, e.g. `wallet=C6y7…qBB,0x240d…82ef`.                                                     |
| `list`                          | integer     | Only the wallets of this list. List IDs come from `GET /api/v1/lists`.                                      |
| `chains`                        | string list | Only these chains, e.g. `chains=solana,base`. The valid values come from [`GET /api/v1/chains`](chains.md). |
| `txTypes`                       | string list | Only these transaction types, e.g. `txTypes=swap,transfer`. See [Transaction types](transaction-types.md).  |
| `tokens`                        | string list | Only transactions with these tokens, by address or symbol, e.g. `tokens=LINK,5F5x…enUB`.                    |
| `minUSD` / `maxUSD`             | number      | USD value range of the transaction.                                                                         |
| `newTrades`                     | boolean     | Only a wallet's first trade of a token.                                                                     |
| `fromTimestamp` / `toTimestamp` | integer     | UNIX time range, in seconds.                                                                                |
| `limit`                         | integer     | Page size, up to 100.                                                                                       |
| `startFrom`                     | string      | Cursor for the next page — see [Pagination](fetch-the-feed.md#pagination).                                  |
| `includeMarketCap`              | boolean     | Add token market caps. Doubles the credit cost.                                                             |

A call costs 3–10 credits depending on the filters — see [feed pricing](credits-and-plans.md#feed-pricing).

### Examples

#### Latest transactions of your tracked wallets

```bash
curl -s "https://api.cielo.finance/api/v1/feed?limit=20" \
  -H "X-API-KEY: YOUR_API_KEY"
```

#### One wallet on one chain

```bash
curl -s "https://api.cielo.finance/api/v1/feed?wallet=0x240df0da944c11428eb9f8ad197cc211fd8d82ef&chains=ethereum" \
  -H "X-API-KEY: YOUR_API_KEY"
```

#### Swaps of a token

```javascript
const token = "9Ttyez3xiruyj6cqaR495hbBkJU6SUWdV6AmQ9MvbyyS";
const res = await fetch(
  `https://api.cielo.finance/api/v1/feed?txTypes=swap&tokens=${token}`,
  { headers: { "X-API-KEY": process.env.CIELO_API_KEY } },
);
const { data } = await res.json();
```

```json
{
  "status": "ok",
  "data": {
    "items": [
      {
        "wallet": "6sdb5o3XWM27RSjcYqoVZ88ruuPzHTfqFQEq26nN6eVq",
        "wallet_label": "whale3",
        "tx_hash": "4r3R5k4XNLhct3o2jLaYwjKRcohmV6jHSd3FipJ4cDDvFB5BwrXq4pVxKGktUNMTmiTFzSu79U2cpp1CjVruFufG",
        "tx_type": "swap",
        "chain": "solana",
        "timestamp": 1711005068,
        "block": 255499560,
        "token0_address": "9Ttyez3xiruyj6cqaR495hbBkJU6SUWdV6AmQ9MvbyyS",
        "token0_amount": 111237179.719028,
        "token0_amount_usd": 52561.70051676631,
        "token0_symbol": "smole",
        "token1_address": "native",
        "token1_amount": 276.577156721,
        "token1_amount_usd": 52561.70051676631,
        "token1_symbol": "SOL",
        "first_interaction": false
      }
    ],
    "paging": {
      "total_rows_in_page": 1,
      "has_next_page": true,
      "next_object_id": "NjVmYzAzOWQ4MDlkZDE4ZDMwZDM2NjljXzE3MTEwMTQ3NjE"
    }
  }
}
```

The fields of each item depend on `tx_type`; the API Reference lists them for every type.

### Pagination

The feed is newest first. When `paging.has_next_page` is `true`, pass `paging.next_object_id` as `startFrom` to get the next page:

```javascript
let cursor;
do {
  const url = new URL("https://api.cielo.finance/api/v1/feed");
  url.searchParams.set("wallet", wallet);
  url.searchParams.set("limit", "100");
  if (cursor) url.searchParams.set("startFrom", cursor);

  const { data } = await (await fetch(url, { headers })).json();
  handle(data.items);
  cursor = data.paging.has_next_page ? data.paging.next_object_id : undefined;
} while (cursor);
```

Each page is a separate call and spends credits.

{% hint style="info" %}
For new transactions as they happen, use the [WebSocket](stream-over-websocket.md) instead of polling the feed.
{% endhint %}
