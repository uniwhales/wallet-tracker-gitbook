# Configure

The [configure](https://app.cielo.finance/configure) page is your mission control. It’s where you adjust the setting for wallets you’re following and the corresponding Telegram bot(s) they’re paired with.

* Create custom lists
* Import premade Cielo lists
* Activate and deactivate wallets you’re following
* Rename wallets and map them to different bots
* Set advanced filters for tx alerts

## Getting started

If you have no wallets assigned to your Telegram bots, the configure page shows the following message:

<figure><img src=".gitbook/assets/unnamed (8).png" alt=""><figcaption></figcaption></figure>

You can start adding wallets by pasting their address into the box on the right hand side. Let’s run through an example of how to do that.

We’re going to create an alert for the following address:

_0xAb5801a7D398351b8bE11C439e05C5B3259aeC9B_

This is one of Vitalik Buterin’s known public wallets. It’s already labeled as such on [Etherscan](https://etherscan.io/address/0xab5801a7d398351b8be11c439e05c5b3259aec9b). Here’s how to add it to Cielo:

1. Paste the address into the **Wallet Address** field.
2. Add an optional label. Here, we’ll call it VB.
3. Choose which List you wish to assign it to. In this example, we only have one List created so it will default to **All**.
4. Choose which bot you wish to assign the wallet to (Whale members only).
5. Click **Add Alert**.

<figure><img src=".gitbook/assets/unnamed (9).png" alt=""><figcaption></figcaption></figure>

💁‍♀️ And that’s it. You’re now following your first wallet in Cielo.

You’ll see the wallet appear like so:

<figure><img src=".gitbook/assets/unnamed (10).png" alt=""><figcaption></figcaption></figure>

Go to your Cielo Feed and you’ll see it’s now populated with recent tx involving this wallet. As you can see, Vitalik’s address receives a lot of spam tx.

<figure><img src=".gitbook/assets/unnamed (11).png" alt=""><figcaption></figcaption></figure>

Now let’s return to Customize and add a second wallet. This time we’ll go with an ENS address. _99th.eth_ is an active NFT collector with a few BAYC to their name. There’s no need to add their wallet address: the ENS will suffice.

This time, we'll click **Advanced Settings** and include some additional filters. In the pop-up that appears you can set a minimum transaction value (in USD), deselect any chains you don’t wish to receive alerts for, and do the same for transaction types you wish to screen under **Alert Filter**.

{% hint style="info" %}
**Note:** Advanced Settings only filters tx that appear in your Telegram bot. It does not exert any effect on Cielo. For example, if you select _Avalanche_ only under Advanced Settings, your Telegram bot will only show tx from that occur on Avalanche network – but Cielo will display tx across all 12 EVM chains.
{% endhint %}

When you’ve finished adjusting Advanced Settings, click the blue **Add Alert** button and within a couple of seconds the wallet will appear in your list of addresses on the Customize page.

<figure><img src=".gitbook/assets/unnamed (12).png" alt=""><figcaption></figcaption></figure>

Now let’s adjust some settings for the two wallets we’ve just added. As you can see, the bot that each address is assigned to is clearly displayed, while hovering over the wallet address allows you to copy it to clipboard.

Click on the three horizontal dots and you’ll be given three options:

**Profile**: Takes you to a Cielo page showing all recent tx for that address.

**Edit Alert**: Opens a popup where you can adjust the wallet name, bot, and any lists it’s assigned to.

**Unfollow**: Delete the wallet from your Cielo dashboard and Telegram altogether.

The final option that appears alongside each wallet is a blue button. Click on this to disable Telegram alerts for the wallet.

{% hint style="info" %}
**Note**: After switching off the blue button, the wallet will remain in Cielo and its tx will be visible in your Cielo Feed. It will only disappear from the Telegram bot channel. Click the button again to re-enable Telegram alerts.
{% endhint %}

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
