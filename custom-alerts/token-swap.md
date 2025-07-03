# Token Swap

Available to Pro and Whale users, Token Swap allows you to receive an alert any time a swap of at least $1,000 is made for a particular token. Just enter the token's contract address, network, and minimum swap size and you'll receive an alert any time an onchain trade is made that meets this criteria.

Token Swap is available on the following networks: _Solana, Ethereum, Base._

For tokens that are deployed on multiple networks, such as USDC, you will only receive an alert for tx on the network you have specified. Similarly, where there are multiple versions of a token deployed on one network, such as USDC, you will only receive an alert for tx that match the contract address you have entered.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-03 at 16.07.30.png" alt="" width="375"><figcaption><p>Creating an alert for ARB token swaps</p></figcaption></figure>



{% hint style="info" %}
Cielo enforces a minimum $1,000 threshold for tokens you're tracking. This is to prevent your feed and bots from being overwhelmed by alerts.
{% endhint %}
