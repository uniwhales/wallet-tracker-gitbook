---
description: Whale Plan
---

# 🌱 Fresh Wallet Buy

A freshly funded wallet (regardless of funding source) starts accumulating a token. Wider than **CEX Fresh Buy** because it catches wallets funded by other wallets, bridges, or anything else, not just exchanges.

Fires the moment a fresh wallet's cumulative purchases of a single token cross your USD threshold.

### Filters

| Setting            | Default    | Notes                                                     |
| ------------------ | ---------- | --------------------------------------------------------- |
| Chain              | All chains | Solana, Ethereum, Base                                    |
| Min cumulative buy | $1,000     | Floor is $500.                                            |
| Max funded age     | 14 days    | Skip wallets first funded longer than this. 1 to 14 days. |

### Sample alert

```
🌱 Fresh wallet 3yZj3QeL bought $6.1k #WIF
Funded by 5tzFkiKs with 6.94 SOL ($1.4k) 4d ago
Token: EKpQGSJtjMFqKZ9KQanSqYXRcF8fBopzLHYxdM65zcjm
🏛 MC: $1.2k
⏳ Age: 2h

#solana | ViewTx | Chart | Wallet
```

