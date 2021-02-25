# Loan approval process

### Voting on loan applications

To vote on loan applications, you need stkTRU. To learn more about how to acquire stkTRU please view the section on [Staking](stake.md). Once you have stkTRU you can visit the [Stake](https://app.truefi.io/stake) page and vote on the loan applications listed on the page. 

The stkTRU balance with which you can vote on loan applications is equal to the stkTRU balance held by your wallet when the loan application was created. You will not be able to vote on loan applications with stkTRU balance acquired after a loan application was created.

Voters can either vote YES or NO with stkTRU on a loan application. Voting YES means you are predicting that the loan is not likely to default, and voting NO means you are predicting that the loan is likely to default. Voters can vote with the entire stkTRU balance of their wallet, including the stkTRU balance delegated to their wallet address.  

Voting on loan applications does not lock your stkTRU, you can use your stkTRU balance to vote on multiple loan applications. 

### What’s the voting period for voting on loan applications? 

There is no specific time period for stkTRU holders to vote on loan applications. After a loan application is live on the TrueFi platform, stkTRU holders can start voting on the loan until the loan application is funded by the lending pool or cancelled by the borrower. 

However, there is a minimum time period that must pass before a loan can be funded by the lending pool. This time period is called the minimum voting period which corresponds to the votingPeriod parameter set in the TrueLender smart contract. 

Visit the [etherscan link](https://etherscan.io/address/0x16d02Dc67EB237C387023339356b25d1D54b0922#readProxyContract) to the TrueLender \(proxy\) smart contract, click on Contract, then click on Read as Proxy. You will find the parameter votingPeriod in seconds. 

stkTRU holders can modify or cancel their votes any number of times before the loan has been funded by the lending pool or cancelled by the borrower.

### How are loan applications approved? 

Loans are approved or rejected based on conditions set in three smart contracts: [TrueFi LP](https://etherscan.io/address/0xa1e72267084192db7387c8cc1328fade470e4149), [TrueRatingAgencyV2](https://etherscan.io/address/0x05461334340568075bE35438b221A3a0D261Fb6b), and [TrueLender](https://etherscan.io/address/0x16d02Dc67EB237C387023339356b25d1D54b0922). 

stkTRU holders can vote on loan applications to signal their willingness to approve or reject the loan by voting YES or NO respectively. 

Only whitelisted borrowers can submit their loan applications to the TrueRatingAgencyV2 contract. Whitelisted addresses will return true when queried against allowedSubmitters in the TrueRatingAgencyV2 contract.  

The following parameters set in the TrueLender contract should be satisfied for a loan to be approved: 

TrueLender \(proxy\): [0x16d02Dc67EB237C387023339356b25d1D54b0922](https://etherscan.io/address/0x16d02Dc67EB237C387023339356b25d1D54b0922)

1. maxSize and minSize refer to the maximum and minimum loan amount. 
2. maxTerm and minTerm refer to the maximum and minimum loan term. The values are in seconds. 
3. maxAPY and minAPY refer to the maximum and minimum APR for the loans. 
4. participationFactor refers to the minimum number of Yes votes that a loan must receive in order to be approved. For example, if the participation factor is 5000, it means that for a loan of 1,000,000 to be approved it should receive a minimum of 500,000 Yes votes. 
5. riskAversionFactor is a factor in the pool’s expected value calculation that can be modified to reflect the pool’s risk tolerance. If this value is set higher, then loan applications will need to clear a higher hurdle in order to be approved. Only those loan applications where the expected value is greater than zero will be approved \(see the ‘Expected value of loan’ section for more information\)

### Expected value of a loan

In order for a loan to be approved, it must have a positive expected value as calculated by the TrueFi lending pool. The lending pool uses data provided by the TrueRatingAgencyV2 contract to determine the probability of default for the loan.

Take the example below:

A loan of principal = 1,000,000 TUSD, term = 30 days, and APR = 12% receives a total of 1,200,000 stkTRU votes, of which 1,150,000 are YES votes and 50,000 are NO votes. 

Let’s assess whether the loan would be approved by the protocol’s expected value assessment, where \(Upside potential\) - \(Risk aversion factor\) x \(Downside potential\) must be greater than 0.

#### Downside potential calculations:

* **Probability of default** = \(\# of NO votes\) / \(total votes received\) 
  * Example: 50,000 / 1,200,000 = 4.17% 
* **Maximum downside** = loan principal \(worst case assumes no principal is paid back\)
  * Example : 1,000,000 TUSD
* **Downside potential** = Probability of default \* Principal
  * Example: \(4.17%\) \* \(1,000,000 TUSD\) = 41,700 TUSD

#### Upside potential calculations:

* **Probability loan repaid** = 1 - Probability of default
  * Example: 1 - 4.17% = 95.83%
* **Upside potential** = \(Probability loan repaid\) \* \(interest amount\)
  * Example: \(95.83%\) \* \(1,000,000 TUSD x 12% x 30/365\) = 95.83% \* 9,863 TUSD = 9,451.72 TUSD.

#### Expected value calculation:

For this example, we assume the risk aversion factor is set to 1.5.

**Expected value** = \(Upside potential\) - \(Risk aversion factor\) x \(Downside potential\)

Example: \(9,451.72 TUSD\) - \(1.5 \* 41,700 TUSD\) = -52,967 TUSD

Since this loan’s expected value is less than zero, this loan would not be approved. 

### Incentive for voting on loan applications

For voting on loan applications stkTRU holders would receive rewards in the form of TRU tokens. The rewards will be claimable as soon as the loan is withdrawn by the borrower and the status of the loan becomes active. 

_**TRU Reward = \(interest \* TRU distribution factor \* multiplier\)**_

#### Interest = interest = \(loan APR \* term \* principal\) 

The loan APR, term and the principal can be obtained from the respective loan token contracts.

#### TRU distribution factor = \(TRU remaining in distributor\) / \(Total TRU allocated for distribution\)

This can be obtained from the RatingAgencyV2Distributor contract.  
RatingAgencyV2Distributor \(Proxy\): [0x6151570934470214592AA051c28805cF4744BCA7](https://etherscan.io/address/0x6151570934470214592AA051c28805cF4744BCA7)

Visit the [etherscan link](https://etherscan.io/address/0x6151570934470214592AA051c28805cF4744BCA7) to the RatingAgencyV2Distributor \(proxy\) smart contract, click on Contract, then click on Read as Proxy. The parameters are amount and remaining. remaining corresponds to the TRU remaining in the distributor and amount is the total amount of TRU that was allocated for distribution. 

Multiplier is set in the TrueRatingAgencyv2 contract. The parameter is called rewardsMultiplier. 

TrueRatingAgencyV2 \(Proxy\): [0x05461334340568075bE35438b221A3a0D261Fb6b](https://etherscan.io/address/0x05461334340568075bE35438b221A3a0D261Fb6b)

