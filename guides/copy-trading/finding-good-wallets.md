# Finding Good Wallets

Use the following resources to discover good quality wallets to copy trade.

#### 1. Cielo Discovery Page

Avilable to Pro and Whale users, Cielo’s built-in [Discovery page](https://app.cielo.finance/wallet-discovery) (trending) is designed for this exact purpose. Some key strategies here:

* Sort by PnL, ROI, or win rate to find consistently profitable wallets.
* Filter by chain (ETH, BSC, Base, Solana etc.)&#x20;
* Select a tag that you find interesting. (Human Operated, Gem Finder, High Winrate etc.)
* Look for wallets whose last trade was within the last 24 hours.
* Trace a wallet’s full trading history and see how often they win vs. cut losses.



#### 2. Cielo API

The [Cielo API](https://api-info.cielo.finance/) lets you build custom scripts to automate wallet discovery:

* Fetch trending wallets by for example Chain, PnL, Winrate, Hold Time, Last Trade.
* Analyze behavior over time
* Combine with Discord/webhook alerts to get notified when top wallets act.



#### 3. Blockchain Explorers (Etherscan, Basescan, Solscan etc.)

Classic but still very powerful. Some angles here:

* Look for wallets interacting with new tokens or contracts just deployed.
* Use token holders [pages](https://solscan.io/token/KMNo3nJsBXfcpJTVhZcXLW7RmTwTt4GVFE7suUBo9sS#holders) (top 100 holders of a memecoin) and trace their other trades.
* Also useful for confirming if a wallet is trading manually or via a smart contract/bot.
* When found, you can open these wallets in Cielo for review.

####

#### 4. Token Order Books on CEXs

Not directly onchain, but can be a signal source:

* Track tokens that just got listed on major CEXs (e.g., Binance, KuCoin).
* Backtrace wallets that were active just before the CEX listing – they’re likely well-connected.
* Use CEX data + DEX data to see wallets that profit from arbitrage or pre-listing pumps.
* Bonus tip: Check wallets that interact with bridge contracts or liquidity deployments just before listings.

####

#### 5. Smart Money Trackers (Arkham, Nansen, DeBank, Zerion, Chainedge)

These tools already analyze wallets for you. Specific things to do:

* Use Arkham Intelligence to identify funds or whale wallets.
* Use Nansen's “Smart Money” tags to find early buyers, yield farmers, and DEX traders.
* Use DeBank to see full wallet portfolios and yield positions.
* Filter by activity e.g. wallets that do $X in swaps per week.
* Use ChainEDGE to track elite on-chain traders and replicate profitable strategies.
* Alpha Hunter&#x20;
* Dune dashboards

####

#### 6. Telegram/Discord Alpha Groups + Bot Channels

These are goldmines.

* Join groups on Telegram  that share wallet addresses when a call hits. You can find groups for example in the channel of well-known copy trade bots.
* Use bots like DexScreener, DexTools, and CieloBot to track real-time buys/sells.
* Build a system to log addresses mentioned in groups, then analyze trade histories.\


#### 7. Token Sniping Bots

Some wallets are clearly sniping newly deployed contracts.

* Identify first wallets to buy new tokens with low gas (they likely used a bot).
* Backtrace contract deployments and pair creations using DexScreener or TokenSniffer.
* Wallets sniping low-liquidity pairs early are high-risk, high-reward and could be copy trade gems but the potential of losing funds by copying these wallets is significant.

_Only copy sniping bots if you are experienced and understand the risk you’re taking on._



**8. Copy Wallets of Known Influencers**

Some influencers trade publicly from known wallets:

* Find ENS names or promoted trades on their X/Twitter profiles.
* Use DeBank or Cielo to trace their trades.
* Cross-reference with Cielo to see if they're actually profitable.
