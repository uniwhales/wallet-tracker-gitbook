# Renames

Renames let you label any wallet address with a custom name and emoji without adding it to your tracked wallets. Think of it as a personal wallet address book.

There are many addresses you may want to recognize but don't need alerts for: CEX wallets, deployers, smart contracts, LP addresses, or high-volume wallets that can't be tracked. Renames gives you a way to label these wallets so you can identify them wherever they appear across Cielo.

#### Renaming a Wallet

You can rename a wallet from multiple places in the app:

* **Trades table** on the Trading Terminal: click a wallet address and select "Rename wallet"
* **Holders tab**: click a holder address and select "Rename wallet"
* **Top Traders tab**: click a trader address and select "Rename wallet"
* **Wallet profile page**: click the edit icon next to the wallet address
* **Renames tab** on the Tracking page: click the edit icon on any existing rename

When you rename a wallet, a modal will appear where you can:

* Select an **emoji** to visually identify the wallet (optional)
* Enter a **label** of up to 50 characters
* Click **Save**

Renaming a wallet does not add it to tracking. If you also want to track the wallet and receive alerts, use the separate "Add to Tracking" option.

#### Where Renamed Labels Appear

Once you rename a wallet, the custom label and emoji replace the raw address everywhere that wallet appears in Cielo:

* Trades table (Trading Terminal)
* Holders tab
* Top Traders tab
* Feed cards
* Wallet profile pages

This works across all chains.

#### Renames Tab

The **Renames** tab on the Tracking page is where you manage all your labeled wallets. The table displays:

| Column             | Description                                                                 |
| ------------------ | --------------------------------------------------------------------------- |
| **Wallet**         | Emoji + custom label + truncated address. Click to open the wallet profile. |
| **Rename Time**    | When the label was first set.                                               |
| **Native Balance** | SOL, ETH, BTC, or SUI balance depending on the chain.                       |
| **Total Profit**   | All-time PnL in USD and percentage.                                         |
| **TXs**            | Total transaction count.                                                    |
| **Last Active**    | Time since the wallet's last onchain activity.                              |

All columns are sortable. By default, the table sorts by newest rename first.

**Actions available on each wallet:**

* **Add to Tracking**: promotes the wallet to full tracked status with alerts and filters
* **Copy address**
* **Delete**: removes the rename (does not affect tracking if the wallet is also tracked)

**Top bar actions:**

* **Search**: filter by name or address
* **Delete selected**: select multiple renames and delete them
* **Remove All**: clear all renames (requires confirmation)

#### Renames vs. Tracked Wallets

Renames and tracked wallets are independent. You can rename a wallet without tracking it, track a wallet without renaming it, or do both.

|                              | Renamed wallet | Tracked wallet |
| ---------------------------- | -------------- | -------------- |
| Custom label + emoji         | Yes            | Yes            |
| Alerts and notifications     | No             | Yes            |
| Filter settings              | No             | Yes            |
| Appears in Feed              | No             | Yes            |
| Counts toward tracking limit | No             | Yes            |
| Label visible across app     | Yes            | Yes            |

If you rename a wallet and later add it to tracking, the label persists. If you remove it from tracking, the rename still exists in your Renames library.

#### Limits

You can rename up to **1,000** wallets per account. Renames do not count toward your tracked wallet limit.
