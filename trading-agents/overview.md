---
description: Agents that trade for you when the wallets you follow make a move.
---

# Overview

You've always used Cielo to find and track wallets, then had to go somewhere else to act on them. Trading agents close that gap. An agent watches the wallets you choose and buys when they buy, with your size, your filters and your exit rules, so the trade happens whether or not you're at the screen.

Cielo acquired OdinBot, the copy trading bot with $250M in volume, and built its engine into the app. On Solana, about 70% of copy trades land in the same slot as the wallet being copied.

{% embed url="https://x.com/CieloFinance/status/2080640098308116866" %}

## Signal types

Every agent runs on one signal, which decides when it buys.

| Signal                             | When the agent buys                                                                                                                        |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Wallet Copy**                    | A wallet you copy buys a token. This is copy trading. See [Copy trading](copy-trading.md).                                                 |
| **Multi-Buy**                      | Several of your tracked wallets buy the same token inside a short window. You're trading on confluence instead of one wallet's conviction. |
| **Trending Token** _(coming soon)_ | A token climbs the trending rankings.                                                                                                      |

Whichever signal you pick, most of the same settings apply: token filters, buy size, execution, and exit rules. They're all listed in [Agent settings](agent-settings.md).

{% embed url="https://x.com/CieloFinance/status/2095549109994139723" %}

## Chains

Agents run on **Solana, Base, Robinhood and Arc**. Each agent trades on one chain, from one of your [trading wallets](../trading/portfolio.md#wallets) on that chain. Fund the wallet before you turn the agent on, including a little extra for gas: SOL on Solana, ETH on Base and Robinhood, USDC on Arc.

## The Agents page

Everything lives on the [Agents](https://app.cielo.finance/agents) page, in two tabs: **Trading Agents** and [**Research Agents**](../wallet-tracking/research-agents/). The counter at the top shows how many agents you have against your plan limit.

**Summary** shows realized and unrealized PnL, win rate, total trades, tokens traded, buys and sells, median hold time and fees, for the chain and timeframe you pick (**1D**, **7D**, **30D**, **Max**). The **Token Profit Distribution** buckets every token your agents traded by return. Turn off **Include my manual sells** to see your agents' results without the sells you made by hand.

Below that, each agent has its own card with its status (**Running** or **Paused**), the wallets it copies, its trading wallet and balance, fees paid and a summary of its buy and exit settings. Drag the cards to reorder them.

Positions and trades are grouped by agent:

* **Active positions**: what your agents hold now, with live PnL
* **History**: closed positions
* **Trades**: every buy and sell, including skipped trades and why they were skipped. Toggle **Hide skipped trades** to clean the list up.

## Pausing an agent

Pausing stops new buys. Exit rules keep running on positions the agent already holds, so stop loss, take profit, trailing stop, time limit and copy sells still fire. To stop the agent selling too, turn off its exits under **Sell** or close the positions yourself.

## Blocklist

The **Blocklist** applies to all your agents at once.

* **Tokens** you block are never bought by any agent. Skipped trades show the reason "blocked token".
* **Wallets** you block are removed from every agent and you'll get a warning if you try to add them again.

## Agents in the terminal

Open **Agents** from the footer of the trading terminal to trade alongside your agents. You can turn an agent on or off, see every copied buy and sell on the chart and in **Activity**, and sell part of a position yourself. The agent keeps managing the rest by its settings. If you sell the whole position by hand, the agent stops managing it.

{% embed url="https://x.com/CieloFinance/status/2108527912311722448" %}

{% embed url="https://x.com/CieloFinance/status/2110344629098856587" %}

## Agents on mobile

You can create agents, turn them on or off and track their PnL from the Cielo Telegram mini app. See [Telegram trading](../trading/telegram-trading.md#mini-app).

{% embed url="https://x.com/CieloFinance/status/2113324515296264235" %}

## Limits

|                          | Free | Pro | Whale |
| ------------------------ | ---- | --- | ----- |
| Trading agents           | 20   | 50  | 200   |
| Copied wallets per agent | 250  | 750 | 2,000 |

## Fees

Trades placed by agents cost 1%. Priority fees and tips go to the network.
