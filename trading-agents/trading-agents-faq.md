# Trading agents FAQ

Answers to the questions we get most about trading agents: why a trade was or wasn't copied, how exits work, what the simulator shows, and what to do when something looks wrong. If your question isn't here, contact support with the agent name, chain, copied wallet and the token or transaction hash.

### Getting started

<details>

<summary>How do I create a trading agent?</summary>

Copy trading runs through trading agents on the Agents page. The quickest way is the Copy Trade button on any wallet profile: pick an agent or create one, then click Start copying. For full control, build the agent yourself.

1. Click Deposit (top right) and fund your Cielo trading wallet on the chain you want. You can also create a trading wallet during setup.
2. Go to Agents > New Trading Agent. Name the agent, choose Wallet Copy, pick the chain and add wallet addresses, or paste a list with + Add batch.
3. In Trading settings, set Amount per buy, filters (market cap, token age, platforms), entry mode (Instant or Buy the dip) and exits. Check the Simulation panel on the right.
4. Click Create & Activate. You can pause, edit or delete the agent any time from the Agents page.

</details>

<details>

<summary>What types of trading agents are there?</summary>

There are two signal types. Wallet Copy buys whenever any wallet you copy buys. Multi-Buy buys only when several of your tracked wallets buy the same token within a time window, and it can use your lists, including public lists you follow. A Trending Token signal is coming soon.

</details>

### Plans and limits

<details>

<summary>How many agents and copied wallets does my plan allow?</summary>

Free plans allow 20 trading agents, Pro 50 and Whale 200. Each agent can copy up to 250 wallets on Free, 750 on Pro and 2,000 on Whale. The Trading Agents page shows your agent count against your limit, and the counter under the wallet list shows how many wallets you've used. If you need more wallets in one strategy, upgrade or split them across several agents.

</details>

### Chains

<details>

<summary>Which chains support trading agents?</summary>

Trading agents run on Solana, Base, Robinhood chain and Arc. Each agent trades on one chain, which you choose when you create it. BSC and Ethereum mainnet aren't supported.

</details>

### Wallet and funding

<details>

<summary>How do I fund an agent?</summary>

Your agent spends from the Cielo trading wallet selected in its settings, on the agent's chain. That wallet needs the token you buy with plus the chain's gas token: SOL on Solana, ETH on Base and Robinhood, even if you buy with USDC or USDG. Arc agents trade with USDC. Click Deposit (top right) to fund it, and keep a buffer so several buys at once don't drain it. On Solana, keep extra SOL for fees and token account rent. On Robinhood, gas can spike to about $0.35 per transaction.

</details>

<details>

<summary>Why did my agent turn itself off?</summary>

An EVM agent switches off when its trading wallet can't pay gas, because every swap would fail. If only the buy amount is short, the agent skips that trade and logs Low balance in the Trades tab (skipped trades) instead. Solana agents skip rather than switch off.

1. Open the agent and check the trading wallet's balance of both the buy token and the gas token.
2. Deposit what's missing, then switch the agent back on.
3. If you use Scaling buys, make sure your balance covers the maximum buy size, or lower the max.

_Applies to: Base, Robinhood and Arc_

</details>

### Copied wallets

<details>

<summary>How do I add many wallets at once?</summary>

In the agent's Signal step, paste an address with an optional label and click + Add wallet, or click + Add batch to paste a whole list. You can also start an agent from any wallet profile with the Copy Trade button. Searching your tracked wallets by label in the add-wallet box isn't available yet.

1. Go to Agents > New Trading Agent, or edit an existing agent.
2. Click + Add batch and paste one address per line.
3. Review the list before saving. If a label lands on the wrong wallet, remove that row and add it again.

</details>

<details>

<summary>Can I copy trade a whole wallet list?</summary>

You can't add a tracked list to a Wallet Copy agent yet. Instead, copy the list's addresses and paste them with + Add batch, or create a Multi-Buy agent, which works with your tracked wallets and lists, including public lists you follow.

</details>

<details>

<summary>Can I give one copied wallet different settings?</summary>

Yes. A wallet you add to an agent inherits the agent's settings. You can then open that wallet's row and override settings such as its buy size or buy limits without affecting the other wallets. For a completely different strategy on the same wallets, create a second agent, ideally with its own trading wallet.

</details>

### Filters

<details>

<summary>Why did my agent skip a trade for market cap?</summary>

The market cap filter is checked at the moment of your buy, using the current price, not the copied wallet's entry. After the copied wallet and other copiers buy, market cap can jump past your max. In Buy the dip mode it can fall below your min. Leave headroom on max for heavily copied wallets. With Buy the dip, lower your min by the dip %: a 200k min with a 10% dip becomes 180k. If the agent bought outside your range, send support the buy transaction hash.

</details>

<details>

<summary>Which platforms should I select?</summary>

The Platforms filter (Token filters > Platforms) only copies buys of tokens trading on the platforms you leave checked, so check every launchpad and DEX your copied wallets trade on. On Base and Robinhood, Uniswap V2, V3 and V4 are unchecked by default because that's where most honeypots are. Checking them copies more trades but raises rug risk. A token launched on a launchpad that later trades on a Uniswap pool still counts as that launchpad. Solana options include Pump.fun, Pump Mayhem mode, PumpSwap, Raydium V4, Raydium CPMM, Raydium LaunchLab, Bonk/LetsBonk, Meteora DBC, Boop, Heaven, Moonit, Token Mill and standard markets.

</details>

<details>

<summary>Why are Stonk.fun tokens missed?</summary>

There's no separate Stonk.fun option. Stonk.fun tokens launch on Raydium LaunchLab and migrate to Raydium CPMM, so check both Raydium LaunchLab and Raydium LP (CPMM) under Platforms. If a buy made through a trading bot was still missed, send support the transaction hash.

_Applies to: Solana_

</details>

<details>

<summary>What does Only copy new positions do?</summary>

Your agent only copies a buy when the copied wallet opens a brand-new position, meaning it held none of that token before. Top-up and averaging-down buys are skipped. If the wallet fully sells and later buys again, that counts as new. To block re-entries completely, combine it with a buy limit such as max buys per token per day or week.

</details>

### Buy sizing

<details>

<summary>Why did my agent buy more than my buy limit?</summary>

Buy limits count per copied wallet, so a limit of 1 buy per hour allows one buy from each wallet in the agent. Failed on-chain buys also count toward the limit, and two signals within 1-2 ms can both pass. To cap exposure per token, also turn on Cross-copied-wallet trade prevention. A conservative start is about 3 buys per hour and 6 per day per wallet. Use max buys per token per day or week to avoid re-buying a token you already exited.

</details>

<details>

<summary>How do Constant and Scaling buy sizes work?</summary>

Amount per buy has two modes. Constant spends the same amount every time. Scaling spends a % of the copied wallet's buy, with a minimum and a maximum: smaller results are skipped and larger ones are capped. Scaling is available on Solana and Robinhood. If Skipped trades shows Scaling buys below your minimum, lower the min. Make sure your balance covers the max buy size.

</details>

<details>

<summary>What is the copied wallet's buy size filter?</summary>

It copies a buy only when the copied wallet spent within a range you set. It filters their buy size, not yours. Use it to ignore dust buys or occasional oversized apes. Set a min, a max or both in the agent settings or on an individual wallet.

</details>

### Execution

<details>

<summary>What does Degen mode do?</summary>

Degen mode turns off the engine's price safety checks, so trades go through at entries it would normally decline and slippage failures become rarer. It's meant for fast launch trading where you accept worse fills. You'll find it under Execution. Leave it off unless you understand the risk of very bad fills.

_Applies to: Solana_

</details>

<details>

<summary>What slippage should I use?</summary>

Default slippage is 30%. About 20-30% suits launchpad trading. Go higher for new bonding-curve tokens and heavily copied wallets, or buys will fail when price jumps. There's no auto-retry, so set it high enough up front. On Pump.fun, slippage is measured from the price after the copied wallet's buy, so your fill can be well above their entry and still be within your slippage. Set it under Execution.

</details>

<details>

<summary>How fast are copy trades on Solana?</summary>

About 70% of copies land in the same slot as the copied wallet, and most of the rest one slot later (about 400 ms). Speed sets your priority fee: Standard (\~0.002 SOL per trade), Turbo (\~0.008 SOL), Godly (\~0.06 SOL) or Custom. Use Turbo or Godly for heavily copied wallets. For MEV protection, Fastest sends straight to the block leader, Balanced avoids leaders known for sandwiching and is a good default, and Protected goes through Jito only. Adding filters doesn't slow down copy buys.

_Applies to: Solana_

</details>

<details>

<summary>Why did my copy buy fill much higher than the copied wallet?</summary>

Big gaps come from buying after the copied wallet and other copiers, who push the price up, and sometimes from routing through a bad pool. Bad-quote protection blocks absurd fills while Degen mode is off, and routing compares DFlow and Jupiter quotes. Use smaller sizes on low-cap tokens where your own price impact is large. If a fill is far off the copied wallet's price, send support the transaction hash.

_Applies to: Solana_

</details>

### Buy the dip

<details>

<summary>How does Buy the dip work?</summary>

Buy the dip waits for price to fall a set % below the copied wallet's entry price, not from the peak or your own entry. If price never drops into range, nothing is bought. If the copied wallet fully sells first, the order is cancelled, but a partial sell leaves it active. The market cap filter is checked at your dip buy, so lower your min market cap by your dip %. To enter right away, switch Entry to Instant. Pending dip orders can't be viewed or cancelled in the app yet.

_Applies to: Solana, Base and Robinhood_

</details>

<details>

<summary>Why did my dip orders fill early or all at once?</summary>

If price crashes through several levels at once, every dip order whose level was crossed fills at about the same time and price. Very small dips (1-10%) often fill almost immediately, sometimes in the same second as the copied wallet, so your entry can be above theirs. Larger dips (20% and up) behave as expected. If a dip buy landed at the wrong moment, send support your buy and the copied wallet's buy transaction hashes.

_Applies to: Solana_

</details>

### Snipe launches

<details>

<summary>How do I snipe token launches?</summary>

Turn on Snipe token launches under Buy. When a wallet you copy deploys a token on a launchpad like Pump.fun, your agent buys it immediately with the amount you set. To snipe only launches, also set Market cap min extremely high (for example $99T) so normal copies are skipped. The option isn't available on Multi-Buy agents. If a launch wasn't sniped, send support the token and deployer address.

_Applies to: Solana_

</details>

### Multi-Buy agents

<details>

<summary>Why didn't my Multi-Buy agent trigger?</summary>

Multi-Buy only counts buys above its min USD per time frame (for example $1k), so several small buys may not trigger it. Also check the number of wallets and the time window, that the agent is on Solana, Base, Robinhood or Arc, and that the wallets are tracked or in a list you follow. Skipped trades are logged for Multi-Buy agents too, with the reason.

</details>

### FOMO and stablecoin buys

<details>

<summary>Can I copy FOMO app wallets?</summary>

Yes. Solana agents copy USDC and USD1 buys as well as SOL buys, and your agent buys the equivalent amount in SOL. On Base, Robinhood and Arc, buys in any quote currency are copied as long as the relevant launchpads are selected in Platforms. There's no FOMO account link, so find the user's wallet address, for example on their Social.Fun profile, and add it to an agent. Small incoming transfers on a FOMO wallet are fees from other users' trades, not its own buys.

</details>

### Not copying trades

<details>

<summary>Why didn't my agent copy a buy?</summary>

Most missed buys are skipped on purpose by your own settings or by a low balance. Check skipped trades first, then failed trades. If the trade appears in neither, send support the transaction hash of the copied wallet's buy.

1. On the Agents page, open the Trades tab, turn off Hide skipped trades and read the reason for that token.
2. Look for a failed attempt in the Trades tab, usually slippage exceeded or insufficient balance.
3. Compare the buy with your filters: market cap, token age, Platforms, Copied wallet's buy size filter, Buy limits and Only copy new positions.
4. Check that the copied wallet spent at least 0.01 SOL. Smaller buys are ignored and not logged.
5. In Buy the dip mode, the agent only buys if price drops into your range. Switch Entry to Instant to buy right away.

</details>

<details>

<summary>Where do I find skipped trades?</summary>

Skipped trades appear in the Trades tab below your agents, next to Active Positions and History. Turn off Hide skipped trades to see them. Each row shows the reason, such as Low balance, Agent disabled, Scam token or Already bought. Other reasons include market cap or token age outside your range, an unselected platform, Only copy new positions, a buy limit reached, a Scaling size below your minimum, or a failed safety check. Adjust the matching setting if you want those trades copied.

</details>

<details>

<summary>Why are my agent's buys failing?</summary>

A failed trade means the agent tried to buy but the transaction didn't go through. Failed trades show in the agent's Trades tab. The usual causes are slippage exceeded, not enough balance at that moment (common when several buys fire at once), or not enough gas on EVM. For slippage failures, raise Slippage or, on Solana, turn on Degen mode if you accept worse fills. For balance failures (error code 1 on Solana), keep more SOL than your buy size. On EVM, keep ETH for gas in the trading wallet.

</details>

<details>

<summary>Why did Cielo show a trade my agent missed?</summary>

Alerts and agents run on separate systems, and your agent also applies your filters and safety checks. Check skipped and failed trades in the Trades tab first. If the trade isn't there, send support the copied wallet's transaction hash.

</details>

### Safety checks

<details>

<summary>Why did a safety check skip my trade?</summary>

The engine skips clearly bad entries: tokens whose freeze authority isn't revoked (Solana), routes with extreme pool fees or tax, and quotes where your entry would be far worse than the copied wallet's. On Solana you can turn off the price checks with Degen mode under Execution if you accept worse fills. On EVM these checks can't be turned off, and the token usually has an unsafe pool.

</details>

### Copy sells

<details>

<summary>How does Sell when copied wallet sells work?</summary>

Your agent exits when the wallet you copied sells, on top of any stop loss, take profit, trailing stop or time limit you set. In proportional mode, shown as Copy sells (prop.) on the agent card, it sells the same share the copied wallet sold: they sell 40%, you sell 40%. It always applies to your whole position in that token, even with Individual TP/SL per buy on.

1. Go to Agents, open the agent and click Edit.
2. Open Trading settings and scroll to Sell.
3. Turn on Sell when copied wallet sells, pick a mode such as Proportionally, and save.

_Applies to: Solana, Base and Robinhood_

</details>

<details>

<summary>Why didn't my agent sell when the copied wallet sold?</summary>

First confirm Sell when copied wallet sells is on and not turned off by a per-wallet override. It also won't fire if the wallet sold into an unusual pair (such as another meme token instead of SOL or USDC), your position was opened by a different copied wallet, the wallet was removed from the agent, or your dip entry filled after the wallet had already sold. Sells that were attempted but failed show in the Trades tab.

1. Go to Agents > Edit > Trading settings > Sell and confirm Sell when copied wallet sells is on.
2. Check the copied wallet's row for an override that turns copy sells off.
3. Look in the Trades tab for a failed or skipped sell on that token.
4. If nothing is logged, sell manually from the token page or Portfolio and contact support.

</details>

<details>

<summary>Why do tiny copy sells cost more in fees than they're worth?</summary>

The copied wallet's buy size filter only applies to buys, so every sell by the copied wallet is mirrored, including tiny reward sells. A minimum copied sell size isn't available yet. To avoid these, turn off Sell when copied wallet sells and rely on take profit, stop loss, trailing stop or time limit.

_Applies to: Solana_

</details>

<details>

<summary>Why did proportional copy sells leave part of my position?</summary>

This can happen when the copied wallet sells, buys back and sells again, or when the token pays rewards into your wallet (for example Stonk tokens). Proportional sells are based on the wallet's balance at each sell, so small remainders can be left. Open the token from Portfolio or the agent's Active Positions and sell the remainder manually.

_Applies to: Solana_

</details>

### Take profit and stop loss

<details>

<summary>Why didn't my take profit trigger?</summary>

Your TP is measured from your own entry, not the copied wallet's, so the chart may look higher than your real gain. Other common causes: the position was opened before you changed the TP and kept the old target, the TP sells only part of the position, or price spiked above the TP and dropped back before the sell could execute. Tokens paired with another meme token can also be harder to price.

1. Check the Sell settings and any per-wallet override for the actual TP % and sell %.
2. Compare when the position was opened with when you last edited the TP.
3. Compare the TP to your own entry price.
4. If it's still unexplained, contact support with the token and transaction.

</details>

<details>

<summary>Why did my agent sell at my old take profit?</summary>

Editing TP/SL settings only applies to future buys. Positions opened before your edit keep their original targets. To change an open position, open the token in the trading terminal and set your own TP/SL order.

</details>

<details>

<summary>How does Individual TP/SL per buy work?</summary>

Each buy of the same token is tracked as its own entry. Take profit, stop loss, trailing stop and time limit are measured from that buy's price and sell only that buy's amount. For example, buys at $1.00, $0.80 and $0.60 with a 20% TP sell separately at $1.20, $0.96 and $0.72. Sell when copied wallet sells still applies to the whole position. Changes apply to future buys only. Turning it off merges new buys again but keeps existing entries separate.

1. Go to Agents > New Trading Agent, or edit an agent, and open Trading settings > Sell.
2. Turn on Individual TP/SL per buy and save.

</details>

<details>

<summary>How do take profit tiers add up?</summary>

Each TP or SL tier sells a percentage of your original position, so tiers stack predictably: 50% at +50% and 50% at +100% sells everything. Make sure your tiers add up to 100% if you want a full exit. If a small balance is left after all tiers fire, it's usually rounding dust or reward tokens outside the agent's position. Sell it manually from the token page or Portfolio.

</details>

<details>

<summary>Why did my stop loss trigger early?</summary>

Stop loss and take profit are measured from your own entry price, not the copied wallet's. Your entry is often worse than theirs, so you can hit your stop loss before the chart suggests. On very illiquid tokens, a single swap in a thin pool can also move price enough to trigger it. Check your buy price in the Trades tab, and give volatile low caps a wider stop, for example -30% instead of -15%.

</details>

<details>

<summary>Why didn't my stop loss fire on a quick wick?</summary>

Stop loss and take profit won't fire if price only touches the level and recovers immediately. The agent needs to see price at the level long enough to execute, so one-candle wicks are often skipped on purpose to avoid selling at the worst tick.

</details>

<details>

<summary>Why did my stop loss sell far below the trigger?</summary>

Stop losses sell at market, so on fast-moving or illiquid tokens the fill can land well below the trigger. On tokens paired with another meme token, the quote token's own move can trigger your stop loss, so use a wider stop loss or none on those pairs. If you think the sell was routed badly, send support the transaction signature.

_Applies to: Solana_

</details>

<details>

<summary>Does TP/SL work on tokens paired with another token?</summary>

Yes, but tokens whose main pool is paired with another token instead of SOL, USDC or USD1 (for example Stonk, Fartcoin or HYPE pairs) are harder to price and route. If a take profit or stop loss misses on one of these tokens, send support the transaction.

_Applies to: Solana_

</details>

### Trailing stop and time limit

<details>

<summary>Why did the trailing stop sell the rest after my take profit?</summary>

That's expected when your TP sells less than 100%. The TP sold its share (for example 50%), then the trailing stop sold the remainder when price fell the set % from its peak. If you want the TP to be your full exit, make your TP tiers add up to 100%.

</details>

<details>

<summary>How does the trailing stop work?</summary>

The trailing stop follows price up and sells your whole remaining position when price drops a set % from its peak. Activation sets when trailing starts: trail 20% with activation 50% means that once you're up 50%, the agent sells if price then falls 20% from its high. Set activation to 0 to trail from entry. It works on Wallet Copy and Multi-Buy agents.

1. Go to Agents > New Trading Agent, or edit an agent.
2. Open Trading settings and scroll to Sell.
3. Turn on Trailing Stop and set the trail % and activation %.

</details>

<details>

<summary>How does the time limit sell work?</summary>

Time Limit sells your position a set time after the buy, whatever the price. You can set it in seconds, hours or days and add tiers, for example 50% after 6 hours and the rest after 24 hours. Turn it on under Trading settings > Sell.

</details>

### Positions

<details>

<summary>Why did one wallet's sell close a position another wallet opened?</summary>

Within one agent there's one position per token per trading wallet, not one per copied wallet. If wallets A, B and C all buy the same token, a sell by any of them can reduce the shared position. Turn on Cross-copied-wallet trade prevention (Solana, Base and Robinhood) so only the wallet that opened your position can trade it. For fully independent strategies, use separate agents with separate trading wallets.

</details>

<details>

<summary>Why are several buys of the same token shown as one position?</summary>

By default an agent keeps one position per token per trading wallet. Each new buy adds to it, and TP/SL targets are recalculated from the new average entry. To have each buy exit on its own, turn on Individual TP/SL per buy under Sell. To keep two strategies fully apart, give each agent its own trading wallet.

</details>

<details>

<summary>Why is a small amount of the token left after my agent sold?</summary>

The leftover is usually reward tokens, such as Stonk rewards, that reached your wallet outside the agent's trades. Agents only sell their own position, so tokens from other sources stay behind. Find the token in Portfolio and sell it manually.

_Applies to: Solana_

</details>

### Closing and disabling

<details>

<summary>What happens to open positions if I remove a wallet from my agent?</summary>

Nothing automatic. Positions opened from that wallet stay open and your TP/SL rules keep applying. Copy sells for those positions stop because the wallet is no longer followed, so you'll need to close or manage them yourself.

</details>

### Failed sells

<details>

<summary>Why did my agent's sell fail?</summary>

Most failed sells come from slippage (price moved more than your tolerance) or balance (not enough SOL or ETH for fees at that moment). Failed trades appear in the agent's Trades tab.

1. Open the Trades tab, find the failed sell and open the transaction on the explorer.
2. Check the error and the wallet's SOL or ETH balance at that moment.
3. Raise Slippage under Execution (it applies to sells too), or turn on Degen mode on Solana.
4. Top up SOL or ETH for fees.
5. If the position is still open, sell it manually.

</details>

<details>

<summary>Why isn't my Base or Robinhood agent selling?</summary>

EVM agents need ETH in the trading wallet for gas on every buy and sell, even if they trade with USDG or USDC. If gas runs out, sells fail and the agent can switch itself off. Keep a buffer, since Robinhood gas can spike 10-15x to around $0.35 per transaction. The app shows low gas warnings for deposits and agents.

1. Deposit ETH to the agent's trading wallet.
2. Check the Trades tab for failed sells.
3. Switch the agent back on if it was disabled.

_Applies to: Base and Robinhood_

</details>

<details>

<summary>Why can't I sell a token my agent bought?</summary>

Some EVM tokens are honeypots built so they can't be sold. Agents run spam and route checks, but the safest protection is to copy only platforms you trust. Under Token filters > Platforms, leave Uniswap V2, V3 and V4 unchecked (the default for new Base and Robinhood agents) and select only launchpads you trust. If a honeypot slipped through, send support the token address.

_Applies to: EVM chains_

</details>

### Simulator

<details>

<summary>Where is the simulator and what does it include?</summary>

The simulator is the panel on the right when you create or edit an agent. It replays your settings on the copied wallets' real trades over 1D, 3D or 7D. Options include Precise fills (on by default), Worst-price fills for a pessimistic view, Starting loss per buy, and Ask AI, which suggests settings you can apply. Results are hypothetical.

1. Go to Agents > New Trading Agent, or edit an agent.
2. Add at least one wallet and an amount per buy.
3. Set your exit rules and pick 1D, 3D or 7D.

</details>

<details>

<summary>Why are my live results worse than the simulation?</summary>

The simulator can't fully reproduce live execution. Your real buy lands after the copied wallet and other copiers, at a worse price, and can fail on slippage or balance. The simulation deliberately leans pessimistic so it doesn't over-promise. Stress-test with Worst-price fills, keep amounts small on low-cap tokens, and test a new setup live with a small size first. If a token differs a lot, send support the token and copied wallet address.

</details>

<details>

<summary>What do Precise mode and Worst-price fills do?</summary>

Precise mode simulates entries and exits at 1-second granularity, which matters when many trades happen within a minute. Worst-price fills also turns on Precise. It looks at the 1-second candle of each fill and the next one, and uses the highest price for buys and the lowest for sells. With it on, a take profit can show a small loss, which models a real-world bad fill. For a simpler haircut, set a starting loss % per buy.

</details>

<details>

<summary>Why does the simulation show trades my agent never made?</summary>

Some differences are expected. Live filters like min market cap are checked at the moment of your buy, while the simulation uses candle prices. A dip entry can appear in the simulation but never fill, and live trades can be skipped for balance or fail on slippage.

1. Scroll to the bottom of the simulation panel to see its own skipped trades section.
2. Check the agent's Trades tab for skipped or failed trades on the same token.
3. If nothing explains it, send support the wallet and token.

</details>

<details>

<summary>Why do wallets lose money when simulated together?</summary>

Turn on Precise for the combined simulation so it's comparable with single-wallet results, which use Precise by default. Combining wallets can also genuinely change results because of buy limits and Cross-copied-wallet trade prevention.

</details>

<details>

<summary>What should I do if the simulation won't load?</summary>

Try fewer wallets or a shorter period, for example 1D instead of 7D, then refresh and retry. Very large results (above 9,999%) can also cause an error. If it still fails, send support the wallet addresses and your settings.

</details>

<details>

<summary>Why does Ask AI show a different PnL than the simulation?</summary>

That's expected. The full simulation is more precise than the quick Ask AI search, so numbers can shift after you apply a suggestion. Trust the simulation figure. Ask AI returns Recommended and Max profit setups, and tells you when it can't find a profitable one.

</details>

### Agent PnL and stats

<details>

<summary>Why does the Trades table show the wrong reason or agent for a sell?</summary>

Some sells can be labelled incorrectly in the Trades table. Open the transaction on the explorer to confirm what happened, and send support the transaction if it's mislabelled. The Current MC column shows today's market cap, not your fill.

</details>

<details>

<summary>Can I compare my entry to the copied wallet's entry?</summary>

Not side by side yet. The Trades table shows which wallet was copied and your own fill. Click the copied wallet's address to open its token PnL and compare manually.

</details>

### Results vs the copied wallet

<details>

<summary>Why is my result worse than the copied wallet's?</summary>

You always buy after the copied wallet, and often after other copiers, so you enter higher and exit later. The gap grows on illiquid tokens, on heavily copied wallets, and when the trader averages into a position opened much lower. Pick wallets whose edge survives that delay, keep sizes small on low caps, and run the simulator with Worst-price fills before going live. Buy the dip can help you avoid buying the top of the copier rush.

</details>

### Fees

<details>

<summary>What fees do agent trades pay?</summary>

Agent trades carry a 1% Cielo fee on each executed buy and sell, compared with 0.6% on manual trades. You also pay network costs. On Solana that's the priority fee set by Speed (Standard \~0.002 SOL, Turbo \~0.008 SOL, Godly \~0.06 SOL) and refundable token account rent. On EVM chains it's gas.

</details>

### Notifications

<details>

<summary>Can I get Telegram notifications when my agent trades?</summary>

There are no built-in agent trade notifications yet. Instead, track your agent's trading wallet like any other wallet and you'll get an alert whenever it buys or sells. The app also shows low gas warnings for agents.

1. Copy the agent's trading wallet address from Agents > Edit > Buy > Wallet, or from Portfolio.
2. On the Tracking page, add the wallet and label it, for example My agent.
3. Turn on alerts for it in your Telegram bot or Discord.

</details>

### Not available yet

<details>

<summary>Can I blacklist tokens, delay buys or cap spend per token?</summary>

Not yet. Token blacklists, max-buyer filters, buy delays and a max SOL per token limit aren't available. To avoid re-buying a token you sold, set max buys per token per week under Buy limits.

</details>

<details>

<summary>Can an agent buy from research agent signals?</summary>

Not yet. Research agents only send alerts. For confluence buying, use a Multi-Buy trading agent. Agents that learn from your own trading style aren't available.

</details>
