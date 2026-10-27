# Stream over WebSocket

The WebSocket pushes the same transactions as the [feed](fetch-the-feed.md) the moment Cielo indexes them. It is available on paid plans and spends 1 credit per 10 delivered transactions.

### Connect

```
wss://api.cielo.finance/api/v1/ws
```

Send your API key in the `X-API-KEY` header of the upgrade request. After connecting, send JSON commands; the server answers each command with an acknowledgement event and then streams `tx` events.

```javascript
import WebSocket from "ws";

const ws = new WebSocket("wss://api.cielo.finance/api/v1/ws", {
  headers: { "X-API-KEY": process.env.CIELO_API_KEY },
});

ws.on("open", () => {
  ws.send(JSON.stringify({
    type: "subscribe_feed",
    filter: { tx_types: ["swap"], chains: ["solana", "base"], min_usd_value: 1000 },
  }));
});

ws.on("message", (raw) => {
  const event = JSON.parse(raw);
  if (event.type === "tx") console.log(event.data);
  else console.log(event.type, event.data);
});
```

### Commands

#### `subscribe_feed`

Stream the transactions of your tracked wallets, or of one list with `list_id`. `filter` is optional.

```json
{
  "type": "subscribe_feed",
  "list_id": 1234,
  "filter": {
    "tx_types": ["transfer", "swap"],
    "chains": ["ethereum", "solana"],
    "tokens": ["0x514910771af9ca656af840dff83e8264ecf986ca"],
    "min_usd_value": 1000,
    "new_trade": true
  }
}
```

| Filter field    | Description                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `tx_types`      | Only these [transaction types](transaction-types.md). `transfer_in` and `transfer_out` narrow transfers to one direction. |
| `chains`        | Only these [chains](chains.md).                                                                                           |
| `tokens`        | Only transactions with these token addresses.                                                                             |
| `min_usd_value` | Minimum USD value.                                                                                                        |
| `new_trade`     | Only a wallet's first trade of a token.                                                                                   |

#### `subscribe_wallet`

Stream one wallet, tracked or not. Send the command again for each wallet. Takes the same optional `filter`.

```json
{ "type": "subscribe_wallet", "wallet": "0x240df0da944c11428eb9f8ad197cc211fd8d82ef" }
```

#### Unsubscribe and keep-alive

```json
{ "type": "unsubscribe_feed" }
{ "type": "unsubscribe_wallet", "wallet": "0x240df0da944c11428eb9f8ad197cc211fd8d82ef" }
{ "type": "ping" }
```

### Events

Every message from the server is `{"type": …, "data": …}`.

| `type`                                      | `data`                                             |
| ------------------------------------------- | -------------------------------------------------- |
| `feed_subscribed` / `feed_unsubscribed`     | The accepted subscription.                         |
| `wallet_subscribed` / `wallet_unsubscribed` | The wallet and its filter.                         |
| `tx`                                        | One transaction, in the same shape as a feed item. |
| `pong`                                      | Reply to `ping`.                                   |
| `error`                                     | The error text, e.g. for an invalid command.       |

The server checks the key every 30 seconds and closes the connection once it runs out of credits or stops being valid. Reconnect with backoff and send your subscriptions again.
