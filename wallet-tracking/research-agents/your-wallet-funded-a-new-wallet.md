---
description: Pro+Whale Plans
---

# 🔍 Your Wallet Funded a New Wallet

A wallet you track sends native SOL or ETH to a brand-new address with no prior on-chain history. Catches the moment a wallet you care about spins up a new one, which often means a separate trading account or a setup for something specific.

### Filters

| Setting                 | Default    | Notes                                                             |
| ----------------------- | ---------- | ----------------------------------------------------------------- |
| Chain                   | All chains | Solana, Ethereum, Base, Robinhood, Arc                            |
| Min funding · Solana    | (empty)    | Skip funding below this size in SOL. Leave empty for any amount.  |
| Min funding · Ethereum  | (empty)    | Skip funding below this size in ETH. Leave empty for any amount.  |
| Min funding · Base      | (empty)    | Skip funding below this size in ETH. Leave empty for any amount.  |
| Min funding · Robinhood | (empty)    | Skip funding below this size in ETH. Leave empty for any amount.  |
| Min funding · Arc       | (empty)    | Skip funding below this size in USDC. Leave empty for any amount. |

Amounts are in each chain's native unit (SOL on Solana, ETH on Ethereum, Base and Robinhood, USDC on Arc).

### Sample alert

```
🔍 New wallet funded by 0x77134c
0x94db6bcf0a4a6FB166EFFC75f69CeeA8a4D91CBD (Profile)
Amount: 0.0001 ETH ($0.17)

#ethereum | ViewTx
```
