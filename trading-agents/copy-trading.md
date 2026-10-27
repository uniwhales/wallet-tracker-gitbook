---
description: Copy any wallet's buys automatically, with your own size, filters and exits.
---

# Copy trading

The wallets you already track are two clicks from being copied. When they buy, your agent buys, with your size, your filters and your exit rules.

## What a copy trading agent can do

* Copy buys from up to 250 wallets per agent on Free, 750 on Pro and 2,000 on Whale
* Copy SOL, USDC and USD1 trades on Solana, so wallets trading from apps like Fomo can be copied too
* Skip tokens by market cap, token age and launch platform
* Enter straight away or wait to buy the dip
* Exit on your terms: copy the wallet's sells, or use stop loss, take profit, trailing stop, time limit and break even rules
* Buy a token the moment a wallet you copy launches it
* Show you how the setup would have done over the last 7 days before you turn it on

{% embed url="https://x.com/CieloFinance/status/2081771797360283896" %}

## Copy a wallet in two clicks

Every [wallet profile](../wallet-tracking/my-wallets/wallet-profiles.md) has a **Copy Trade** button. Click it, pick the agent that should copy the wallet (or create a new one on the spot) and confirm. The wallet uses that agent's buy size, filters and exits, and you can change any of them for this wallet before you start.

Check the wallet's **Copy score** on its profile first. It rates from 0 to 100 how well the wallet's trading style suits copy trading.

Found someone in the Feed, in Discovery or on the PnL Leaderboard? You're two clicks from copying them.

In Telegram, send `/add @username` to find a fomo or Pump.fun trader by their username, track them and copy trade them in one setup. See [Telegram trading](../trading/telegram-trading.md).

{% embed url="https://x.com/CieloFinance/status/2080640204843434494" %}

## Create an agent

Click **New Trading Agent** on the Agents page. Start from a template or from scratch. It takes two steps.

{% stepper %}
{% step %}
### Signal

1. Name your agent so you'll recognize it later.
2. Pick **Wallet Copy** as the signal type.
3. Pick a chain: **Solana**, **Robinhood**, **Base** or **Arc**.
4. Add the wallets to copy. Paste an address and an optional label, click **+ Add batch** to paste a list (one `address,label` per line), or **+ Browse tracked** to pick from wallets you already track. Paste EVM addresses into a new Solana agent and Cielo switches it to Robinhood for you.

You can leave the list empty and add wallets after the agent is created.
{% endstep %}

{% step %}
### Trading settings

Set what the agent buys, how it enters and how it exits. The defaults are a reasonable start. At minimum, check:

* **Amount per buy**: what the agent spends each time it copies a buy.
* **Stop loss**: on by default at -30%, selling 100% of the position.
* **Take profit**: on by default at +50%, selling 100% of the position.

Every option is explained in [Agent settings](agent-settings.md).

Click **Create & Activate**. The agent starts right away. Pause, edit or delete it any time from the Agents page. Pausing stops new buys but keeps the exits running on open positions. See [Pausing an agent](overview.md#pausing-an-agent).
{% endstep %}
{% endstepper %}

While you build the agent, the panel on the right shows a live summary and a [simulation](simulator.md) of how these exact settings would have performed on the wallets' real trades. Use **Ask AI** to have it search for the settings those wallets responded best to.

## Manage copied wallets

Open an agent to see the wallets it copies, with each wallet's balance, PnL from your copies, unrealized PnL and trades per token. Columns are sortable.

* **Per-wallet settings** override the agent's settings for one wallet, for example a smaller buy size for a riskier trader.
* **Move** wallets to another agent on the same chain type. Labels and per-wallet settings come along.
* **Remove** a wallet in one click. If it has open positions, you'll be asked to confirm. Positions it opened stay open and your exits keep running on them.

## Robinhood, Base and Arc

EVM agents work the same way, with a few differences:

* The platform list covers EVM launchpads and DEXs, such as Virtuals, Clanker, Flaunch, Bankr, Pools, Pons, Up, Hood and Uniswap. Uniswap V2, V3 and V4 are off by default on new agents.
* Extra token filters for **Liquidity** and **Volume 24h**.
* Buy with ETH or USDG on Robinhood, ETH or USDC on Base, and USDC on Arc.
* **Ultra-fast FOMO & Pump.fun copy trading** (Robinhood) copies trades made in the Fomo and Pump.fun apps at ultra-fast speed. While it's on, the agent ignores swaps made anywhere else, so only use it for wallets that trade from those apps.

{% embed url="https://x.com/CieloFinance/status/2106157335131341149" %}

{% embed url="https://x.com/CieloFinance/status/2086834078964203830" %}

## FAQ

<details>

<summary>What settings should I start with?</summary>

Start small. Keep each buy under 10% of your balance, and under 2% if your balance is large. Lower the amount per buy as you add more wallets, so ten wallets buying at once can't drain you. Set buy limits per wallet: around 3 buys per hour and 6 per day is a careful start, and you can loosen it once you trust the wallet.

</details>

<details>

<summary>I copied a profitable trade. Why is mine at a loss?</summary>

You're always second in line. By the time your buy lands, the wallet's own buy (and every other copier's) has already pushed the price up, so you enter higher and exit later. The gap is worse on illiquid tokens, on heavily copied wallets, and when the wallet is averaging into a position it opened much lower. Some wallets also look better than they are because they never sell their losers. The [copy trading guide](../guides/copy-trading/) covers how to pick wallets where the edge survives the delay.

</details>

<details>

<summary>Why did my agent skip a trade?</summary>

Usually one of your own settings: the token's market cap or age was out of range, its platform was unchecked, the buy went over a buy limit, a scaled buy came in under your minimum, the token is on your blocklist, or your wallet didn't have enough balance or gas. The engine also refuses clearly bad entries: it won't buy tokens whose freeze authority hasn't been revoked, and it skips trades where your price would be far worse than the wallet's. Open the agent's **Trades** tab to see the reason for each skip.

</details>

<details>

<summary>Why did my agent buy the same token twice?</summary>

Two of your copied wallets bought it, or one wallet bought it twice. Buy limits count per wallet, not per token. Turn on **Cross-copied-wallet trade prevention** so only the first wallet that triggered a position can add to it, and **Only copy new positions** so averaging-down buys don't count.

</details>

<details>

<summary>My buys on pump.fun keep failing. What gives?</summary>

Slippage. New bonding-curve tokens move fast, and if the price jumps past your slippage before the transaction lands, it's rejected. Raise slippage for launchpad tokens and heavily copied wallets, and accept that you'll sometimes pay more. Tight slippage misses fills; loose slippage fills at worse prices.

</details>

More questions are answered in the [Trading agents FAQ](trading-agents-faq.md).
