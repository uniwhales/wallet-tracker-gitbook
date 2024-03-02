# Feed

Your feed displays recent transactions (tx) from wallets you’re following. Each row represents an onchain tx and is enhanced with labeling and links to aid your understanding.

A typical entry might show the wallet (_Address or ENS/.sol_) tx type (_Swap_), network (_Arbitrum_), protocol (_Uniswap_), tokens exchanged (_ETH>USDC_), tx value ($800), and  elapsed time since the tx occured (_2 mins ago_). For NFTs a thumbnail is also shown.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.18.25.png" alt=""><figcaption></figcaption></figure>

## Reading your feed

A single transaction looks like this:

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.22.57.png" alt=""><figcaption></figcaption></figure>

Or if a wallet makes a series of related transactions within a short timeframe, Cielo will cluster them:

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.28.21.png" alt=""><figcaption></figcaption></figure>

Click on the name or label assigned to a wallet (e.g. _dolgame.eth_; _Major Airdrop Receiver_) to open a new page for that wallet profile. For example, [**this**](https://app.cielo.finance/profile/0xe3c5f195efb34d723543d8bd5bf85a910a22852e) is the wallet profile for 0xprinterr.eth.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.34.31.png" alt=""><figcaption><p>0xprinterr.eth, which has been labeled in Cielo as <strong>Onchain267</strong></p></figcaption></figure>

The **High TX** label alongside this wallet shows that it is highly active onchain.

...it means the wallet in question has high transaction volume. You can still add the address to Cielo, but it could fill your feed with an excessive number of tx.

### Transaction header

The ENS or wallet name assigned within Cielo appears in the top left. Clicking on the wallet name or avatar to the left of it opens a page showing all recent activity for that wallet e.g. [https://app.cielo.finance/feed/0x…72](https://app.cielo.finance/feed/0x)

<figure><img src="../.gitbook/assets/Screenshot 2023-06-08 at 16.48.06.png" alt=""><figcaption><p>Example of a transaction header</p></figcaption></figure>

To the right of the wallet name, an abbreviation of the wallet address is displayed e.g. _0x73...303f_. Click on this to copy the full address to your clipboard. To the right of this, the list this wallet is assigned to is shown (if applicable). Clicking on the list name opens a new window showing all recent tx for wallets within that list. Finally, to the right of the tx header, the date and time of the transaction is displayed.\


### Transaction body

The box on the left applies a label to the tx type e.g. _Send, Borrowed, Contract Interaction_. Below this, the protocol where the tx took place is labeled where available. The logo of the EVM chain where the tx occurred is also shown.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-08 at 16.49.05.png" alt=""><figcaption><p>Example of a transaction body</p></figcaption></figure>

The larger box to the right displays the most important information about the tx: the amount being transacted, the token(s) involved, and the sender or recipient where relevant. If the tx involves an NFT, its thumbnail is displayed. Hovering your cursor over this produces a popup linking to marketplaces where this NFT can be viewed. There’s also a link to the Cielo page for that particular NFT collection.

Hover over a token icon to produce the following pop-up:&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-08-17 at 15.23.05.png" alt=""><figcaption></figcaption></figure>

Then click on the address to copy the token contract or click **Stats** to view current market data:

<figure><img src="../.gitbook/assets/Screenshot 2023-08-17 at 15.23.17.png" alt="" width="371"><figcaption></figcaption></figure>

If you see a star ⭐ displayed beside a tx, it means it’s the first time the wallet has purchased this particular token.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-08 at 16.35.25.png" alt=""><figcaption></figcaption></figure>

Finally, to the right of the transaction body, the elapsed time since the tx occurred is shown e.g. 2 hours. Clicking on this opens a block explorer link to this specific transaction.

### Refreshing your feed

\
When there are new transactions to view in your feed, a notification like this appears at the top of the page:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-08 at 16.38.54.png" alt=""><figcaption></figcaption></figure>

Clicking on it will update your feed to show the latest tx. If you prefer, you can set your feed to auto-update so that new tx are published automatically. To do so, just click the Auto button in the bottom right. The icon will turn yellow to denote that auto-updates are on. Click it again to deactivate.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-08 at 16.37.47.png" alt=""><figcaption></figcaption></figure>

\
