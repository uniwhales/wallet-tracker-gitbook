# Feed

Your feed displays recent transactions (tx) from wallets you’re following. Each row represents an onchain tx and is enhanced with labeling and links to aid your understanding.

A typical entry might show the wallet (_Address or ENS/.sol_) tx type (_Swap_), network (_Arbitrum_), protocol (_Uniswap_), tokens exchanged (_ETH>USDC_), tx value ($800), and  elapsed time since the tx occured (_2 mins ago_). For NFTs a thumbnail is also shown.

Upon loading your feed, you will see a pinging blue dot at the top. This denotes that a web sockets connection is active that will continually refresh your feed whenever new transactions are delivered. Click the audio icon alongside the blue dot if you'd like to receive an audible alert whenever your feed updates. This is helpful when you're browsing or trading in other tabs and want to learn instantly whenever a new alert arrives.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-28 at 17.26.53.png" alt=""><figcaption></figcaption></figure>

## Reading your feed



A single transaction looks like this:

<figure><img src="../.gitbook/assets/Screenshot 2025-02-28 at 17.27.55.png" alt=""><figcaption></figcaption></figure>

Or if a wallet makes a series of related transactions within a short timeframe, Cielo will cluster them:

<figure><img src="../.gitbook/assets/Screenshot 2025-02-28 at 17.44.51.png" alt=""><figcaption></figcaption></figure>

Click on the name or label assigned to a wallet (e.g. _dolgame.eth_; _Major Airdrop Receiver_) to open a new page for that wallet profile. For example, [**this**](https://app.cielo.finance/profile/0xe3c5f195efb34d723543d8bd5bf85a910a22852e) is the wallet profile for 0xprinterr.eth.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.34.31.png" alt=""><figcaption><p>0xprinterr.eth, which has been labeled in Cielo as <strong>Onchain267</strong></p></figcaption></figure>

The **High TX** label alongside this wallet shows that it is extremely active onchain. If you enable Telegram alerts for this wallet, you'll receive a lot of notifications by default. You can resolve this by clicking the **Edit** icon for this wallet and selecting **Alert Settings**.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.40.47.png" alt="" width="348"><figcaption><p>Cielo lets you specify alerts for each wallet</p></figcaption></figure>

## Learning more

Cielo displays multiple data points for each tx that appears in your feed. Click on the icons, wallet name, and other metadata to learn more.

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 15.53.53.png" alt=""><figcaption></figcaption></figure>

In the above transaction, the following actions are available:

**Wallet Name** _(Onchain209)_: Click to open wallet profile page

**List** (_Library Onchain_): Click to open the list containing this wallet

**Wallet Address** _(0xac)_: Click to copy the address to clipboard

**Token Icon**: Click to view recent market data for this token and chart (You can change your default chart provider in [Settings](https://app.cielo.finance/settings))

**Timestamp** _(3 mins ago)_: Click to open blockchain explorer link



If you see a rocket icon displayed beside a tx, it means it’s the first time the wallet has traded this particular token:

<figure><img src="../.gitbook/assets/Screenshot 2024-03-02 at 16.06.59.png" alt=""><figcaption></figcaption></figure>

Depending on the transaction, other information displayed may include include the tx type, number of tokens swapped, token price, and total tx value.

###

\
