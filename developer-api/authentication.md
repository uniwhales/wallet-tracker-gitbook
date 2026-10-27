# Authentication

### Get an API key

1. Sign in to the [Cielo API portal](https://build.cielo.finance/my-dashboard/general) and pick a [plan](https://build.cielo.finance/my-dashboard/plans).
2. On the **General** settings page, scroll to **API Key Manager** and click **Generate New Key**.

### Send the key

Pass the key in the `X-API-KEY` header on every request:

```bash
curl -s "https://api.cielo.finance/api/v1/chains" \
  -H "X-API-KEY: YOUR_API_KEY"
```

```javascript
const res = await fetch("https://api.cielo.finance/api/v1/feed?limit=10", {
  headers: { "X-API-KEY": process.env.CIELO_API_KEY },
});
const { status, data, message } = await res.json();
```

```python
import os, requests

res = requests.get(
    "https://api.cielo.finance/api/v1/feed",
    params={"limit": 10},
    headers={"X-API-KEY": os.environ["CIELO_API_KEY"]},
)
body = res.json()
```

The WebSocket takes the same header on the upgrade request — see [WebSocket](stream-over-websocket.md).

{% hint style="danger" %}
Keep the key server-side. Anyone with the key spends your credits.
{% endhint %}

### Key errors

| HTTP | `message`                                                       | Meaning                                                                      |
| ---- | --------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| 403  | API Key is required to access to API                            | No `X-API-KEY` header.                                                       |
| 403  | Your API key is not valid…                                      | The key is unknown or was deactivated.                                       |
| 402  | Your subscription has expired…                                  | Renew the plan to reactivate the key.                                        |
| 429  | You have reached your maximum API credit limit…                 | The plan's credits are spent until the quota resets.                         |
| 403  | Your current plan does not include access to this API endpoint… | Upgrade to call this endpoint — see [Credits & plans](credits-and-plans.md). |

The full list is in [Errors](errors.md).
