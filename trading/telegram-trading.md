# Telegram Trading

Cielo's Telegram bot includes native trading functionality, allowing you to buy and sell Solana tokens directly from your alerts.

When Telegram Trading is enabled, every swap alert in your bot will include **Quick Buy buttons** at the bottom of the message, letting you act on a trade the moment you spot it.

#### Enabling Telegram Trading

To get started, your Solana trading wallet must be funded with SOL. You can view your trading wallet address and balance at any time by sending `/start` to your Cielo bot. The home screen shows:

* Your current plan and wallet counts
* Your active Solana trading wallet address and balance
* Navigation buttons for Positions, PnL, Trading Wallets, Settings, and more



***

#### Quick Buying from Alerts

When a tracked wallet makes a swap on Solana, your alert will display three **Quick Buy buttons** beneath the transaction — for example:

> 🟢 **0.1 SOL**   🟢 **0.5 SOL**   🟢 **1 SOL**

Tap any button to instantly buy that token using the selected SOL amount from your default trading wallet. Once executed, you'll receive a transaction receipt with a link to view it onchain.

You can customise these preset amounts at any time in **Trading Settings → Buy Presets**.

***

#### Trading a Specific Token

You can also open a token's buy/sell panel at any time by pasting a Solana token address directly into the Telegram chat. The bot will display:

* Token name, symbol, and mint address
* Market cap, price, and liquidity
* Your current position and PnL for that token (if you hold it)

From here you can buy using preset amounts or a custom SOL value, and sell in preset percentages (25%, 50%, 100%) or a custom amount.

***

#### Positions

Tap **📊 Positions** from the bot home menu (or send `/positions`) to see all your currently open Solana positions across your trading wallets, including each token's unrealised PnL in both SOL and USD.

Tap any token in the list to open its buy/sell panel directly.

***

#### PnL Dashboard

Tap **📈 PnL** (or send `/pnl`) to view your trading performance for the last 1D, 7D, 30D, or all time. The dashboard shows:

* Realised and unrealised PnL in USD and SOL
* Total portfolio value
* Tokens traded, total transactions, buys vs sells, and win rate
* Token performance distribution (e.g. how many of your trades returned >500%, 200–500%, etc.)

***

#### Trading Wallets

Tap **💼 Trading Wallets** to manage the Solana wallets used for trading. From here you can:

* View all wallets and their SOL balances
* Create a new trading wallet
* Set a default wallet
* Rename, archive, or withdraw funds from any wallet

***

#### Trading Settings

Tap **⚙️ Settings → Trading Settings** to configure your trading behaviour:

**Transaction Settings** Configure separately for buys and sells:

* **Slippage**: The maximum price movement you'll accept on a trade
* **Priority Fee**: Increase to get your transaction confirmed faster during congestion
* **MEV Protection**: Protects your trade from sandwich attacks (Disabled / Reduced / Secure)
* **Auto Fee**: Automatically selects an optimal priority fee, with an optional SOL cap

**Buy Presets** The three SOL amounts shown as Quick Buy buttons in alerts. Defaults are 0.1, 0.5, and 1 SOL. Tap any preset to change it.

**Sell Presets** The three percentage amounts shown when selling a token. Defaults are 25%, 50%, and 100%.

***

> 💡 Telegram trading uses the same execution engine as the Cielo web app — your positions, wallets, and PnL are shared across both.
