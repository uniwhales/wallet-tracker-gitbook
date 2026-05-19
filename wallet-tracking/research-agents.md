# Research Agents

The [Research Agents](https://trading.cielo.finance/agents/research) page lets you spin up a watcher that pings you the moment a specific onchain pattern fires. Pick a trigger, tune the filters, point it at a Telegram bot or Discord channel, and the agent does the watching so you can focus on the trade.

Each agent does one job: it watches the chain for a specific signal and posts an alert when it fires. No copy trading, no execution. You decide what to do with the alert.

\{% hint style="info" %\} Research Agents work alongside your existing Cielo alerts. You can route each agent to a different Telegram bot or Discord channel so the signals stay sorted. \{% endhint %\}

### Creating an agent

From the Research Agents page, click **Make an agent** (or **Make my first agent** if you don't have any yet). The wizard walks you through five steps:

1. **Trigger** - Pick which onchain pattern should fire this agent.
2. **Filters** - Tune the trigger. Each trigger has its own filter set (covered below).
3. **Output** - Pick a Telegram bot, a Discord channel, or both. You need at least one to continue.
4. **Name** - Give the agent a short label so you recognise it at a glance.
5. **Preview** - Review the configuration and see a sample alert. Click **Activate agent** to go live.

Once active, the agent runs immediately and starts posting to your chosen channels.

### Popular starting points

The Research Agents landing page surfaces three quick-start cards at the bottom: **Your Wallet Funded a New Wallet**, **CEX Fresh Buy**, and **KOL Cluster Buy**. Clicking any of them opens the wizard pre-loaded with that trigger.

### Triggers

Triggers are grouped by what they watch.

#### Wallet activity

These fire on something a single wallet does.

**💳 CEX Fresh Buy&#x20;**_**(Whale)**_

A brand-new CEX-funded wallet makes its first buy of size on a token. Someone pulled money off an exchange, set up a wallet, and immediately bought, which usually means real new demand rather than recycled supply.

Fires when a wallet funded from a centralized exchange in the last 7 days commits at least $1,000 USD to a single token. The buy is locked in as the wallet's first on-chain trade.

**Filters**

| Setting        | Default    | Notes                                                     |
| -------------- | ---------- | --------------------------------------------------------- |
| Chain          | All chains | Solana, Ethereum, Base                                    |
| Min amount USD | $1,000     | Floor is $1,000. Raise it if you want only larger buys.   |
| Max funded age | 7 days     | Skip wallets first funded longer than this. 1 to 14 days. |

**Sample alert**

```
💳 CEX-funded wallet 0×123456 bought $1.9k #PEPE
Funded by Binance (2h ago)
Token: 0×6982...
🏛 MC: $450.0k
⏳ Age: 2038d
💼 Volume: $15.6k

#ethereum | ViewTx | Chart | Wallet
```

**🌱 Fresh Wallet Buy&#x20;**_**(Whale)**_

A freshly funded wallet (regardless of funding source) starts accumulating a token. Wider than CEX Fresh Buy because it catches wallets funded by other wallets, bridges, or anything else, not just exchanges.

Fires the moment a fresh wallet's cumulative purchases of a single token cross your USD threshold.

**Filters**

| Setting            | Default    | Notes                                                     |
| ------------------ | ---------- | --------------------------------------------------------- |
| Chain              | All chains | Solana, Ethereum, Base                                    |
| Min cumulative buy | $1,000     | Floor is $500.                                            |
| Max funded age     | 14 days    | Skip wallets first funded longer than this. 1 to 14 days. |

**Sample alert**

```
🌱 Fresh wallet 3yZj3QeL bought $6.1k #WIF
Funded by 5tzFkiKs with 6.94 SOL ($1.4k) 4d ago
Token: EKpQGSJtjMFqKZ9KQanSqYXRcF8fBopzLHYxdM65zcjm
🏛 MC: $1.2k
⏳ Age: 2h

#solana | ViewTx | Chart | Wallet
```

**🔍 Your Wallet Funded a New Wallet&#x20;**_**(Pro+Whale)**_

A wallet you track sends native SOL or ETH to a brand-new address with no prior on-chain history. Catches the moment a wallet you care about spins up a new one, which often means a separate trading account or a setup for something specific.

**Filters**

| Setting                | Default    | Notes                                                            |
| ---------------------- | ---------- | ---------------------------------------------------------------- |
| Chain                  | All chains | Solana, Ethereum, Base                                           |
| Min funding · Solana   | (empty)    | Skip funding below this size in SOL. Leave empty for any amount. |
| Min funding · Ethereum | (empty)    | Skip funding below this size in ETH. Leave empty for any amount. |
| Min funding · Base     | (empty)    | Skip funding below this size in ETH. Leave empty for any amount. |

Amounts are in each chain's native unit (SOL on Solana, ETH on Ethereum and Base).

**Sample alert**

```
🔍 New wallet funded by 0×77134c
0×94db6bcf0a4a6FB166EFFC75f69CeeA8a4D91CBD (Profile)
Amount: 0.0001 ETH ($0.17)

#ethereum | ViewTx
```

#### Aggregate signal

This group fires when several wallets line up on the same token.

**💫 KOL Cluster Buy&#x20;**_**(Free)**_

Three or more verified KOLs (curated X/Twitter influencers) buy the same token inside a configurable time window. Catches the moment a cluster of known accounts agree on something before it shows up in price.

**Filters**

| Setting                       | Default    | Notes                                                                            |
| ----------------------------- | ---------- | -------------------------------------------------------------------------------- |
| Chain                         | All chains | Solana, Ethereum, Base                                                           |
| Min KOLs                      | 3          | Minimum number of unique KOL wallets buying the same token in the window.        |
| Timeframe                     | 1h         | How long all the KOL buys must happen within. Options: 1m, 5m, 15m, 1h, 6h, 24h. |
| Min market cap _(optional)_   | 0          | 0 means no floor.                                                                |
| Max market cap _(optional)_   | 0          | 0 means no ceiling.                                                              |
| Min combined USD _(optional)_ | $100       | Sum of buy amounts across the matching KOLs.                                     |
| Max token age _(optional)_    | 3 days     | Skip tokens older than this. Units: minutes, hours, or days.                     |

**Sample alert**

```
💫 3 KOLs bought #Anon @ MC: $3.2M
Token: 9McvH6w97oewLmPxqQEoHUAv3u5iYMyQ9AeZZhguYf1T
⏳ Age: 507d
💼 Volume: $1.5k
🔍 KOLs: saale, Loopierr, CoCo

#solana | Chart
```

### Output channels

In the **Output** step, pick where alerts should publish.

* **Telegram**: choose one of your Cielo Telegram bots from the dropdown. Free users have one bot, Pro users two, Whale users get more. See [Telegram](https://docs.cielo.finance/discord-+-telegram-bots/getting-started) for setup.
* **Discord**: click **Connect** to link your Discord. See [Discord](https://docs.cielo.finance/discord-+-telegram-bots/discord) for setup.

You need at least one channel selected. Leave the other one empty to skip it.

### Coming soon

A few triggers are visible in the wizard but tagged **Soon** and not yet live:

* **Dormant Awakening** _(Pro+Whale)_ - a sleeping wallet trades again
* **Strong Floor** _(Pro+Whale)_ - price holds while holder count rises
* **Top Holders Accumulation** _(Pro+Whale)_ - top X wallets quietly add supply
* **Dynamic Holders Tracking** _(Whale)_ - always-on top-20 watch for a single token

The **Templates** and **Activity** tabs on the Research Agents page are also coming soon. Templates will let you spin up agents from saved configurations, and Activity will give you a feed of everything your agents have fired.
