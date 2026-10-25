---
description: >-
  Buy, sell and copy trade from Telegram, with the same wallets and positions as
  the web app.
---

# Telegram trading

The Cielo Telegram bot you get alerts from is also a trading bot. When a tracked wallet buys something, the alert has buy buttons right under it, so you can act from your phone in one tap. Trades run on Solana, Base, Robinhood and Arc, through the same engine and wallets as the web app. A position you open in Telegram shows up in the web terminal and the other way round.

## Get started

1. Activate a bot in **Settings >** [**Alerts**](https://app.cielo.finance/settings/alerts) if you haven't already. See [Telegram bot](../discord-+-telegram-bots/getting-started.md).
2. Fund your trading wallet: SOL or USDC on Solana, ETH or USDC on Base, ETH or USDG on Robinhood, USDC on Arc. Keep a little SOL or ETH for network fees, even if you trade with USDC or USDG.
3. Send `/start` to the bot. The home screen shows your plan, wallet counts and the active trading wallet with its balance.

## Buy from an alert

Swap alerts come with quick buy buttons at the bottom, one for each of your preset amounts. Tap one to buy that token with that amount from your default trading wallet. You get a receipt with a link to the transaction once it lands.

Change the amounts in **Settings > Trading Settings > Buy Presets**.

## Trade any token

Paste a token address into the chat. The bot shows the token's name, market cap, price, liquidity and a risk scan, plus your position if you hold it. From there you can:

* Buy with a preset or a custom amount
* Sell 25%, 50%, 100% or a custom amount
* Place a **limit order** to buy or sell at a target price, with an optional expiry

## Positions and PnL

| Command      | What it does                                                                                                                          |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| `/positions` | Your open positions across all trading wallets, with unrealized PnL. Tap a token to trade it.                                         |
| `/pnl`       | Your PnL for 1D, 7D, 30D or all time: realized and unrealized, win rate, tokens traded and how your trades are distributed by return. |

## Trading wallets

Tap **Trading Wallets** to see every wallet and its balance, create a new one, set your default, rename, archive or withdraw.

## Trading settings

Open **Settings > Trading Settings** to set how your trades execute. Buys and sells are configured separately.

| Setting                  | What it does                                                          |
| ------------------------ | --------------------------------------------------------------------- |
| **Slippage**             | The most the price can move against you before the trade is rejected. |
| **Priority Fee**         | Pay more to land faster when the network is busy.                     |
| **Auto Fee**             | Picks a priority fee for you, with an optional cap.                   |
| **MEV Protection**       | Protects against sandwich attacks.                                    |
| **Buy Presets**          | The amounts on the quick buy buttons.                                 |
| **Buy Button on Alerts** | Turn the buy buttons on alerts on or off.                             |
| **Sell Presets**         | The percentages on the sell buttons. Defaults are 25%, 50% and 100%.  |

## Mini app

The Cielo Telegram mini app puts copy trading on your phone. Create a [trading agent](../trading-agents/overview.md), add wallets to copy, turn agents on or off and check their PnL, all without opening the web app.

{% embed url="https://x.com/CieloFinance/status/2113324515296264235" %}

## Fees

0.6% per manual trade and 1% per trading agent trade, the same as the web app.
