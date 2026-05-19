# Research Agents

The [Research Agents](https://trading.cielo.finance/agents/research) page lets you spin up a watcher that pings you the moment a specific onchain pattern fires. Pick a trigger, tune the filters, point it at a Telegram bot or Discord channel, and the agent does the watching so you can focus on the trade.

Each agent does one job: it watches the chain for a specific signal and posts an alert when it fires. No copy trading, no execution. You decide what to do with the alert.

\{% hint style="info" %\} Research Agents work alongside your existing Cielo alerts. You can route each agent to a different Telegram bot or Discord channel so the signals stay sorted. \{% endhint %\}

### Creating an agent

From the Research Agents page, click **Make an agent** (or **Make my first agent** if you don't have any yet). The wizard walks you through five steps:

1. **Trigger** - Pick which onchain pattern should fire this agent.
2. **Filters** - Tune the trigger. Each trigger has its own filter set.
3. **Output** - Pick a Telegram bot, a Discord channel, or both. You need at least one to continue.
4. **Name** - Give the agent a short label so you recognise it at a glance.
5. **Preview** - Review the configuration and see a sample alert. Click **Activate agent** to go live.

Once active, the agent runs immediately and starts posting to your chosen channels.

### Available triggers

Triggers are grouped by what they watch.

**Wallet activity** (single-wallet signals):

* **CEX Fresh Buy** _(Whale)_ - brand-new CEX-funded wallet bought above $1k on its first token
* **Fresh Wallet Buy** _(Whale)_ - newly funded wallet accumulates a token
* **Your Wallet Funded a New Wallet** _(Pro+Whale)_ - a tracked wallet funds a fresh wallet

**Aggregate signal** (multiple wallets lining up):

* **KOL Cluster Buy** _(Free)_ - three or more verified KOLs buy the same token in a chosen timeframe

### Popular starting points

The Research Agents landing page surfaces three quick-start cards at the bottom: **Your Wallet Funded a New Wallet**, **CEX Fresh Buy**, and **KOL Cluster Buy**. Clicking any of them opens the wizard pre-loaded with that trigger.

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

&#x20;

