# Token Swap

Token Swap allows you to receive an alert any time a swap of at least $1,000 is made for a particular token. Just enter the token's contract address, network, and minimum swap size and you'll receive an alert any time an onchain trade is made that meets this criteria.

Token Swap is available on the following networks: _Solana, Ethereum, Base._

For tokens that are deployed on multiple networks, such as USDC, you will only receive an alert for tx on the network you have specified. Similarly, where there are multiple versions of a token deployed on one network, such as USDC, you will only receive an alert for tx that match the contract address you have entered.

<figure><img src="https://1250667054-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgZTvWhkjLJ8uCLtiUaPq%2Fuploads%2FiSEJpUVF9HAxSmGKaJKA%2FScreenshot%202025-07-03%20at%2016.07.30.png?alt=media&#x26;token=2df39cdf-e454-44d5-ac99-ad7275e9f846" alt="" width="375"><figcaption><p>Creating an alert for ARB token swaps</p></figcaption></figure>

{% hint style="info" %}
Cielo enforces a minimum $1,000 threshold for tokens you're tracking. This is to prevent your feed and bots from being overwhelmed by alerts.
{% endhint %}
