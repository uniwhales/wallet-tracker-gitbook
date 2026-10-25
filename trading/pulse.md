---
description: >-
  New tokens from supported launchpads on Solana, Base, Robinhood and Arc, from
  launch to migration.
---

# Pulse

[Pulse](https://app.cielo.finance/pulse) streams new tokens the moment they launch on a launchpad and follows them until they migrate to a full DEX pool. Use it when you want to be early: you see a token minutes after it exists, with the holder and dev data you need to decide whether it's worth a buy.

Pulse covers Solana, Base, Robinhood and Arc. Pick **ALL** at the top of the page or narrow it to one chain with **SOL**, **BASE**, **HOOD** or **ARC**.

## The three columns

| Column              | What it shows                                                             |
| ------------------- | ------------------------------------------------------------------------- |
| **New Pairs**       | Tokens that just launched and are still early on their bonding curve.     |
| **Almost Migrated** | Tokens close to completing their bonding curve.                           |
| **Migrated**        | Tokens that finished the curve and moved to a DEX pool, such as PumpSwap. |

Each token card shows the ticker, age, volume (**V**), market cap (**MC**), fees paid (**F**), transaction count (**TX**) and holder count. The crown counter shows how many of the dev's previous tokens migrated (for example **1/3**). Hover the logo to see how far along the bonding curve the token is.

The row of percentages along the bottom is a quick audit:

| Pill               | What it shows                                          |
| ------------------ | ------------------------------------------------------ |
| **Top 20 Holders** | Share of supply held by the 20 largest holders.        |
| **Dev Holding**    | Share the deployer still holds.                        |
| **Snipers**        | Share held by wallets that bought in the first blocks. |
| **Bundlers**       | Share bought in bundled transactions.                  |
| **Paid**           | The token paid for its DexScreener profile.            |

## Filters and trading presets

Every column has its own filter button, so you can set New Pairs to be loose and Migrated to be strict. Filters cover things like market cap, volume, holders, token age, launchpad and audit thresholds.

Filters apply to every chain at once, so a minimum of 2 means 2 SOL on Solana and 2 ETH on Base. If you need different values per chain, view one chain at a time. If a launchpad's tokens are missing, check it's ticked in the launchpad filter.

**P1**, **P2** and **P3** above each column are your trading presets. Hover one to see what it holds: slippage, priority fee and MEV protection. The quick buy on that column uses the preset you pick, so you can keep a fast preset for New Pairs and a cheaper one for Migrated.

## Quick buy

The amount on each card (for example **⚡ 0.05 SOL**) is a one-click buy. Set the amount and the currency at the top of each column. On Robinhood you can quick buy with ETH or USDG, on Arc with USDC.

Click anywhere else on the card to open the token in the trading terminal, where you get the full chart, the [token checklist](overview.md#token-checklist) and limit orders.

## Display and Moderation

**Display** controls what each card shows, so you can hide metrics you don't use and keep the columns compact.

**Moderation** keeps junk out of your view. Hover a token's logo and click the eye icon to hide it, or the block icon to block its dev so nothing they launch shows up again. The **Moderation** panel lists your **Hidden Tokens** and **Blocked Devs**, and you can undo either from there.

{% embed url="https://x.com/CieloFinance/status/2047748341744767118" %}
