---
description: Every trading agent setting and what it does.
---

# Agent settings

This is the full list of trading agent settings, in the order they appear under **Trading settings**. You can change any of them after the agent is created, and many can also be changed for a single copied wallet.

Settings marked _Solana_ or _EVM_ only exist on that type of agent. EVM covers Base, Robinhood and Arc.

## Token filters

Filters decide which buys the agent copies. A buy that fails a filter is skipped, and the reason shows in the agent's **Trades** tab.

| Setting                | What it does                                                       |
| ---------------------- | ------------------------------------------------------------------ |
| **Market cap**         | Minimum and maximum market cap in USD.                             |
| **Token age**          | Minimum and maximum token age, in seconds, minutes, hours or days. |
| **Liquidity** _(EVM)_  | Minimum and maximum pool liquidity in USD.                         |
| **Volume 24h** _(EVM)_ | Minimum and maximum 24 hour volume in USD.                         |
| **Platforms**          | Only copy buys of tokens on the platforms you leave checked.       |

On Solana, **Platforms** covers Pump.fun, Pump "Mayhem mode", PumpSwap, Raydium V4, Raydium CPMM, Raydium LaunchLab, Bonk / LetsBonk, StonkFun, Meteora DBC, Boop, Heaven, Moonit / Moonshot, Token Mill and standard Solana markets.

On EVM it covers the launchpads and DEXs on that chain, such as Pools.trade, Pools.fun, Up, Pons, Noxa, Virtuals, Flap, Trench, Bankr, Long.xyz, Clanker, Flaunch, Bow, Bags, Hood, Sushi Launchpad, Varo, o1 Launchpad and Uniswap V2, V3 and V4. Uniswap is off by default.

{% hint style="info" %}
On EVM, set your platforms deliberately. They keep the agent on the launchpads you actually want to copy. Cielo also drops spoofed Relay buys (fake buys made to look like they came from well-known wallets) before they reach your agents, feed or alerts.
{% endhint %}

## Buy

| Setting                                                   | What it does                                                                                                                                                                                                                                                   |
| --------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Allow buys**                                            | Turn off to run the agent in sell-only mode: it manages and exits positions but opens no new ones.                                                                                                                                                             |
| **Wallet**                                                | The trading wallet the agent spends from.                                                                                                                                                                                                                      |
| **Amount per buy**                                        | **Constant** spends the same amount every time. **Scaling** sizes your buy as a % of the copied wallet's buy, between a minimum and a maximum you set. Buys that would size below the minimum are skipped; larger ones are capped at the maximum.              |
| **Copied wallet's buy size filter**                       | Only copy a buy when the copied wallet spent within this range. It filters their buy size, not yours. Useful for ignoring a whale's dust buys or an occasional oversized ape.                                                                                  |
| **Entry**                                                 | **Instant** copies the buy straight away. **Buy the dip** waits for the price to drop by a % inside a time window, and can split the entry into several orders. Queued dip buys show in the agent, where you can **Skip**, **Buy now** or **Cancel** the rest. |
| **Execution**                                             | How your trades are sent. See [Execution](agent-settings.md#execution) below.                                                                                                                                                                                  |
| **Only copy new positions**                               | Only copy a buy when the wallet is opening a new position (its balance of that token was zero). Filters out averaging-down buys.                                                                                                                               |
| **Snipe token launches** _(Solana)_                       | When a wallet you copy launches a token on a launchpad like Pump.fun, buy it straight away.                                                                                                                                                                    |
| **Buy limits**                                            | Cap how often the agent buys, per hour or per day. Unlimited by default. Individual wallets can have their own limits.                                                                                                                                         |
| **Cross-copied-wallet trade prevention**                  | Only the copied wallet that opened a position can make the agent buy more or sell it, until the position is closed. Stops two copied wallets from doubling you into the same token.                                                                            |
| **Ultra-fast FOMO & Pump.fun copy trading** _(Robinhood)_ | Copies trades made in the Fomo and Pump.fun apps at ultra-fast speed. While it's on, every other swap is ignored.                                                                                                                                              |

### Execution

| Setting                   | What it does                                                                                                                                                                                                                                                                                                 |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Speed** _(Solana)_      | The priority fee each trade pays. **Standard** (about 0.002 SOL) is fast in normal conditions. **Turbo** (about 0.008 SOL) stays fast when the network is busy. **Godly** (about 0.06 SOL) is for winning races on heavily copied wallets. **Custom** lets you set the fee and tip yourself. Default: Turbo. |
| **Gas** _(EVM)_           | **Auto** sets gas for you. You can also set your own gas and priority tip, separately for buys and sells. On Robinhood, higher gas doesn't make trades land faster, so leave it on **Auto**.                                                                                                                 |
| **MEV protection**        | Protects your trades from sandwich bots. On Solana, **Fastest** sends straight to the block leader, **Balanced** only sends to leaders with no history of sandwiching, and **Protected** goes only through Jito (default: Balanced). On EVM, **Secure** is on by default.                                    |
| **Slippage**              | The most the price can move before the trade is rejected. Default 30%. Raise it for new bonding-curve tokens and heavily copied wallets; keep it tighter elsewhere.                                                                                                                                          |
| **Degen mode** _(Solana)_ | Turns off the engine's price safety checks, so trades go through even at entries it would normally refuse. Leave it off unless you know exactly why you need it.                                                                                                                                             |

## Sell

Exit rules can be combined. Each sell % applies to the size of the original position, and tiers together can sell up to 100%.

| Setting                                      | What it does                                                                                                                                                                                                                                                                                                       |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Individual TP/SL per buy**                 | Treats each buy of the same token as its own entry. Take profit, stop loss, trailing stop, time limit and break even are measured from that buy's price and only sell that buy's amount. Example: you buy at $1.00, $0.80 and $0.60 with a 20% take profit. Each entry sells on its own at $1.20, $0.96 and $0.72. |
| **Sell when copied wallet sells**            | Sell when the wallet you copy sells, either the whole position or the same proportion they sold.                                                                                                                                                                                                                   |
| **Sell when copied wallet transfers tokens** | Sell when the wallet you copy sends the token to another wallet.                                                                                                                                                                                                                                                   |
| **Stop loss**                                | Sells part of the position at each loss tier. Default: at -30%, sell 100%.                                                                                                                                                                                                                                         |
| **Take profit**                              | Sells part of the position at each profit tier. Default: at +50%, sell 100%. Add tiers to ladder out.                                                                                                                                                                                                              |
| **Trailing Stop**                            | Follows the price up and sells the whole position when it drops a set % from its peak. It only starts once the position is up your activation %. Set activation to 0 to trail from entry.                                                                                                                          |
| **Time Limit**                               | Sells after a set time, whatever the price. On Solana you can set seconds, hours or days and add tiers, like 50% after 6 hours and the rest after 24. On EVM it's in hours.                                                                                                                                        |
| **Break Even**                               | Once the position is up your activation %, sells everything if the price falls back to your entry (or to an exit level you set just above it). It helps stop a winning trade from turning into a loss, though the sell fills at market and can land slightly below your entry.                                     |
| **Break Even from Loss**                     | Once the position is down your activation %, sells everything if the price recovers to your exit level: your entry, a smaller loss or a small win. Add a time limit, counted from activation, to sell anyway if it hasn't recovered by then.                                                                       |

{% hint style="info" %}
"Sell when copied wallet sells" applies to the whole position even when **Individual TP/SL per buy** is on.
{% endhint %}

{% embed url="https://x.com/CieloFinance/status/2085339713817251998" %}

{% embed url="https://x.com/CieloFinance/status/2100560991117357419" %}

{% embed url="https://x.com/CieloFinance/status/2105250356116554112" %}
