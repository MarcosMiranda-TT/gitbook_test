# Loan approval process

### Voting on loan applications

To vote on loan applications, you need stkTRU. To learn more about how to acquire stkTRU please view the section on [Staking](stake/). Once you have stkTRU you can visit the [Stake](https://app.truefi.io/stake) page and vote on the loan applications listed on the page. 

The stkTRU balance with which you can vote on loan applications is equal to the stkTRU balance held by your wallet when the loan application was created. You will not be able to vote on loan applications with any stkTRU balance acquired after a loan application was created.

Stakers can either vote YES or NO with stkTRU on a loan application. Voting YES means you are predicting that the loan is not likely to default, and voting NO means you are predicting that the loan is likely to default. Stakers can vote with the entire stkTRU balance of their wallet, including the stkTRU balance delegated to their wallet address.  

Voting on loan applications does not lock stkTRU, stakers can use their stkTRU balance to vote on multiple loan applications. 

### What’s the voting period for voting on loan applications? 

There is no specific time period for stkTRU holders to vote on loan applications. After a loan application is live on the TrueFi platform, stkTRU holders can start voting on the loan until the loan application is funded by the lending pool or cancelled by the borrower. 

However, there is a minimum time period that must pass before a loan can be funded by the lending pool. This time period is called the minimum voting period which corresponds to the votingPeriod parameter set in the TrueLender smart contract. 

Visit the etherscan link to the TrueLender \(proxy\) smart contract, click on Contract, then click on Read as Proxy. You will find the parameter votingPeriod in seconds. 

stkTRU holders can modify or cancel their votes any number of times before the loan has been funded by the lending pool or cancelled by the borrower.

### How are loan applications approved? 

Loans are approved or rejected based on conditions set in three smart contracts: TrueFi lending pool contract, TrueRatingAgency, and TrueLender. 

Only whitelisted borrowers can submit their loan applications to the TrueRatingAgency contract. Whitelisted addresses will return true when queried against allowedSubmitters in the TrueRatingAgency contract.  

The following parameters set in the TrueLender contract should be satisfied for a loan to be approved: 

TrueLender \(proxy\): [0xa606dd423dF7dFb65Efe14ab66f5fDEBf62FF583](https://etherscan.io/address/0xa606dd423dF7dFb65Efe14ab66f5fDEBf62FF583)

TrueRatingAgency \(proxy\): [0x05461334340568075bE35438b221A3a0D261Fb6b](https://etherscan.io/address/0x05461334340568075bE35438b221A3a0D261Fb6b)

stkTRU holders can vote on loan applications to signal their willingness to approve or reject the loan by voting YES or NO respectively. A loan is approved if it satisfies two conditions.

1. Minimum of 15 Million votes 
2. 80% of the votes should be YES

### Incentive for voting on loan applications

For voting on loan applications stkTRU holders would receive rewards in the form of TRU tokens. The rewards will be claimable as soon as the loan is withdrawn by the borrower and the status of the loan becomes active. 

_**TRU Reward = \(interest \* TRU distribution factor \* multiplier\)**_

#### Interest = \(loan APR \* term in days \* principal\) /365

The loan APR, term and the principal can be obtained from the respective loan token contracts.

#### TRU distribution factor = \(TRU remaining in distributor\) / \(Total TRU allocated for distribution\)

This can be obtained from the RatingAgencyV2Distributor contract.  
RatingAgencyV2Distributor \(Proxy\): [0x6151570934470214592AA051c28805cF4744BCA7](https://etherscan.io/address/0x6151570934470214592AA051c28805cF4744BCA7)

Visit the etherscan link to the RatingAgencyV2Distributor \(proxy\) smart contract, click on Contract, then click on Read as Proxy. The parameters are amount and remaining. Remaining corresponds to the TRU remaining in the distributor and amount is the total amount of TRU that was allocated for distribution. 

Multiplier is set in the TrueRatingAgency contract. The parameter is called rewardsMultiplier. 

