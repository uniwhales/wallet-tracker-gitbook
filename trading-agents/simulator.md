---
description: Test a copy trading setup on real past trades before you risk any money.
---

# Simulator and Ask AI

Before an agent trades for real, you can see how your exact settings would have done on the copied wallets' actual trades. It's the fastest way to catch a setup that looks good on paper but loses money, for example a stop loss that's too tight for how a wallet trades.

The simulator is in the panel on the right when you create or edit a trading agent (**Agents > New Trading Agent**, or **Edit** on an existing agent). It starts as soon as you've added a wallet and an amount per buy.

## The simulator

It replays your agent's settings, including wallets, buy size, filters and exit rules, on the wallets' real trades over the last **1D**, **3D** or **7D**. You get:

* Simulated PnL, win rate, number of trades, tokens traded and median hold time
* Results net of Cielo's fees
* A fill-by-fill breakdown of every simulated trade

Two settings control how fills are priced:

| Mode                  | How it prices your fills                                                                                                                  |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Precise fills**     | Prices fills with 1-second price data. On by default.                                                                                     |
| **Worst-price fills** | Fills each trade at the worst price in the second or so after it: the high for buys, the low for sells. Use it for a pessimistic version. |

**Starting loss per buy** lets you add an assumed entry loss to every buy, to account for slippage and for being behind the wallet you copy.

## Ask AI

**Ask AI** searches for the settings your agent's wallets responded best to over the selected window. It tries combinations of stop loss, take profit tiers, buy limits, Buy the dip versus Instant entries, and market cap and token age filters.

It comes back with two options:

* **Recommended**: a balanced setup
* **Max profit**: the setup that made the most in the window

Click **Apply to agent** and the settings are written into your agent. Change anything you like before you save.

Not every wallet has a profitable setup. If Ask AI can't find one, it says so, which usually means the wallet isn't worth copying with these filters.

{% hint style="warning" %}
Simulated results are hypothetical. They use real trades, but they can't account for everything that happens live, such as other copiers buying ahead of you. Past performance doesn't guarantee future results.
{% endhint %}

{% embed url="https://x.com/CieloFinance/status/2102773542555189278" %}

{% embed url="https://x.com/CieloFinance/status/2091943796053319798" %}
