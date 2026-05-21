---
description: (Pro+Whale)
---

# 👥 Top Holders Supply Change

The top-20 holders' combined share of a token's supply shifts by your chosen percentage in a rolling window. Direction-symmetric, so it fires on both accumulation (group adding) and distribution (group dumping). Catches quiet supply moves that don't show up as a single big trade.

### Filters

| Setting                     | Default    | Notes                                                                                   |
| --------------------------- | ---------- | --------------------------------------------------------------------------------------- |
| Chain                       | All chains | Solana, Ethereum, Base                                                                  |
| Min supply change           | 5%         | Absolute delta that fires the alert. \`                                                 |
| Min market cap              | $300,000   | Hard floor is $100,000.                                                                 |
| Max market cap _(optional)_ | $5,000,000 | Leave empty for no ceiling.                                                             |
| Min token age _(optional)_  | 3 hours    | Skip tokens younger than this. Units: minutes, hours, or days. Leave at 0 for no floor. |
| Max token age _(optional)_  | 14 days    | Skip tokens older than this. Units: minutes, hours, or days. Leave at 0 for no ceiling. |

### Sample alert

```
👥 Top-20 holders distributed #WIF
Holdings: 11.0% → 8.5% (-2.5%) in 1h

Token: EKpQGSJtjMFqKZ9KQanSqYXRcF8fBopzLHYxdM65zcjm
🏛 MC: $457.0k
⏳ Age: 1h

#solana | Chart
```

The verb in the headline flips between "accumulated" and "distributed" depending on which way the share moved.
