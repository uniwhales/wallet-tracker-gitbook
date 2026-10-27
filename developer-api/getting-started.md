# Getting started

The Cielo API gives programmatic access to the on-chain data behind [Cielo Finance](https://app.cielo.finance/): a real-time feed of wallet transactions, wallet PnL and trading stats, token data and safety checks, wallet tags, portfolio tracking and on-chain trading, across EVM chains, Solana and more.

### Base URL

```
https://api.cielo.finance
```

Every endpoint lives under `/api/v1/...` or `/api/v2/...`. The real-time stream is at `wss://api.cielo.finance/api/v1/ws`.

{% hint style="warning" %}
`feed-api.cielo.finance` is deprecated. It serves the same API for now, but responses carry a `Deprecation` header and it will be switched off. Move to `api.cielo.finance` — nothing else changes.
{% endhint %}

### Your first request

1. [Get an API key](authentication.md) in the [Cielo API portal](https://build.cielo.finance/).
2. Send it in the `X-API-KEY` header:

```bash
curl -s "https://api.cielo.finance/api/v1/feed?limit=5" \
  -H "X-API-KEY: YOUR_API_KEY" \
  -H "accept: application/json"
```

Every response is a JSON envelope:

```json
{
  "status": "ok",
  "data": { "...": "..." }
}
```

On failure `status` is `"error"` and `message` says why — see [Errors](errors.md).

### Next steps

* [Credits & plans](credits-and-plans.md) — what each call costs and what your plan includes.
* [Fetch the transaction feed](fetch-the-feed.md) — filters, pagination and examples.
* [Stream transactions over WebSocket](stream-over-websocket.md).
* The **API Reference** section documents every endpoint, parameter and response field.
* [`llms.txt`](https://api.cielo.finance/llms.txt) and [`llms-full.txt`](https://api.cielo.finance/llms-full.txt) give the same reference in plain text for LLMs and agents; the raw OpenAPI spec is at [`/swagger/openapi.json`](https://api.cielo.finance/swagger/openapi.json).
