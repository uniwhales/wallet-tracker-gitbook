# Overview

You've always used Cielo to find and track wallets... but had to go elsewhere to act on them. Not anymore. Agents act on what your tracked wallets do, automatically, so the edge doesn't depend on you being awake.

Cielo acquired OdinBot, the undefeated, fastest copy trading bot with $250M in volume, and built its engine directly into the app. When a wallet you copy buys a token, your agent buys it too, from alert to fill, without you touching anything. 70% of copies land in the same slot as the wallet copied. The copy trade lands before the fomo notification does.

Everything lives on the [Agents page](https://app.cielo.finance/agents), split into two tabs:

* **Trading agents**: Execute on-chain for you, with your own size, entry, and exit rules. This section covers them.
* **Research agents**: Watch the chain and alert you when specific patterns fire, like a KOL cluster buy or a fresh wallet accumulating. See Research agents.

Agents run on Solana, Base, and Robinhood Chain. Each agent is tied to one chain and trades from your Cielo trading wallet on that chain (click **Deposit** in the top right if you haven't funded one yet).

**Signal types**

Every trading agent runs on a signal that decides when it buys:

* **Wallet Copy**: When a tracked wallet buys a token, your agent buys it too. This is copy trading, the main event: see **Copy trading** for the full walkthrough.
* **Multi-Buy**: Enters when several tracked wallets buy the same token within a short window. Confluence over conviction in any single wallet.
* **Trending Token** _(coming soon)_: Enters tokens as they climb the trending rankings across social and volume metrics.

Whatever the signal, the same controls apply: token filters, buy sizing, execution, and exit rules. The full reference is on the **Agent settings** page.

### Track your performance

The Agents page doubles as your dashboard for every agent you run.

**Summary panel**: Realized and unrealized PnL, win rate, total trades, tokens traded, buys/sells, and median hold time for the timeframe you select (1D, 7D, 30D, or Max). The **Token Profit Distribution** chart buckets every traded token by return, from below -50% to above +500%, so you can see the shape of your results, not just the total.

**Chain filter**: View performance for all chains together or Solana, Base, and Robinhood individually.

**Agents list**: Each agent shows as Running or Paused. Pause or edit an agent any time; its settings and history are kept.

**Positions tables**: Three tabs track the actual trades:

* **Active positions**: What your agents currently hold, with live PnL.
* **History**: Closed positions.
* **Trades**: Every individual buy and sell.

### Fees

Trading agents charge a 1% fee per executed trade.
