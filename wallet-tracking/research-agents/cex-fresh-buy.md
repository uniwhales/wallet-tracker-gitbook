---
description: Whale Plan
---

# 💳 CEX Fresh Buy

A brand-new CEX-funded wallet makes its first buy of size on a token. Someone pulled money off an exchange, set up a wallet, and immediately bought, which usually means real new demand rather than recycled supply.

Fires when a wallet funded from a centralized exchange in the last 7 days commits at least $1,000 USD to a single token. The buy is locked in as the wallet's first on-chain trade.

### Filters

| Setting        | Default    | Notes                                                     |
| -------------- | ---------- | --------------------------------------------------------- |
| Chain          | All chains | Solana, Ethereum, Base                                    |
| Min amount USD | $1,000     | Floor is $1,000. Raise it if you want only larger buys.   |
| Max funded age | 7 days     | Skip wallets first funded longer than this. 1 to 14 days. |

### Sample alert

```
💳 CEX-funded wallet 0×123456 bought $1.9k #PEPE
Funded by Binance (2h ago)
Token: 0×6982...
🏛 MC: $450.0k
⏳ Age: 2038d
💼 Volume: $15.6k

#ethereum | ViewTx | Chart | Wallet
```
