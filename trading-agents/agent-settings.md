# Agent settings

Every agent setting and what it does. You can edit any of these after the agent is created.

#### Token filters

Controls which copied buys the agent acts on. Buys that don't pass the filters are skipped.

* **Market cap**: Minimum and maximum market cap in USD.
* **Token age**: Minimum and maximum age, in hours.
* **Platforms**: Only copy buys for tokens traded on the platforms you leave checked. On Solana this covers Pump.fun, Pump "Mayhem mode", PumpSwap, Raydium V4, Raydium LP (CPMM), Raydium LaunchLab, Bonk / LetsBonk, Meteora DBC, Boop, Heaven, Moonit / Moonshot, Token Mill, and standard Solana markets.

#### Buy

* **Wallet**: The trading wallet the agent spends from.
* **Amount per buy**: How much the agent spends on each copied buy.
  * **Constant** buys the same fixed amount every time, regardless of what the copied wallet spends.
  * **Scaling** sizes your buy as a percentage of the copied wallet's buy, inside bounds you set. Three parameters: the multiplier (percentage of their trade size), a minimum (trades that would size below it are skipped), and a maximum (larger trades are capped there). A 1% multiplier mirrors a big trader proportionally; a 200% multiplier trades more aggressively than a small one.
* **Copied wallet's buy size filter**: Only copy a buy when the copied wallet spent within a range you set. This filters their buy size, not the size of your own buy. Useful for ignoring a whale's dust buys, or their occasional oversized ape.
* **Entry**: **Instant** copies the tracked wallet's buys immediately, with no delay. **Buy the dip** waits for a pullback instead.
* **Execution**: How aggressively your buys chase the next block, and how they're protected on the way there.
  * **Speed** sets how your copy trades are prioritized on-chain through the priority fees each trade pays. **Standard** (\~0.002 SOL per trade) is fast in normal conditions. **Turbo** (\~0.008 SOL) stays fast even when the network is congested. **Godly** (\~0.06 SOL) is for winning races on heavily copied wallets. **Custom** lets you set your own fees.
  * **MEV protection** shields your trades from sandwich and front-running bots. **Fastest** routes directly to the block leader, **Balanced** only sends to leaders with no history of sandwiching, and **Protected** routes exclusively through Jito, where sandwiching is prohibited.
  * **Slippage** is the maximum price movement you'll accept before a trade is rejected (default 30%). Raise it for early bonding-curve tokens and heavily copied wallets, where prices jump fast; keep it tight elsewhere.
  * **Degen mode** switches off the engine's price safety checks, so trades execute even at entries the engine would normally decline. Leave it off unless you know exactly why you're turning it on.
* **Only copy new positions**: Only copy a buy when the tracked wallet is opening a brand-new position, meaning its balance for that token was zero. Filters out averaging-down buys.
* **Duplicate buy protection** _(Solana agents, in the agent's settings after creation)_: Once your agent has bought a token, further buy signals for that token are ignored, across every wallet the agent copies. Two wallets aping the same launch means one buy, not two.
* **Snipe token launches**: When a wallet you copy launches a token on a launchpad like Pump.fun, buy it immediately.
* **Buy limits** _(Solana agents)_: Caps how often your agent buys. Unlimited by default; individual wallets can override the cap.

#### Sell

* **Sell when copied wallet sells**: Exit alongside the wallet you copy, instead of relying only on your stop loss and take profit rules.
* **Stop loss**: Sells a share of your position at each loss tier. Default: at -30%, sell 100% of the position. Add tiers to scale out in steps; together they can sell up to 100%.
* **Take profit**: Same idea in the other direction. Default: at +100%, sell 50% of the position. Add tiers to ladder your exits.

Each sell percentage applies to the original position size, so tiers stack predictably.
