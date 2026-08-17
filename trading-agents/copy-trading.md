# Copy Trading

Track. Trade. Copytrade. From alert to fill.

The wallets you already track are two clicks from being copied. When they buy, your agent buys, with your size, your filters, and your exit rules.

**What a copy trading agent can do**

* Copy buys from up to 250 wallets per agent on the Free plan, 750 on Pro, and 2,000 on Whale
* Copy USDC trades as well as SOL on Solana, which means fomo wallets can be copied too
* Filter which tokens it copies by market cap, token age, and launch platform
* Enter instantly or wait to buy the dip
* Exit on your terms: copy the wallet's sells, or rely on tiered stop loss and take profit rules
* Snipe token launches from wallets you copy, the moment they deploy
* Simulate its performance against the last 7 days before you run it

### Copy a wallet in two clicks

Every wallet profile has a **Copy Trade** button. Click it, pick which of your agents should copy the wallet (or spin up a new agent on the spot), and hit **Start copying**. The wallet inherits that agent's buy size, filters, and exit strategy, and you can customize any of it for this wallet before you start.

Found someone in your Feed, in Discovery, or on the PnL Leaderboard worth following? You're two clicks from mirroring them.

### Create an agent

Want to set your own filters and exits? Click **New Trading Agent** on the Agents page. Two steps, about a minute.

**Step 1: Signal**

1. **Name your agent**. Something you'll recognize in the dashboard later.
2. **Pick a signal type**. For copy trading, that's **Wallet Copy**.
3. **Pick a chain**: Solana, Base, or Robinhood.
4. **Add wallets to copy**. Paste an address, add an optional label, and click **+ Add wallet** for more, or **+ Add batch** to paste a list. Limits depend on your plan: 250 copied wallets per agent on Free, 750 on Pro, 2,000 on Whale. You can also leave this empty and add wallets after creating the agent.

The panel on the right shows a live summary of your draft, and a **Simulation** of how it would have performed over the last 1, 3, or 7 days once you've filled in a wallet and buy amount. Use it to sanity-check your settings before running anything.

**Step 2: Trading settings**

This is where you set what the agent buys, how it enters, and when it exits. The defaults are sensible; the full reference is on the **Agent settings** page. At minimum, check:

* **Amount per buy**: How much the agent spends on every copied buy.
* **Stop loss and take profit**: On by default, at -30% sell 100% and at +100% sell 50% respectively. Adjust to taste.

Click **Create & Activate**. Your agent starts running immediately, and you can pause, edit, or delete it at any time from the Agents page.

### FAQ

<details>

<summary>What settings should I start with?</summary>

Start small. Keep each buy under 10% of your account, and under 2% if your account is large. Scale your per-buy amount down as you add more copied wallets, so ten wallets firing at once can't drain your balance. On Solana, set buy limits per wallet: something like 3 buys per hour and 6 per day is a conservative start, and you can loosen it once you trust the wallet. The engine keeps a buffer of SOL in reserve so you can always close positions.

</details>

<details>

<summary>I copied a profitable trade. Why is mine at a loss?</summary>

You're always second in line. By the time your buy lands, the original wallet's buy (and every other copier's) has already pushed the price up, so you enter higher and exit later. The gap gets worse with illiquid tokens, with heavily copied wallets, and when the trader you copy is averaging into a position they opened much lower, which makes their percentage gain look better than anything you could have matched. Some wallets also look better than they are because they never sell their losers. This is the core tradeoff of copy trading; the [copy trading guide](https://docs.cielo.finance/guides/copy-trading) covers how to pick wallets where the edge survives the delay.

</details>

<details>

<summary>What happens to open positions if I remove a wallet from my agent?</summary>

Nothing, automatically. Positions opened from that wallet's activity stay open, and your stop loss and take profit rules keep applying. If you also had sell-when-copied-wallet-sells on, that trigger is gone with the wallet, so close or manage those positions yourself.

</details>

<details>

<summary>Why did my agent skip a trade?</summary>

Usually one of your own filters: the token's market cap or age was outside your range, its platform was unchecked, the buy would have exceeded your buy limits, or a Scaling buy sized below your minimum. The engine also protects you from clearly bad entries: it won't buy tokens whose freeze authority hasn't been revoked, and it declines trades where your entry price would be far worse than the wallet you're copying.

</details>

<details>

<summary>Why did my agent buy the same token twice?</summary>

On Solana, turn on **Duplicate buy protection**: once your agent holds a token, further buy signals for it are ignored, no matter which of your copied wallets triggers them. Without it, two wallets buying the same token means two buys, because buy limits count per wallet, not per token. **Only copy new positions** also cuts repeats, since averaging-down buys stop qualifying.

</details>

<details>

<summary>My buys on pump.fun keep failing. What gives?</summary>

Slippage. New bonding-curve tokens move violently, and if the price jumps beyond your slippage tolerance before your transaction settles, the trade is rejected. Raise slippage for launchpad trading and for heavily copied wallets, and accept that you'll sometimes pay up. That's the risk-reward dial: tight slippage misses fills, loose slippage fills at worse prices.

</details>
