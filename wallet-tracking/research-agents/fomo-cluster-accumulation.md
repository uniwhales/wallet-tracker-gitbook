---
description: (Whale)
---

# 👀 FOMO Cluster Accumulation

Three or more wallets from the FOMO app build net-positive positions in the same token inside a rolling window with 1000+ wallets labeled

### Filters

| Setting                     | Default    | Notes                                                                                                                    |
| --------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------ |
| Chain                       | All chains | Solana, Ethereum, Base                                                                                                   |
| Min FOMOs                   | 3          | Minimum distinct FOMO wallets with positive net in the window. Floor is 3.                                               |
| Timeframe                   | 1h         | Sliding window. Only buys and sells inside this period count toward the cluster. Options: 1m, 5m, 15m, 1h, 6h, 24h.      |
| Min net buy volume          | $1,000     | Sum of buys minus sells across the cluster. Alert fires only when this much has been accumulated. Set to 0 for no floor. |
| Max token age _(optional)_  | 1 day      | Skip tokens older than this. Units: minutes, hours, or days. Set to 0 for no ceiling.                                    |
| Min market cap _(optional)_ | $10,000    | Set to 0 for no floor.                                                                                                   |
| Max market cap _(optional)_ | no cap     | Leave empty for no ceiling.                                                                                              |

### Sample alert

```
👀 4 FOMOs bought #KLUD @ MC: $5.1k
Token: 3LKbVEWXHcHdfwDYz2FviYhRL9Km6vTghSQ4u12dpump
⏳ Age: 3m
💰 Net Buy: $1.2k
3LKbVEWX: $480, 9aXpHnRf: $260, Bn4Q92zP: $180, Fxq2K8ts: $160, Hzx9MTpa: $120

#solana | Chart
```

The alert lists each contributing wallet and what they put in, so you can size up who's behind the cluster at a glance.
