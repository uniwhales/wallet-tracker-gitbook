# Configure

The [configure](https://app.cielo.finance/configure) page is your mission control. It’s where you add wallets, set alert filters, configure Telegram notifications, and create lists. There’s a lot you can do in configure. Mastering the features contained within this page is the key to mastering Cielo.

### Getting started

If you're not following any wallets, your configure page will start out blank:

<figure><img src=".gitbook/assets/Screenshot 2023-06-10 at 10.45.59.png" alt=""><figcaption></figcaption></figure>

If you _are_ already following wallets or public lists, however, your configure page will look like this:

<figure><img src=".gitbook/assets/Screenshot 2023-06-10 at 10.46.51.png" alt=""><figcaption></figcaption></figure>

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

<figure><img src=".gitbook/assets/Screenshot 2023-06-10 at 10.53.23.png" alt=""><figcaption></figcaption></figure>

💁‍♀️ And that’s it. You’re now following your first wallet in Cielo.

The wallet will now appear in configure:

<figure><img src=".gitbook/assets/Screenshot 2023-06-10 at 10.57.14.png" alt=""><figcaption></figcaption></figure>

Visit your Cielo [feed](https://app.cielo.finance/feed) and you’ll see recent tx involving this wallet:

<figure><img src=".gitbook/assets/Screenshot 2023-06-10 at 10.58.31.png" alt=""><figcaption></figcaption></figure>

Now let’s return to [configure](https://app.cielo.finance/configure) and add a second wallet. This time we’ll go with an ENS address. _99th.eth_ is an active NFT collector. There’s no need to add their wallet address: the ENS will suffice. We'll apply the wallet label _NFT Holder_.

Now, under **Alert Settings**, we'll add some Telegram bot filters. In the pop-up that appears you can set a minimum transaction value (in USD), deselect any chains you _don’t_ wish to receive alerts for, and do the same for transaction types you wish to screen under **Alert Filter**.

{% hint style="info" %}
**Note:** Alert Settings only apply filters to your Telegram bot(s). They do not affect tx as they appear in the Cielo web app. For example, if you limit your chain selection to _Avalanche_, your Telegram bot will only show tx that occur on Avalanche network – but the Cielo web app will continue to display tx for all EVM chains.
{% endhint %}

<figure><img src=".gitbook/assets/Screenshot 2023-06-12 at 11.51.42.png" alt=""><figcaption><p>Using the settings shown here, the Telegram bot will only show alerts for tx involving NFTs.</p></figcaption></figure>

When you’ve finished adjusting **Alert Settings**, click **Save changes** and the wallet will appear in your list of addresses on the configure page.



### Editing wallets

After manually adding wallets to Cielo or following one or more public lists, your configure page will look something like this:

<figure><img src=".gitbook/assets/Screenshot 2023-06-12 at 12.02.13 (1).png" alt=""><figcaption><p>The two wallets at the top of the page (NFT Collector + VB) were manually added. The remaining wallets have been imported by following a public list called <em>NewWhaleWallets</em>.</p></figcaption></figure>



From left to right, each wallet as it appears on the configure page can be read and interacted with as follows:

* **Select button**: Click the circular button on the left to select the wallet. Repeat this action to select multiple wallets.
* **Avatar**: Click the colored avatar to open a new Cielo page for the wallet in question. This will display all recent tx involving this wallet.
* **Wallet name**: Descriptive label applied when you added the wallet to Cielo or when the list creator added it e.g. _NFT Collector_.
* **Edit icon**: Clicking the icon to the right of the wallet name opens a popup where you can edit the wallet settings.
* **Address:** Displays abbreviated view of the wallet's address e.g. _0x01...795a_. Click the icon to the right of the wallet to copy the full address to your clipboard.
* **Last active**: Time elapsed since the wallet last made a transaction.
* **List name**: Name of the list the wallet is assigned to. If no list is selected, this will default to _All_.
* **Telegram alerts**: Denotes whether Telegram bot alerts are on/off for the wallet.

## Add Contacts

With Cielo, you can import the ENS addresses for the Twitter accounts you’re following. This is a useful way of creating a custom List for accounts of interest without the need to import them manually.

<figure><img src=".gitbook/assets/Screenshot 2022-10-17 at 12.14.50.png" alt=""><figcaption><p>Add Contacts can be found in the top right of the Customize page.</p></figcaption></figure>

In [Customize](https://app.cielo.finance/customize), click the **Add Contacts** button at the top of the page. You will then be connected to the Twitter API which will prompt you to import your contacts. Cielo will only import accounts you’re following that meet this criteria. It does this by scanning their username and bio to detect a .ens handle.

Note that it can take over a minute for your Twitter contacts to be analyzed and imported.

## Bulk Add

Bulk Add is a convenient way of importing multiple addresses in one go. Using this feature, you can import up to 50 wallet addresses from a CSV file.

<figure><img src=".gitbook/assets/Screenshot 2022-10-17 at 12.15.48.png" alt=""><figcaption><p>Bulk Add can be found in the top right of the Customize page.</p></figcaption></figure>

Under Customize, click the **Bulk Add** button at the top of the page. You will then be prompted to import the file. As the pop-up explains, addresses should be placed in column one of the file and an optional label for each one should go in column two.

<figure><img src=".gitbook/assets/Screenshot 2022-10-17 at 12.16.31.png" alt=""><figcaption></figcaption></figure>

After uploading the CSV, wait a few seconds and your imported addresses will appear in your Cielo dashboard. They can then be added to a new or existing custom list if desired.

## Bulk Actions

Near the top of the Customize page is an option titled **Bulk Actions**. Clicking on this produces a range of editing options you can apply to some or all wallets you’ve added. Click **Bulk Actions** again and a tick icon will appear alongside all of your wallets. Now click on any wallet(s) you _don’t_ wish to edit. Finally, click on the action you wish to perform (e.g. _Unfollow_) and it will be applied to all wallets that have been ticked.

The **Bulk Actions** option is particularly useful when managing a large number of wallets.

<figure><img src=".gitbook/assets/unnamed (13).png" alt=""><figcaption></figcaption></figure>

To disable Telegram alerts for all wallets or a particular List, under Customize select **Bulk Actions** and then click to tick the yellow circle that appears:

<figure><img src=".gitbook/assets/Screenshot 2022-10-17 at 11.59.09.png" alt=""><figcaption></figcaption></figure>

Click the blue toggle switch to the right and the following pop-up will appear:

<figure><img src=".gitbook/assets/Screenshot 2022-10-17 at 12.01.25.png" alt=""><figcaption></figcaption></figure>

Select **Continue** and Telegram alerts will be disabled for all wallets you have selected.

Click the toggle switch at the top right of the page to reverse this process and re-enable Telegram alerts.
