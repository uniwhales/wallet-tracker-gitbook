# Telegram

1. [**Bypassing the Cielo web app**](getting-started.md#bypassing-the-cielo-web-app)
2. [**Adding a wallet**](getting-started.md#adding-a-wallet)
3. [**Adding a token**](getting-started.md#adding-a-token)
4. [**Editing wallets + tokens**](getting-started.md#editing-wallets--tokens)
5. [**Alert settings**](getting-started.md#alert-settings)
6. [**Viewing contract address**](getting-started.md#viewing-contract-address)
7. [**Telegram trading**](getting-started.md#telegram-trading)

Cielo provides free users with one Telegram bot. Any wallets or tokens you enable alerts for will automatically be assigned to this bot. However, Pro + Whale members can access **two** and **nine** bots respectively, plus two and nine [private bots](telegram-private-bot.md).

This allows you to map specific tx types to a specific bot. For instance, you could use one bot for your own wallets, another for NFT traders, and another for DEX whales.

To activate your Telegram bots, in the Cielo web app visit [Alerts](https://app.cielo.finance/settings/alerts).

To change which bot a wallet is assigned to, in **Tracking**, click the edit icon alongside the wallet name. In the popup that appears, click the dropdown titled **Receive Alerts On**. Pick a desired bot and then hit **Save changes**.

## Bypassing the Cielo web app

It's possible to use Cielo as a standalone Telegram bot, without pairing it to the Cielo web app.

However it's recommended that you use the bot in conjunction with the Cielo [web app](https://app.cielo.finance). The app is free to use and its interface makes it easier to adjust wallet settings than doing so within Telegram. If you'd rather just use the Telegram bot on its own, however, read on.

To initialize the [Cielo Wallet Tracker bot](https://t.me/evmtrackerbot), open it in Telegram and press the blue **Start** button.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FnffUNLOj1OCH1hSu4TY6%2FScreenshot%202024-09-12%20at%2014.36.28.png?alt=media&#x26;token=bf8b2333-2234-46e0-958f-cce1368aca30" alt=""><figcaption></figcaption></figure>

Press the blue menu icon to view wallet settings:

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FhyFhsvkIjj9pKuRiaPzq%2FScreenshot%202023-06-18%20at%2019.14.12.png?alt=media&#x26;token=40792464-bfd4-403c-86a6-c438ffab32aa" alt="" width="261"><figcaption></figcaption></figure>

The following options are displayed:

* **Add wallet or token**: Input the address and label for a wallet you wish to track or the smart contract address for a token.
* **List**: View all of the wallets that you're currently tracking. You can then click on the edit option beside each wallet to adjust its settings.
* **Menu**: View master menu that includes options for setting group and channel alerts.
* **Bot settings**: Opens options to disable bot or reset chat.

You can also control the Telegram bot by entering the following commands:

<mark style="color:blue;">/start -</mark> Initialize the bot

<mark style="color:blue;">/add\_wallet\_or\_token</mark> - Add new wallet or token

<mark style="color:blue;">/list</mark> - Get the list of all tracked wallets / tokens

<mark style="color:blue;">/bots</mark> - View available reserve bots

<mark style="color:blue;">/pnl</mark> - Get your trading PnL

<mark style="color:blue;">/menu</mark> - Open the menu

<mark style="color:blue;">/add \[wallet] \[label]</mark> - Add a new wallet. You can specify multiple wallets separated by comma (e.g. /add WALLET\_ADDRESS\_1 LABEL\_1, WALLET\_ADDRESS\_2 LABEL\_2)

<mark style="color:blue;">/add\_token \[chain\_name] \[token\_address] \[min\_amount\_usd]</mark> - Add a new token

<mark style="color:blue;">/bot\_settings</mark> - Open bot settings

<mark style="color:blue;">/delete \[wallet</mark>] - Delete wallet. You can specify multiple wallets separated by comma (e.g. /delete WALLET\_ADDRESS\_1, WALLET\_ADDRESS\_2)

<mark style="color:blue;">/help</mark> - View a list of all supported commands

### Adding a wallet

To add a wallet using the Telegram bot, click the blue menu icon followed by the top option that appears: **Add new wallet or token**.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2F8I11QwxrQGzaqdKdj2P3%2FScreenshot%202023-06-18%20at%2019.23.49.png?alt=media&#x26;token=ed9e75e1-6842-4113-ac41-8e8ab58e07b0" alt=""><figcaption></figcaption></figure>

Then click the **Wallet** button and paste in the wallet address followed by a space and then an optional name for the wallet e.g. _My Trading Wallet_. By default, all of the chains that Cielo tracks are enabled. If you wish to disable alerts for any of these chains, just click the relevant button to disable the selection.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FEDY01Abuz5catse373qE%2FScreenshot%202024-09-12%20at%2014.46.35.png?alt=media&#x26;token=f002e62c-9c67-4163-9b01-8647ada9cadf" alt=""><figcaption></figcaption></figure>

When you're done, click **Confirm**. You'll then see the following screen for controlling tx types:

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2F4diicxFL9PsPQdELeDL2%2FScreenshot%202023-06-18%20at%2019.27.13.png?alt=media&#x26;token=a1bc39ae-5be3-429c-8f07-a706b9e907cd" alt=""><figcaption></figcaption></figure>

Click on a tx type you wish to disable and then hit **Confirm**. You will now see the following notification:

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FTlTjz3sRbxX3V7SnKArn%2FScreenshot%202023-06-18%20at%2019.29.03.png?alt=media&#x26;token=b5992dc1-227d-4960-928f-9371d01bd05e" alt=""><figcaption></figcaption></figure>

And that's it: you're now tracking your first wallet using Cielo's Telegram bot.

### Adding a token

To start tracking a token, repeat the procedure described above but select the **Token** button. You will then see the following option:

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2F1an9MSp9zsj6iTikxot0%2FScreenshot%202024-09-12%20at%2014.49.54.png?alt=media&#x26;token=b6706df8-d1d5-4989-a2ab-ae55e3fabf8f" alt=""><figcaption></figcaption></figure>

Select your desired chain, enter the smart contract address for the token and hit return. You can find this in a block explorer or using a market data site such as [CoinGecko](https://www.coingecko.com/).

You will now be asked to set a DEX swap threshold. This is to prevent you from being overwhelmed with alerts for popular tokens.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2F743816G9g2TyZhTWo29d%2FScreenshot%202023-06-18%20at%2019.34.37.png?alt=media&#x26;token=2f03db58-8dd1-4b72-a458-4a54838e75b2" alt=""><figcaption></figcaption></figure>

Enter a value (denominated in USD) and press return or hit **Skip** if you wish to receive alerts for all swaps, regardless of size. You will now see the following notification:

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FeCTnHoSjHvAs3VlRBBRr%2FScreenshot%202023-06-18%20at%2019.36.13.png?alt=media&#x26;token=9b50c356-6857-4253-bec9-4a171fb41c9b" alt=""><figcaption></figcaption></figure>

### Editing wallets + tokens

To edit a wallet or token you're tracking, click the blue menu icon followed by the _/list_ option. This will produce a list of all wallets you're following.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2F6qrHnNn82NE87X0dU9p1%2FScreenshot%202023-06-18%20at%2019.47.25.png?alt=media&#x26;token=a00f1ca7-01f4-40ed-a307-8e53c0374e1a" alt=""><figcaption><p>In this example, the ARB token is being tracked.</p></figcaption></figure>

Click the blue edit link beneath the address to make an edit to the wallet or token. In addition to adjusting which chains and tx types are enabled (wallet) and the minimum tx size (tokens), you can disable alerts or delete the address altogether.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FbVwOaXwX8Dl50qwvzUp4%2FScreenshot%202023-06-18%20at%2019.49.33.png?alt=media&#x26;token=a933f627-873b-4f86-af12-0d7e09ea8009" alt=""><figcaption></figcaption></figure>

To re-enable alerts for a particular address, just repeat the process above and click the **Enable** button when prompted.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FYh5xPn9L7Ho3XdiRbbz1%2FScreenshot%202023-06-18%20at%2019.50.39.png?alt=media&#x26;token=4980d2c3-0af6-4e54-ae20-dc5d758790b3" alt=""><figcaption></figcaption></figure>

### Alert settings

Pro and Whale users can opt to have market cap and liquidity information displayed in bot alerts for token swaps. To enable this, in the web app check the **Display Market Cap and Liquidity** button in [Settings > Advanced](https://app.cielo.finance/settings/advanced).

By default, Cielo Wallet Tracker alerts include a **Chart** link, where applicable.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FQyONrvWmsPpVSINGLU2w%2FScreenshot%202023-06-19%20at%2014.47.30.png?alt=media&#x26;token=773ae5cf-9fce-4164-ba38-3d95664c69a8" alt=""><figcaption></figcaption></figure>

Cielo allows you to choose which trading terminal you would like the **Chart** link to direct to. To adjust this setting, click the blue menu icon in the Cielo Wallet Tracker to pull up the main menu and then select **Alert Settings** followed by **Chart**.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FzXv1rKZ6SZ8pPuA0bKso%2FScreenshot%202023-06-19%20at%2014.50.02.png?alt=media&#x26;token=fbd1e538-48de-48fb-a7c0-db8a385ec7b6" alt=""><figcaption></figcaption></figure>

Then choose which of the four available terminals you would like to use for charting and hit **Confirm**.

### Viewing contract address

\
To trade a token that is displayed in the Cielo web app or Telegram bot, the contract address is required. Upon pasting this into a DEX such as Uniswap or an aggregator like Dexscreener, you can trade the token in question. There are a number of ways to obtain the contract address:<br>

1\. Click the **ViewTx** link to inspect the transaction in a block explorer.

2\. Click **Chart** to view the tx in a platform such as Gecko Terminal.

3\. Enable one-click contract address copy within Telegram.

To enable the latter option when using the Cielo Telegram bot, select **Menu** > **Alert Settings** > **Show Token Address**. When activated, this displays the contract address with each tx alert, allowing you to trade tokens faster and on the platform of your choosing.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FO5DTrVauzAoa3l977XtD%2FScreenshot%202023-08-28%20at%2011.52.29.png?alt=media&#x26;token=1b419205-a57d-48e7-85bf-ba78c4c49a62" alt=""><figcaption><p>The contract address is shown in red.</p></figcaption></figure>

### Telegram trading

Swap alerts include Quick Buy buttons, so you can trade directly from your Cielo Telegram bot. See [Telegram Trading](https://docs.cielo.finance/trading/telegram-trading).

{% hint style="info" %}
_**Disclaimer**: Trading tokens, particularly new memecoins, is risky as there is a high chance of financial loss. It is the responsibility of each user to research any asset they wish to purchase and to acknowledge the risks inherent to Telegram trading._

_tl;dr DYOR._
{% endhint %}
