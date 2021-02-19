# Farm - Liquidity Mining

### TRU incentive distribution Farms <a id="what-are-the-incentives-for-liquidity-mining-tru"></a>

To farm TRU by providing liquidity outside of TrueFi, LP tokens need to be staked in exchange for farm tokens. Holders of LP tokens can claim rewards in TRU as incentive for providing liquidity. These incentives are:

* TFI - LP - This provides additional incentive for the liquidity providers of the Truefi lending pool.
* Uniswap ETH/TRU - This will incentivise TRU liquidity versus ETH. ETH holders can farm TRU using ETH with an upside to both.
* Uniswap TUSD/TFI - LP - This provides much needed liquidity for swapping pool tokens and TUSD. It may be very useful for pool token holders who need TUSD liquidity in/out of the pool. You can earn yield through TrueFi, uniswap fees, and TRU rewards.

You can start liquidity mining TRU on the [Farm](https://app.truefi.io/farm) page. Check out our step-by-step video guide below:

{% embed url="https://www.youtube.com/watch?v=BYGfqpdfILA" %}

### Farm Smart contracts

| Farm | Contract |
| :--- | :--- |
| TFI - LP \(proxy\) | [0x8FD832757F58F71BAC53196270A4a55c8E1a29D9](https://etherscan.io/address/0x8FD832757F58F71BAC53196270A4a55c8E1a29D9) |
| Uniswap ETH /TRU \(proxy\) | [0xED45Cf4895C110f464cE857eBE5f270949eC2ff4](https://etherscan.io/address/0xED45Cf4895C110f464cE857eBE5f270949eC2ff4) |
| Uniswap TUSD /TFI - LP \(proxy\) | [0xf8F14Fbb93fa0cEFe35Acf7e004fD4Ef92d8315a](https://etherscan.io/address/0xf8F14Fbb93fa0cEFe35Acf7e004fD4Ef92d8315a) |

### TRU Distributor Smart contracts

| Farm | Contract |
| :--- | :--- |
| TFI - LP \(proxy\) | [0xfB8d918428373f766B352564b70d1DcC1e3b6383](https://etherscan.io/address/0xfB8d918428373f766B352564b70d1DcC1e3b6383) |
| Uniswap ETH /TRU \(proxy\) | [0x8EFF7d12118Fd599772D6448CDAd11D5fb2568e0](https://etherscan.io/address/0x8EFF7d12118Fd599772D6448CDAd11D5fb2568e0) |
| Uniswap TUSD /TFI - LP \(proxy\) | [0xCc527F4f8c76dB1EBA217d001cCc6f8bD9e0D86E](https://etherscan.io/address/0xCc527F4f8c76dB1EBA217d001cCc6f8bD9e0D86E) |

To calculate the incentive distribution for a farm you can divide the totalAmount by duration. Visit the etherscan link to the smart contract, click on Contract, then click on Read as Proxy. You will find the two parameters totalAmount and duration. The duration is in seconds.

TRU distribution per day = \(totalAmount/10^8\) / \(duration/\(24\*3600\)\)

### What are the risks of participating in TrueFi farms? <a id="what-is-the-distribution-schedule-of-tru-for-liquidity-providers"></a>

**TFI-LP** - There is no additional risk associated with staking your TrueFi LP tokens. You are inherently exposed to borrower default risk as a depositor but there is no additional risk for staking TFI-LP tokens.  
  
**Uniswap ETH / TRU** - Risk of impermanent loss and price exposure to ETH and TRU.  
  
**Uniswap TUSD / TFI - LP** - Risk of impermanent loss due to price difference between TFI-LP and TUSD. As a holder of TFI-LP tokens these liquidity providers also inherit borrower default risk.

