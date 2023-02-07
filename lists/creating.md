# Creating

You can create a List based around any topic you’d like to follow, whether it’s for your own wallets or tracking which influencers are minting NFTs. After creating a List, you can populate it with addresses you’re already following or add new addresses to it.

To get started, go to the [Customize](https://app.cielo.finance/customize) page and click the white plus icon to create a new List.

<figure><img src="../.gitbook/assets/unnamed (22).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/unnamed (23).png" alt=""><figcaption></figcaption></figure>

In this example we’re creating a new List titled _NFT Minters_.

Select Create List and your new List will appear as a tab at the top of the Customize page.

<figure><img src="../.gitbook/assets/unnamed (24).png" alt=""><figcaption></figcaption></figure>

Click on the List and you will see the following message.

<figure><img src="../.gitbook/assets/unnamed (25).png" alt=""><figcaption></figcaption></figure>

Let’s add some wallets to this List and apply some filters.

Click on **All** to return to the list of all wallets you’re following.

<figure><img src="../.gitbook/assets/unnamed (26).png" alt=""><figcaption></figcaption></figure>

In this example we’re following two wallets, which were added as examples earlier in this guide: _99th.eth_ and _Vitalik Buterin_. Since 99th is an NFT collector, let’s add them to the newly created _NFT Minters_ List.

Click the yellow circle to the left of the wallet you wish to add and select **Add to List**. You will then see the following pop-up.

<figure><img src="../.gitbook/assets/unnamed (27).png" alt=""><figcaption></figcaption></figure>

If you have multiple Lists, select the one you wish to use from the dropdown menu and press **Confirm**.

Now, when you click on the NFT Minters tab you can see that _99th_ has been added.

<figure><img src="../.gitbook/assets/unnamed (28).png" alt=""><figcaption></figcaption></figure>

Let’s apply some filters to this address that will dictate which transaction types appear for _99th_ within the Cielo Wallet Tracker channel.

{% hint style="info" %}
**Note**: The following section describes filters that apply to your bot Telegram channel only. These filters will not be applied to your Cielo Feed or to the custom List being described.
{% endhint %}

Click **Bulk Actions** and then tick the yellow circle to the left of the address you wish to edit. Then select **Advanced Settings**.

In this example, we’re going to filter 99th’s transactions so that the EVM Wallet Tracker bot only receives notifications for NFT mints that occur on Ethereum network.

<figure><img src="../.gitbook/assets/unnamed (29).png" alt=""><figcaption></figcaption></figure>

First click on **Alert Filters** and tick the tx types you wish to follow (in this case, **NFT Mint**).

<figure><img src="../.gitbook/assets/unnamed (30).png" alt=""><figcaption></figcaption></figure>

Then click on **Chain Selection** and deselect any networks you don’t wish to follow. By default, all networks are enabled.

When you’re done, select **Save Changes**. Your Cielo Wallet Tracker bot will now only receive notifications of 99th tx if they are NFT mints that occur on Ethereum.

## Expanding a list

Now let’s add a second address to the _NFT Traders_ List. This time, we’ll choose an address that isn’t already in your Cielo Feed.

_0x6c8C7539Bf6A61c249c520C837Ed0e19F91344dC_ is the address of _gdzxvdg_, a well-known NFT flipper whose trades appear in the NFT Ideas [Telegram channel](https://t.me/NFTideasEVMTracker).

On the right hand side of the NFT Traders page, paste in this wallet address and tag it with the label _gdzxvdg_. Under **Advanced Settings** we’ll set the alert filters to track **NFT Mint** only.

Select **Add Alert** and within a few seconds you’ll see the newly added wallet appear in the _NFT Minters_ List.

<figure><img src="../.gitbook/assets/unnamed (31).png" alt=""><figcaption></figcaption></figure>

If you _don’t_ want to see the transactions from this List in your Cielo Wallet Tracker channel, just click the blue switch to the right of each address. This will remove the address from your Telegram channel while retaining it in your Cielo dashboard.

Now that you’ve created your first List, go to Feed and from the dropdown menu at the top of the page, select the List you wish to view – in this case _NFT Minters_.

<figure><img src="../.gitbook/assets/unnamed (32).png" alt=""><figcaption></figcaption></figure>

Transactions that meet the criteria you’ve applied to them will now appear in your Cielo Feed, while everything else will be excluded.

💡 At any time, you can return to your master Feed by selecting **All**.

Because your Cielo Feed gives you additional filtering controls, you can further refine a List using the options at the top of the page. Just click on **Filter Tx types and Chains**.

<figure><img src="../.gitbook/assets/unnamed (33).png" alt=""><figcaption></figcaption></figure>

In this example, we’re filtering the _NFT Minters_ list to display only tx on BNB Chain. As you can see, gdzxvdg hasn’t been active on BNB Chain in six months. Just click the **x** beside your chosen filter to remove it and return to default settings.

💁‍♀️ And that’s it. You should now know to create, manage, and filter your own Lists of onchain data. You should also know how to switch between Lists, edit and delete their contents, and apply advanced filters to your Cielo Feed. We’ve also detailed how to control which transactions appear in your Feed, in your custom Lists, and in your Telegram bots.

Using these controls, Cielo lets you create useful dashboards for monitoring the vast majority of onchain events across the most popular EVM chains. If it happens onchain, with Cielo you can tag, track, and comprehend it in near real-time.
