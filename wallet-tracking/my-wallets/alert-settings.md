---
description: Choose which of a wallet's transactions reach your Telegram and Discord.
---

# Alert settings

Your Feed always shows everything your wallets do. Alert settings decide which of those transactions are also sent to your Telegram bots and Discord channels, so your phone only buzzes for trades you'd act on.

Open them from **Tracking**: click the edit icon next to a wallet, or select several wallets and click **Alert Settings** in the bar at the bottom.

## What you can set

| Setting                                                    | What it does                                                                                                                                                 |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Receive Alerts On**                                      | Which Telegram bot or Discord channel gets this wallet's alerts. A newly activated bot starts with no wallets, so pick it here for each wallet (or in bulk). |
| **In-App Trade Notifications**                             | Show a pop-up and play a sound anywhere in the app when this wallet buys or sells.                                                                           |
| **Chains**                                                 | Only alert on the chains you pick.                                                                                                                           |
| **Transaction types**                                      | Swaps, transfers, NFT trades, perps, approvals and so on. Turning off approvals and keeping swaps and transfers removes a lot of noise.                      |
| **Minimum USD**                                            | Skip transactions below this value.                                                                                                                          |
| [**New Trade Alerts**](new-trade-alerts.md) _(Pro, Whale)_ | Only alert the first time the wallet trades a token. Turn on **First Sell Alerts** in **Settings > Advanced** to also get the first sell.                    |
| [**Token Filters**](token-filters.md) _(Pro, Whale)_       | Only alert when the wallet trades specific tokens. Add up to 10 token addresses per wallet.                                                                  |

When Cielo adds a new chain, it's only switched on for wallets set to track all chains. For the rest, tick it in their alert settings (bulk edit works).

To silence a token or contract for all your wallets at once, use [Exclusions](exclusions.md) instead.

## Alert profiles

**Alert Profile**, at the top of a wallet's alert settings, lets you apply a saved set of alert settings in one click instead of setting chains, types and minimums every time. Pick **Custom** to set them by hand.

## What alerts can show

These toggles are in **Settings > Advanced** and apply to all your alerts:

* **Display Token Address in Alerts**: the token contract, ready to copy
* **Display PnL in Alerts**: the wallet's PnL on the token in sell alerts
* **Display % Sold in Sell Alerts**: whether the wallet trimmed or sold its whole bag
* **Display Remaining Holdings in Alerts**: how much the wallet still holds, in USD and % of supply
* **Highlight Swaps**: a 🟢 or 🔴 emoji on buys and sells
* **X Search**: a link that searches the token address on X

{% embed url="https://x.com/CieloFinance/status/2065108643033366780" %}

## Getting too many alerts?

Telegram limits how fast any bot can send messages. If you track a lot of busy wallets, a burst of alerts can get delayed. You can help:

* Set a minimum USD value
* Turn off transaction types you don't need, approvals especially
* Split busy lists across several bots, including [private bots](../../discord-+-telegram-bots/telegram-private-bot.md)
* Use [Bulk edits](bulk-edits.md) to apply all of this in one go

The web app Feed has no rate limit.
