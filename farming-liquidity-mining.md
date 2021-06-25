# Farm - Liquidity Mining

### TRU incentive distribution Farms <a id="what-are-the-incentives-for-liquidity-mining-tru"></a>

To farm TRU by providing liquidity outside of TrueFi, LP tokens need to be staked in exchange for farm tokens. Holders of LP tokens can claim rewards in TRU as incentive for providing liquidity. These incentives are:

* TrueFi TUSD Pool, TrueFi USDC Pool and TrueFi USDT Pool - This provides additional incentive for the liquidity providers of the TrueFi lending pools.

You can start liquidity mining TRU on the [Farm](https://app.truefi.io/farm) page. 

### Farm Smart contracts

| Farm | Contract |
| :--- | :--- |
| tfTUSD \(proxy\) | [0x8FD832757F58F71BAC53196270A4a55c8E1a29D9](https://etherscan.io/address/0x8FD832757F58F71BAC53196270A4a55c8E1a29D9) |
| tfUSDC \(proxy\) | [0x6b6a4eaba8ba12765df51a859c0fa75894817f5a](https://etherscan.io/address/0x6b6a4eaba8ba12765df51a859c0fa75894817f5a) |
| tfUSDT\(proxy\) | [0xC06E16D2Fbe2b9Fe088a615f23cb20898745Dc6D](https://etherscan.io/address/0xC06E16D2Fbe2b9Fe088a615f23cb20898745Dc6D) |

### TRU Distributor Smart contracts

| Farm | Contract |
| :--- | :--- |
| tfTUSD \(proxy\) | [0xfB8d918428373f766B352564b70d1DcC1e3b6383](https://etherscan.io/address/0xfB8d918428373f766B352564b70d1DcC1e3b6383) |
| tfUSDC \(proxy\) | [0x2185b903867212539f6b744d08fa6fd26c4a9310](https://etherscan.io/address/0x2185b903867212539f6b744d08fa6fd26c4a9310) |
| tfUSDT \(proxy\) | [0xdEc91F8E7C30CEeCb008C82E7f0847aD3Dec98c4](https://etherscan.io/address/0xdEc91F8E7C30CEeCb008C82E7f0847aD3Dec98c4) |

To calculate the incentive distribution for a farm you can divide the totalAmount by duration. Visit the etherscan link to the smart contract, click on Contract, then click on Read as Proxy. You will find the two parameters totalAmount and duration. The duration is in seconds.

TRU distribution per day = \(totalAmount/10^8\) / \(duration/\(24\*3600\)\)

### What are the risks of participating in TrueFi farms? <a id="what-is-the-distribution-schedule-of-tru-for-liquidity-providers"></a>

**TrueFi TUSD Pool or TrueFi USDC Pool** - There is no additional risk associated with staking your TrueFi LP tokens. You are inherently exposed to borrower default risk as a depositor but there is no additional risk for staking TFI-LP tokens.  
  
**Uniswap ETH / TRU** - Risk of impermanent loss and price exposure to ETH and TRU.  
  
**Uniswap TUSD /** tfTUSD - Risk of impermanent loss due to price difference between TFI-LP and TUSD. As a holder of TFI-LP tokens these liquidity providers also inherit borrower default risk.

