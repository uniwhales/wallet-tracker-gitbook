---
description: (Whale)
---

# ⭐ Dynamic Holders Tracking

Watch any token's top holders in real time. The agent pings on their buys, sells, sends, and receives.

What makes it dynamic: the agent follows the supply. When a tracked holder sends tokens to a new wallet, that wallet automatically joins the tracked set. They can move the bag around, but you'll still see where it lands.

### Filters

| Setting        | Default  | Notes                                                                                                        |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------ |
| Chain          | Solana   | Pick one chain: Solana, Ethereum, or Base. The agent is per-chain and per-token.                             |
| Token          | required | Paste the token's address on the chain you picked. EVM addresses are lowercased; Solana base58 is preserved. |
| Top wallets    | 20       | The rank window. Alerts fire only when a wallet's rank is ≤ this number. Range 10 to 100.                    |
| Min trade USD  | $50      | Floor for 🟢 Bought and 🔴 Sold events.                                                                      |
| Min sent %     | 10%      | Floor for 🚀 Sent events. Percent of the sender's pre-send holdings moved. Range 1 to 100%.                  |
| Min received % | 10%      | Floor for 🛬 Received events. Percent of the receiver's resulting holdings. Range 1 to 100%.                 |
