---
description: Free Plan
---

# 💫 KOL Cluster Buy

Three or more verified KOLs (curated X/Twitter influencers) buy the same token inside a configurable time window. Catches the moment a cluster of known accounts agree on something before it shows up in price.

### Filters

| Setting                       | Default    | Notes                                                                            |
| ----------------------------- | ---------- | -------------------------------------------------------------------------------- |
| Chain                         | All chains | Solana, Ethereum, Base                                                           |
| Min KOLs                      | 3          | Minimum number of unique KOL wallets buying the same token in the window.        |
| Timeframe                     | 1h         | How long all the KOL buys must happen within. Options: 1m, 5m, 15m, 1h, 6h, 24h. |
| Min market cap _(optional)_   | 0          | 0 means no floor.                                                                |
| Max market cap _(optional)_   | 0          | 0 means no ceiling.                                                              |
| Min combined USD _(optional)_ | $100       | Sum of buy amounts across the matching KOLs.                                     |
| Max token age _(optional)_    | 3 days     | Skip tokens older than this. Units: minutes, hours, or days.                     |

### Sample alert

```
💫 3 KOLs bought #Anon @ MC: $3.2M
Token: 9McvH6w97oewLmPxqQEoHUAv3u5iYMyQ9AeZZhguYf1T
⏳ Age: 507d
💼 Volume: $1.5k
🔍 KOLs: saale, Loopierr, CoCo

#solana | Chart
```
