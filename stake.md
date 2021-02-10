# Stake

### How can I stake TRU on loan applications?  <a id="how-can-i-stake-tru-on-loan-applications"></a>

You can either stake YES or NO with your TRU on a loan application. Staking YES means you are predicting that the loan is not likely to default, and staking NO means you are predicting that the loan is likely to default. You can stake any number of TRU on each loan application.

For staking on loan applications created by borrowers, you need to have TrueFi tokens \(TRU\) in the Metamask wallet you have connected to the TrueFi portal. You can view the list of loan applications once you click on the Staking tab.

  
[**View the Staking Video Guide**](https://www.loom.com/share/fbbb213590e141f599862bbd5aee9808)\*\*\*\*

### What is the time period during which I can stake TRU on the loan applications? <a id="what-is-the-time-period-during-which-i-can-stake-tru-on-the-loan-applications"></a>

There is no specific time period for TRU holders to stake on loan applications. After a loan application is live on the TrueFi platform, TRU holders can start staking on the loan until the loan application is approved, rejected or cancelled.   
  
However there is a minimum time period before which a loan cannot be approved or rejected by the lending pool. This time period is called the staking period, which is currently set to 3 days.

TRU holders can change their TRU stakes or withdraw TRU any number of times. Once the borrower has withdrawn the applicable loan principal, staked TRU will be locked until the end of the loan term.

If a loan application has been approved by the lending pool but a borrower has not withdrawn the loan principal due to insufficient funds, TRU Stakers can still change their prediction regarding the outcome of the loan or withdraw the staked TRU entirely.

### What’s my incentive for staking TRU on loan applications? <a id="whats-my-incentive-for-staking-tru-on-loan-applications"></a>

Currently the incentive for TRU stakers like you is to earn more TRU, TrueFi platform’s native token. This mechanism of staking TRU against loan applications forms the basis of TrueFi’s credit risk assessment. In the future this may be extended to assess the credit worthiness of other entities, wallet addresses, protocols, and other parts of the DeFi ecosystem.

Suppose the current incentive structure does not guarantee that the credit prediction market will perform well. In that case it is likely that the system will auto correct and evolve the incentive structure so that the market becomes more efficient.

Since TRU stakers play a pivotal role in assessing the creditworthiness of loan applications, they are currently incentivised in two different ways:

* Rewards for participating in the credit prediction market
* Payouts for correctly predicting the outcome of a loan application

TRU rewards are paid out after the borrower has withdrawn the loan principal. Rewards are paid out proportionally to all TRU stakers of a loan application irrespective of whether they staked YES or NO. The TRU rewarding mechanism currently favors participants for staking their TRU against higher interest rate loan applications and can be claimed over the course of a loan’s term. TRU rewards gained from participation in the credit prediction market can be claimed at any time so that there is more value to staking, rather than having to wait until the end of a loan.

Payouts for correctly predicting a loan application’s outcome are paid at the end of a loan’s term. A loan repayment is considered successful if the borrower has paid out the principal and interest within the loan term. In any other case, a loan is considered to have defaulted even if the borrower delays the payment of the loan beyond the loan term. If a loan is repaid successfully within the term, TRU stakers who had staked YES are rewarded. If a loan defaults, TRU stakers who had staked NO are rewarded. The incorrect predictors of the outcome in both cases are penalized for incorrectly predicting the loan outcome.

### How much TRU would be distributed for participating in the credit prediction market?  <a id="how-much-tru-would-be-distributed-for-participating-in-the-credit-prediction-market"></a>

Out of the total TRU in circulation, 45% is currently allocated for distribution to TRU stakers, which would be distributed over a period of four years. This comes out to a total of 254,475,000 TRU.

This is how early participants of the protocol are rewarded. At any point in time, the amount of TRU which is available for distribution by this method would be called TRU remaining in distributor.

`TRU distribution factor = (TRU remaining in distributor) / (Total TRU allocated for distribution)`

The TRU distribution factor calculates the ratio of TRU, which would be available for distribution. Initially, before any loan application, the total TRU remaining in distributor is equal to the Total TRU allocated for distribution, making the TRU distribution factor equal to 1. Gradually the TRU distribution factor will become smaller.

`interest = (loan APY * term * principal)`

Loan APY is the interest rate at which the borrower has borrowed, term is the time period for which the borrower has borrowed, and principal is the amount borrowed by the borrower. The term is the time difference between the date at which the loan was withdrawn by the borrower and the date of repayment. This calculation assumes APY to be quoted as annualized values and a year to be equal to 365 days.

**Example**: For a loan \(principal = 1,000,000 TUSD, term = 30 days, APY = 12%\), interest would be equal to \(12% x 30/365 x 1,000,000 TUSD\) 9,863.013 TUSD.

`TRU Reward = (interest * TRU distribution factor * multiplier)`

For calculating the total TRU reward payable for a loan, TrueFi takes the product of interest associated with the loan, the TRU distribution factor and a multiplier. Currently the multiplier is set to 2.

**Example**: If TRU distribution factor is equal to 1, continuing with the above example the TRU rewards payable to TRU stakers would be \(1 x 9,863.013 TUSD x 2\) 19,726.026 TRU. Each staker gets rewarded based on the percentage of their TRU out of the total TRU that has been staked on that loan. The total TRU is taken into account for this purpose irrespective of the outcome of their prediction. 

**Example**: Consider a total of 1,200,000 TRU was staked on the loan, where 1,150,000 TRU was staked as YES and 50,000 TRU was staked as NO. If an individual had staked 10,000 TRU as YES the total TRU rewards payable to the individual by the end of the term would be \(\(10,000/1,200,000\) \* 19,726.026 TRU \) 164.38355 TRU. Even if the individual would have staked 10,000 TRU as NO the total TRU rewards payable to the individual would be the same as 164.38355 TRU.

TRU rewards are accrued for participating over time and can be claimed by TRU stakers after the loan principal has been withdrawn by the borrower. At any point of time, the percentage of TRU rewards that an individual can claim is proportional to the number of days passed since the loan principal has been withdrawn.

**Example**: Continuing with the above example, let’s assume that 10 days have passed since the loan principal was withdrawn, the total TRU reward which the individual would be able to redeem at the end of 10 days is equal to \(10 days/30 days x 164.38355 TRU\) 54.7945 TRU.

### How are payouts calculated for predicting the outcomes in the credit prediction market? <a id="how-are-payouts-calculated-for-predicting-the-outcomes-in-the-credit-prediction-market"></a>

The payouts for correctly predicting the outcome of a loan is paid by the stakers who had incorrectly predicted the outcome.

Stakers who incorrectly predict the outcome of the loan are penalized. Incorrect predictors lose a certain proportion of the TRU they had staked on the loan. The ratio of TRU that stakers lose is called the Loss factor.

`TRU lost for Incorrect prediction = Loss factor x TRU staked`

Initially, the Loss factor is set at 25%, which means an individual would lose 25% of the TRU they had staked for incorrectly predicting the outcome of the loan. The rest of the 75% can be claimed back by the staker to his/her wallet.

**Example**: If an individual had staked 10,000 TRU as YES on a loan and if it defaults, they would lose \(10,000 TRU x 25%\) 2,500 TRU. They can claim the remaining 7,500 TRU back into their wallet.

From the TRU that was lost by incorrect predictors, a portion of the TRU is burned. The ratio of TRU that is burned to total TRU that was lost by the incorrect predictors is called the Burn factor.

`TRU Burned = Burn factor x Loss factor x TRU staked`

Initially, the burn factor is set at 25%, which means that out of the total TRU lost by incorrect predictors, 25% of the TRU will be burned.

**Example**: If a loan had received a total of 1,200,000 TRU \(1,150,000 TRU as YES and 50,000 TRU as NO\) and the loan was paid back successfully within the loan term, the amount of TRU that would be burned is \(25% x 25% x 50,000\) 3,125 TRU.

The TRU payout that the stakers would receive for correctly predicting the loan’s outcome is the difference between the TRU lost by stakers who had incorrectly predicted the outcome of the loan and the TRU burned. And the payouts received by individuals for correctly predicting would be in proportion to their share of TRU out of the total TRU staked, which correctly predicted the outcome.

`TRU payout for correct predictors = TRU lost by incorrect predictors - TRU burned`

**Example**: If a loan had received a total of 1,200,000 TRU \(1,150,000 TRU as YES and 50,000 TRU as NO\) and the loan was paid back successfully within the loan term. TRU lost by incorrect predictors is equal to \(25% x 50,000\) 12,500 TRU. TRU burned is equal to \(25% x 25% x 50,000\) 3,125 TRU. And the TRU payout for correct predictors would be \(12,500 TRU - 3,125 TRU\) 9,375 TRU. So for every TRU, an individual had staked as YES they would receive \(3,125 TRU/ 1,150,000 TRU\) ~ 0.008 TRU.

### What kind of data will be available to stakers to help them make informed decisions?  <a id="what-kind-of-data-will-be-available-to-stakers-to-help-them-make-informed-decisions"></a>

At launch, the borrower's legal entity name and wallet address would be made available to the stakers. They would also be able to view the repayment history of every borrower and the performance of all the loans made out in the history of TrueFi on the Loans page. Based on this information stakers can do further analysis on how well the borrowers would perform in future loans and draw conclusions required to assist them in correctly predicting the outcomes of a new loan application.

Since TRU stakers are incentivized for correctly predicting the outcome of a loan, they can further devise systems and build mechanisms to gather whatever information is necessary to make the predictions of the credit prediction market more accurate over time.

### Can I stake against multiple loans at once? <a id="can-i-stake-against-multiple-loans-at-once"></a>

Yes, you can stake on multiple loans at once and take different position sizes and predict different outcomes. One thing to note, if you have staked TRU against a particular loan and the loan principal has been disbursed to the borrower, you will not be able to withdraw that TRU and use it to stake on other loan applications. However, you can stake the rest of your TRU balance on as many loan applications as you please.

### How are loans approved?

Loans are approved by the TrueFi lending pool based on TRU staked on the loans. To learn more click [here](pool.md#how-does-the-current-truefi-lending-pool-lend-or-approve-loan-applications). 

