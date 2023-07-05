# Configure

The [configure](https://app.cielo.finance/configure) page is your mission control. It’s where you add wallets, set alert filters, configure Telegram notifications, and create lists. There’s a lot you can do in configure. Mastering the features contained within this page is the key to mastering Cielo.

### Getting started

If you're not following any wallets, your configure page will start out blank:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-10 at 10.45.59.png" alt=""><figcaption></figcaption></figure>

If you _are_ already following wallets or public lists, however, your configure page will look like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-10 at 10.46.51.png" alt=""><figcaption></figcaption></figure>

We'll explain how to edit wallets, lists, and Telegram bots shortly. But first, we'll demonstrate how to add a wallet address and assign it to a list.



### Adding wallets

We’re going to create an alert for the following address:

_0xAb5801a7D398351b8bE11C439e05C5B3259aeC9B_

This is one of Vitalik Buterin’s known public wallets and is labeled as such on [Etherscan](https://etherscan.io/address/0xab5801a7d398351b8be11c439e05c5b3259aec9b). Here’s how to add it to Cielo:

1. Click the blue button marked **Add wallets**.
2. Paste in the wallet address and assign an optional label. Here, we’ll call it VB.
3. Choose which list you wish to assign it to. If you have yet to create any lists, it will default to **All**.
4. Under **Alert Settings** are some optional controls. Assigning a bot ID will activate Telegram alerts for this wallet.
5. Click **Save changes**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-10 at 10.53.23.png" alt=""><figcaption></figcaption></figure>

💁‍♀️ And that’s it. You’re now following your first wallet in Cielo.

The wallet will now appear in configure:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-10 at 10.57.14.png" alt=""><figcaption></figcaption></figure>

Visit your Cielo [feed](https://app.cielo.finance/feed) and you’ll see recent tx involving this wallet:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-10 at 10.58.31.png" alt=""><figcaption></figcaption></figure>

Now let’s return to [configure](https://app.cielo.finance/configure) and add a second wallet. This time we’ll go with an ENS address. _99th.eth_ is an active NFT collector. There’s no need to add their wallet address: the ENS will suffice. We'll apply the wallet label _NFT Holder_.

Now, under **Alert Settings**, we'll add some Telegram bot filters. In the pop-up that appears you can set a minimum transaction value (in USD), deselect any chains you _don’t_ wish to receive alerts for, and do the same for transaction types you wish to screen under **Alert Filter**.

{% hint style="info" %}
**Note:** Alert Settings only apply filters to your Telegram bot(s). They do not affect tx as they appear in the Cielo web app. For example, if you limit your chain selection to _Avalanche_, your Telegram bot will only show tx that occur on Avalanche network – but the Cielo web app will continue to display tx for all EVM chains.
{% endhint %}

<figure><img src="../.gitbook/assets/Screenshot 2023-06-12 at 11.51.42.png" alt=""><figcaption><p>Using the settings shown here, the Telegram bot will only show alerts for tx involving NFTs.</p></figcaption></figure>

When you’ve finished adjusting **Alert Settings**, click **Save changes** and the wallet will appear in your list of addresses on the configure page.

### Bulk adding wallets

If you have multiple wallets to add, Cielo allows you to import these in bulk. There are two ways to do this:

1. Importing a CSV file.
2. Using Twitter Connect. **NOTE**: _Twitter Connect is temporarily unavailable_.

For the latter option, click the **Twitter Connect** button in the top right of the configure page. You will then be connected to the Twitter API which will import your Twitter contacts who have an ENS in their profile name or bio. Note that it can take over a minute for your Twitter contacts to be analyzed and imported.

Alternatively, you can bulk add up to 50 wallets by uploading a CSV. Click **Add Wallets** and then **Import CSV**.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-12 at 12.45.56.png" alt=""><figcaption></figcaption></figure>

Wallet addresses should be placed in column one of the file and an optional label for each one should go in column two.

After uploading the CSV, wait a few seconds and your imported addresses will appear in configure. They can then be added to a new or existing list if desired.

### Editing wallets

After manually adding wallets to Cielo or following one or more public lists, your configure page will look something like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-12 at 12.02.13 (1).png" alt=""><figcaption><p>The two wallets at the top of the page (NFT Collector + VB) were manually added. The remaining wallets have been imported by following a public list called <em>NewWhaleWallets</em>.</p></figcaption></figure>



From left to right, each wallet as it appears on the configure page can be read and interacted with as follows:

* **Select button**: Click the circular button on the left to select the wallet. Repeat this action to select multiple wallets.
* **Avatar**: Click the colored avatar to open a new Cielo page for the wallet in question. This will display all recent tx involving this wallet.
* **Wallet name**: Descriptive label applied when you added the wallet to Cielo or when the list creator added it e.g. _NFT Collector_.
* **Edit icon**: Clicking the icon to the right of the wallet name opens a popup where you can edit the wallet settings.
* **Address:** Displays abbreviated view of the wallet's address e.g. _0x01...795a_. Click the icon to the right of the wallet to copy the full address to your clipboard.
* **Last active**: Time elapsed since the wallet last made a transaction.
* **List name**: Name of the list the wallet is assigned to. If no list is selected, this will default to _All_.
* **Telegram alerts**: Denotes whether Telegram bot alerts are on/off for the wallet.

Clicking the select iconn to the left of a wallet produces the following options:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-12 at 14.33.59.png" alt=""><figcaption></figcaption></figure>

* **Unfollow**: Deletes this wallet from the Cielo web app and bot.
* **Remove from list**: Removes this wallet from the list it is assigned to but does _not_ delete the wallet from Cielo.
* **Add to list**: Add the selected wallet to a new or existing list.
* **Advanced:** Applies advanced settings to all wallets within the selected list. Includes setting minimum tx value, tx type, chain selection, and bot selection. Note: advanced settings apply to Telegram bots only and _not_ the web app.

At the top of the configure page, a range of icons and menus are available for managing and editing wallets you're following:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-12 at 12.56.33.png" alt=""><figcaption></figcaption></figure>

* **Search bar**: Enter the name or address of a wallet you're following to quickly locate it.
* **All**: Select a specific list and make edits that apply only to wallets within that list.
* **Telegram Bots**: Enable/disable your Cielo Wallet Tracker bot(s).
* **Select All**: Clicking the circle icon on the left applies a yellow tick denoting that all wallets have been selected.
* **Slider icon**: Click this to apply advanced edits to all wallets within the selected list.
* **Brush icon**: Click this to display wallets that are currently unassigned to a list. Note: wallets that default to _All_ are classified as unassigned.
* **Wallets**: Displays the number of wallets you are following. In the screeenshot above, the user is following 36 wallets.

Now that we've explained how to add and edit wallets, we'll move on to lists, the final ability that the configure section of Cielo provides.
