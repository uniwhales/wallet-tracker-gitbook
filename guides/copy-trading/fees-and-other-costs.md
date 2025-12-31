# Fees and Other Costs

When starting with copy trading, understanding the different fees and costs involved is essential for managing your expectations and maximizing your returns. While Solana is known for its low transaction fees, there are still several types of costs you should be aware of when using copy trading bots and platforms.

### 1. Transaction Fees

Every time your bot or platform copies a trade, a small transaction fee is charged by the Solana blockchain. These fees are much lower than on most other blockchains, often just a fraction of a cent per transaction. This is one of the main reasons Solana is popular for active trading and automation.

### 2. Bot and Platform Fees

Most copy trading bots and platforms have their own fee structures, which can vary widely.

* **Subscription Fees**: Some bots require a monthly or yearly subscription to use their services.
* **Performance Fees**: Others might take a percentage of your profits, only charging you when you make money.
* **Per-Trade Fees**: Some platforms charge a small fee for every trade executed on your behalf.

It’s important to review the specific fee schedule for the bot or platform you choose. These fees can add up over time, especially if you're copying many trades or using advanced features like faster execution speed.

### 3. Settings and Customization

Bots often offer different settings that can affect your costs. For example, you might be able to adjust the frequency of trades, the size of each trade, or the number of wallets you follow. More frequent trading or following multiple wallets can increase your total transaction fees. Always consider how your settings might impact your overall costs.

### 4. Token Account Rent

On Solana, every token account (including those created by copy trading bots to hold new tokens) requires a small amount of SOL to be locked up as "rent." This isn’t a fee in the traditional sense, because you can get most of it back by closing unused token accounts later. However, it does temporarily tie up some of your funds, so it’s good to be aware of this when managing your portfolio.

### 5. Refunds and Cost Recovery

One unique advantage of Solana is that when you close a token account you no longer need, the rent you paid is refunded to your wallet. This means you can recover some of your costs simply by cleaning up unused accounts. Many platforms, and even dedicated tools like Sol Incinerator, make it easy to close accounts and reclaim your SOL.

### 6. Hidden and Indirect Costs

Don’t forget about indirect costs such as slippage (the difference between the expected price and the price at which a trade is executed), or the opportunity cost of holding certain tokens. These can affect your overall returns, even if they aren’t listed as explicit fees.



## Understanding token rent on Solana

On the Solana blockchain, rent is a system that ensures users don’t use up too much storage for free. Every account that stores data on Solana has to keep a minimum balance of SOL that depends on how much data it stores. This is called “rent,” but it works more like a refundable deposit than an ongoing fee.

Think of Solana’s rent system like renting a storage locker:

* If you want to store a few boxes, you pay for a small locker.
* If you want to store furniture, you need a bigger locker and pay more (bigger rent deposit).
* As long as you keep paying, your stuff stays safe.
* If you empty your locker and close your account, you get your deposit back<br>

In case you're wondering, here's why this system is used on Solana:

**Deposit, Not a Subscription**: Unlike paying rent for an apartment every month, Solana’s rent is a one-time deposit. As long as you keep enough SOL in your account, you don’t lose any money over time. When you’re done, you can “close your locker” and get your deposit back.<br>

**Encourages Efficient Use**: Just as storage facilities want to avoid people leaving empty boxes in lockers forever, Solana’s rent system encourages users to clean up unused accounts. If you don’t keep enough SOL in your account, Solana can remove your data to free up space for others.<br>

#### How Much Space Do You Need?

The more data you store, the higher your minimum balance needs to be. For example, a basic token account might need about 0.002 SOL as a deposit – just a few cents.<br>

#### What happens if you can't pay for the rent?

If an account on Solana runs out of lamports and falls below the rent-exempt minimum balance, it is at risk of being removed from the network. This means the account may be deleted by the Solana runtime to free up storage space.&#x20;

In practical terms, if you don't keep enough lamports in your account to meet the rent-exempt threshold, your account can no longer store data and might become inaccessible or deleted. This mechanism ensures that only accounts actively maintained and funded remain on the blockchain, preventing unused accounts from taking up valuable storage space.



#### Buying a new token on Solana<br>

* You pay for the token.
* You also pay a small extra amount of SOL as rent for the new account that holds your token.
* If you delete the account later, you get the SOL back.



### How to Close a Solana Account

To close a Solana account (such as a token account), you need to remove all tokens from it and then close the account. When you close the account, any SOL (including the rent-exempt minimum) that was locked in it will be returned to your wallet.

**Steps to Close an Account:**

* Transfer any remaining tokens out of the account.
* Use a wallet interface (like Phantom, Solflare, or Backpack) or a tool like Sol Incinerator to close the account and reclaim the SOL.
* If you prefer command-line tools, you can use the Solana CLI to close accounts. This typically involves commands like: spl-token close-account \<ACCOUNT\_ADDRESS> \<RECIPIENT\_ADDRESS>, which sends any remaining SOL to the recipient address you specify.

**Note:** Simply sending the rent to another address will not close the account. The account must be formally closed, either through a wallet UI, a dApp like Sol Incinerator, or the CLI.

### What is Sol Incinerator?

Sol Incinerator is a decentralized application (dapp) built for Solana that lets users easily burn (permanently delete) unwanted tokens, NFTs, and even SOL domains from their wallet. When you burn these assets, any SOL locked as storage rent in those accounts is returned to your wallet.<br>

**Key Features:**

* Burn multiple unwanted assets at once.
* Reclaim SOL locked up as rent in token/NFT accounts.
* Clean up spam, dead tokens, and low-value NFTs.
* Works with major Solana wallets like Phantom, Solflare, Backpack, and Glow.

### How to Use Sol Incinerator

1. Visit the official Sol Incinerator website (e.g., [www.sol-incinerator.com](http://www.sol-incinerator.com/)).
2. Connect your wallet (Phantom, Solflare, Backpack, etc.).
3. The tool will scan your wallet for burnable assets: tokens, NFTs, domains, and even inactive wallets.
4. Review the list of assets and see how much SOL you will reclaim for each.
5. Select the assets you want to burn (be careful, as this process is irreversible).
6. Confirm and execute the burn transaction in your wallet.
7. The assets are permanently removed and the SOL rent is returned to your wallet.

\
\
<br>
