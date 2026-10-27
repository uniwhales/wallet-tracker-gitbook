# Transaction types

### Feed and WebSocket values

Use these values in the feed's `txTypes` parameter and in the WebSocket `tx_types` filter. Each feed item carries its type in `tx_type`.

| Value                  | Transaction                                                                |
| ---------------------- | -------------------------------------------------------------------------- |
| `swap`                 | Exchange one token for another on a DEX or aggregator.                     |
| `transfer`             | Token transfer. The WebSocket also accepts `transfer_in` / `transfer_out`. |
| `lp`                   | Add or remove liquidity.                                                   |
| `lending`              | Deposit, borrow, repay or withdraw on a lending protocol.                  |
| `bridge`               | Move tokens between chains.                                                |
| `reward`               | Claim rewards.                                                             |
| `staking`              | Stake or unstake.                                                          |
| `perp`                 | Leveraged long or short.                                                   |
| `option`               | Option trade.                                                              |
| `wrap`                 | Wrap or unwrap a token, e.g. ETH ↔ WETH.                                   |
| `flashloan`            | Flash loan.                                                                |
| `nft_trade`            | Buy or sell an NFT on a marketplace or aggregator.                         |
| `nft_sweep`            | Buy several NFTs in one transaction.                                       |
| `nft_transfer`         | NFT transfer.                                                              |
| `nft_mint`             | NFT mint.                                                                  |
| `nft_lending`          | Deposit NFTs as collateral or lend against them.                           |
| `nft_liquidation`      | NFT loan liquidation.                                                      |
| `sudo_pool`            | Sudoswap pool action.                                                      |
| `contract_creation`    | Contract deployment.                                                       |
| `contract_interaction` | Any other contract call.                                                   |

### Transaction type IDs

The wallet tracking endpoints take numeric type IDs in alert filters:

| Type              | ID | Description                                                     |
| ----------------- | -- | --------------------------------------------------------------- |
| Transfer          | 1  | Transfer events.                                                |
| Swap              | 2  | Exchange one token for another on a DEX or AMM.                 |
| LP                | 3  | Provide liquidity, e.g. on Uniswap.                             |
| NFT Transfer      | 4  | Transfer an NFT.                                                |
| Approvals         | 5  | Authorize a contract to move tokens.                            |
| Other             | 6  | Anything that fits no other type.                               |
| NFT Trade         | 7  | Buy or sell an NFT on a marketplace or aggregator.              |
| NFT Mint          | 8  | Mint an NFT.                                                    |
| Contract Creation | 9  | Deploy a contract.                                              |
| Wrap              | 10 | Convert between token standards, e.g. ETH ↔ WETH.               |
| Reward            | 11 | Claim rewards, e.g. for providing liquidity.                    |
| Lending           | 12 | Deposit or borrow on protocols like Aave.                       |
| Option            | 13 | Trade the right to buy or sell at a set price.                  |
| Bridge            | 14 | Move tokens between chains.                                     |
| Perpetual         | 15 | Leveraged long or short, e.g. on GMX.                           |
| NFT Lending       | 16 | Use NFTs as collateral, e.g. on Blur or NFTfi.                  |
| NFT Liquidation   | 17 | NFT loan liquidation.                                           |
| Swap Buy          | 18 | Swap into a token that is not a stablecoin or the native asset. |
| Swap Sell         | 19 | Swap a token into a stablecoin or the native asset.             |
