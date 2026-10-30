---
description: >-
  Buy and sell on Solana, Ethereum, Base, Robinhood and Arc from the Cielo
  terminal.
---

# Overview

You can trade any token you find on Cielo without leaving the app. The wallet data that tells you a token is worth a look sits next to the buy button, so you don't lose the moment copying an address into another bot.

Trading works on **Solana, Ethereum, Base, Robinhood and Arc**, in the web app and in [Telegram](telegram-trading.md). Fund your [trading wallet](portfolio.md#wallets) first by clicking **Deposit** in the top right, and keep a little SOL (Solana) or ETH (Ethereum, Base, Robinhood) for network fees, even if you trade with USDC or USDG.

Ethereum has the full terminal with market orders and Advanced Trading Strategy, plus Trending and Telegram trading. Limit and stop orders, Pulse and trading agents aren't on Ethereum yet.

{% embed url="https://x.com/CieloFinance/status/2116157268064681998" %}

## Where you can buy

* **Quick buy buttons** on [Trending](../trending/), [Pulse](pulse.md), both Feed views and Telegram alerts buy in one click at the amount you've set.
* **Clipboard quick buy**: copy a Solana or Base token address anywhere and a quick buy pill shows up in the navbar. Turn it on in **Settings > Advanced > Clipboard token detection**.
* **The terminal**: click any token name to open its full page, with the chart, the order panel and every wallet trading it.

Set your quick buy amount and currency in the bar at the top of the Feed and Trending, and at the top of each Pulse column.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FmBS6adFr5QV4Eh5yTkfD%2Fimage.png?alt=media&#x26;token=702eadeb-ef85-44b2-826d-702c95022a42" alt=""><figcaption></figcaption></figure>

## The terminal

The token page has the chart in the middle, the order panel on the right, and tables underneath.

### Order panel

Switch between **Buy** and **Sell**, then pick an order type:

| Order type | What it does                                                                                                                                                                               |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Market** | Fills now at the best available price.                                                                                                                                                     |
| **Limit**  | Fills when the price (or market cap) reaches your target. Use it to buy a dip or sell into strength without watching the chart. You can set an expiry so an unfilled order cancels itself. |
| **Stop**   | Sells when the price falls to your level, to cap a loss.                                                                                                                                   |

**P1**, **P2** and **P3** are your execution presets. Each one stores slippage, priority fee and MEV protection, so you can keep a fast preset for launches and a cheaper one for everything else.

**Advanced Trading Strategy** attaches take profit and stop loss levels to a buy before you place it. Add several levels, each with its own sell %. When the buy fills, the exit plan is live straight away.

{% embed url="https://x.com/CieloFinance/status/2094434783426118055" %}

### Token checklist

Under the order panel, the token checklist gives you a quick risk read before you buy:

| Check               | What it tells you                                                         |
| ------------------- | ------------------------------------------------------------------------- |
| **Top 20 Holders**  | Share of supply held by the 20 largest holders.                           |
| **Dump Risk**       | Estimated price drop if the largest holder sold everything.               |
| **Top 5 Dump Risk** | Estimated price drop if the five largest holders sold.                    |
| **Dev**             | Share of supply the deployer still holds.                                 |
| **Snipers**         | Share held by wallets that bought in the first blocks.                    |
| **Bundlers**        | Share bought in bundled transactions at launch.                           |
| **Holders**         | Number of holders.                                                        |
| **Dev Tokens**      | How many tokens this deployer has launched before, and how many migrated. |
| **Dex Paid**        | Whether the token paid for its DexScreener profile.                       |

A high Dump Risk doesn't mean the holders will sell. It tells you how thin the book is under them if they do.

{% embed url="https://x.com/CieloFinance/status/2112975000240042251" %}

### Tables under the chart

| Tab                         | What's in it                                                                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Trades**                  | Every trade on the token. Filter to **My Trades**, **KOL**, **Tracked**, **Renames**, **Dev**, **Whale**, **Fresh** or **Snipers**.                                |
| **Orders**                  | Your open limit and stop orders.                                                                                                                                   |
| **Positions** / **History** | Your open and closed positions on this token.                                                                                                                      |
| **Holders**                 | Top holders, with your [renames](../wallet-tracking/my-wallets/renames.md) shown in place of addresses.                                                            |
| **Top Traders**             | The most profitable wallets on this token. Sort by PnL, ROI, volume and more. Once you've bought the token, turn on **First Buyers** to see who got in before you. |
| **Dev Tokens**              | Other tokens launched by the same deployer.                                                                                                                        |

Click any wallet in these tables to rename it, track it or open its profile.

### Callouts

Callouts from fomo, Pump.fun and GMGN show up on the chart, each one on the candle where the trader called the token. On fomo these are a trader's thesis, on Pump.fun their callouts.

Hover a caller's avatar to see who they are and where they posted, what they said, the market cap at the call and how far the token has moved since, and whether they still hold it, with their PnL.

Open **Callouts** next to the trades table to see every call on the token in one list. You can follow a caller from there, show only the callers you follow, or block a caller.

### Display options

**Display Options** on the chart controls what's drawn on it. Pick which markers to show (FOMO Thesis, Pump Callouts, GMGN Callouts, KOL, Dev, Snipers, Tracked wallets and more) and turn on lines such as your average buy, agent entries, TP/SL levels and the all-time high.

{% embed url="https://x.com/CieloFinance/status/2115441683861032999" %}

## Dynamic panels

The footer launcher opens Feed, Trending, Pulse, Tracking, Agents, Positions and PnL as floating panels. Drag them anywhere, snap them side by side, and they stay open as you move between pages. Save a layout as a **Preset** to bring it back in one click.

{% embed url="https://x.com/CieloFinance/status/2088314036458787147" %}

The **Agents** panel shows your [trading agents](../trading-agents/overview.md) inside the terminal: turn an agent on or off, see its buys and sells on the chart, and sell part of a position yourself while the agent manages the rest.

{% embed url="https://x.com/CieloFinance/status/2108527912311722448" %}

## Speed

Solana trades go through Cielo's own router, built to find the fastest path to the best price. It makes Solana copy trades faster too.

{% embed url="https://x.com/CieloFinance/status/2111171937468854327" %}

## Fees

| Trade type                           | Fee  |
| ------------------------------------ | ---- |
| Manual trades (web app and Telegram) | 0.6% |
| Trading agent trades                 | 1%   |

Network fees, priority fees and tips go to the network, not to Cielo. Part of the fees from users you refer can come back to you through [Referrals](referrals.md).

## Fear & Greed Index

The Onchain Fear & Greed Index is one number from 0 to 100 showing how hot the launch market is right now, based on real swaps. It covers Solana launchpads (Pump.fun, LetsBonk and StonkFun) and Robinhood Chain. You'll find it in the footer of every page. Click it for the full page, with tokens launched, how many ran past $50K, $500K and $1M, and the top runners.

{% embed url="https://x.com/CieloFinance/status/2078042022955360549" %}

{% embed url="https://x.com/CieloFinance/status/2110780122446057857" %}
