# Pool

### How do I lend with TrueFi? <a id="what-are-lending-pools"></a>

{% embed url="https://www.youtube.com/watch?v=VV8QUU9PCFQ&feature=youtu.be" %}

Lenders can lend their stablecoins to the TrueFi lending pools that use predefined strategies to lend to creditworthy borrowers. Any stablecoins that are not being actively loaned out may be used to provide liquidity in audited, stable, and high yield DeFi protocols \(such as Aave or Curve.fi\).

Initially, TrueFi will have a single lending pool created by TrustToken, Inc.. This pool will act as a pilot for future pools, and will only lend to a whitelist of trusted borrowers, and any excess capital that is not actively loaned out may be deployed in a DeFi protocol.

Lenders who lend to the Truefi lending pool would receive TrueFi lending pool tokens \(referred to as TFI - LP tokens\) which represents their proportion of lent capital in the TrueFi lending pool.

### How does TrueFi generate yield? <a id="how-does-truefi-achieve-its-apys"></a>

TrueFi lending pools can offer an APY or return that is at least as high as the highest stable rate available in DeFi today by transferring idle capital to existing DeFi protocols to earn a return. TrueFi will only move capital out of the DeFi protocols and make loans when the borrower’s proposed rate exceeds the rate offered by the selected DeFi protocol. For the current TrueFi lending pool the minimum interest rate for a loan application is 10%, so all loan applications will have APRs higher than or equal to this rate.

In comparison to traditional finance, institutions have additional costs like high establishment costs and shareholders who demand higher returns on their capital. In the case of TrueFi, many of these costs will be eliminated by moving this type of lending to DeFi.

Additionally, uncollateralized lending inherently has a higher risk profile and the market demands a higher return.

### What are Lending Pool \(TFI - LP\) tokens?  <a id="what-are-lending-pool-tfi-lp-tokens"></a>

Lending Pool tokens are tradable ERC-20 tokens that represent a lender’s proportional representation in the pool. In the beginning, when no loans have been disbursed by the TrueFi lending pool, for every TUSD deposited, depositors will get one TFI - LP token for every TUSD lent to the pool. As the pool starts earning yields and lending to borrowers, the value of the pool tokens may increase or decrease depending on the yields earned by the pool. Anyone who comes in later to lend to the pool will be getting a new value for the pool. The value of the pool would be the present value of all its tokens \(stablecoins, altcoins and loan tokens\).

### What are loan tokens?  <a id="what-are-loan-tokens"></a>

Loan tokens are non-tradable ERC-20 tokens which represent the lender’s proportional representation in a loan that is issued from the Lending Pool. Each loan issued from the Lending Pool will create a unique loan token used to track the present value of each loan. Loan tokens form an important building block of TrueFi, as they can operate independently from the TrueFi lending pools. Tokenized loans open up opportunities for calculating and tracking the value to the individual loans within the Lending Pool. TrueFi will initially not allow for the transfer of Loan tokens and will not create a secondary market for loan tokens. It is important to note that all Loan tokens are unique and can be tracked on the [Loans](https://app.truefi.io/loans) page of the TrueFi website.

Creating a Loan token requires a borrower’s wallet address, principal amount, term, and interest rate or APR associated with a loan. When a loan is approved by the pool, loan tokens are minted by funding the loan token contract with the principal amount, and the minted loan tokens represent a share in the total amount payable at the end of the term which is the sum of principal and interest.

Loan tokens are minted at a discounted rate, meaning for every unit of principal added to the loan token contract, the number of tokens that are minted is equal to the sum of a unit of stablecoin and the interest amount applicable to that unit of stablecoin. Once a loan is funded, the borrower can call a function which allows them to borrow the funds from the smart contract. At the end of the term, once the borrower pays back the loan, loan token holders can exchange their loan tokens for an equivalent number of stablecoins.

`Number of loan tokens minted = principal + interest`

**Example**: When a loan \(principal = 1,000,000 TUSD, term = 30 days, APR = 12%\) is approved, \(1,000,000 + 1,000,000 x 12% x 30/365 \) 1,009,863.013 loan tokens would be minted. And at the end of the loan term if the borrower repays the entire loan amount along with interest lenders or the lending pool can exchange 1 loan token for 1 TUSD.

### What is the value of a loan token at any point of time? <a id="what-is-the-value-of-a-loan-token-at-any-point-of-time"></a>

The theoretical present value of a loan token is calculated by assuming that the loan would be repaid in full by the end of the loan term. Understandably, the loan token value at the end of the loan term is equal to a unit of the underlying stablecoin. This valuation of the loan token is used by the Lending Pool smart contract in calculating the value of TFI - LP tokens:

`Value of loan tokens after time t (time since minted) = principal + (t / term ) x interest`

`Value of a single loan token after time t = Value of loan tokens after time t / Number of loan tokens minted`

`Value of a single loan token after time t = (principal + (t / term ) x interest)/(principal + interest)`

**Example**: When a loan \(principal = 1,000,000 TUSD, term = 30 days, APR = 12%\) is approved, \(1,000,000 + 1,000,000 x 12% x 30/365 \) 1,009,863.013 loan tokens would be minted. The value of a single loan token at the end of n days where n is less than or equal to 30 can be given as \(1,000,000 + \(n/30\) x 9,863.013\) / \(1,000,000 + 9,863.013\) TUSD.

![](https://lh6.googleusercontent.com/9Cxq4WAOkc_onJ0iibik1y6njflxEVPMZzN8KQEL5Ro2Ppk2ysoAENSaT_3xBhXlqVjd0ZFlLsBaNB1_rOS688iJWbw2N_Vn5wCvSQeCL5oYGlvBw6lSK79BT6DomMAXHtlpN-m5)

### How is the theoretical price of the TrueFi lending pool \(TFI - LP\) token calculated? <a id="how-is-the-theoretical-price-of-the-truefi-lending-pool-tfi-lp-token-calculated"></a>

The TrueFi lending pool’s theoretical value is calculated by adding the present value of all loan tokens, stablecoins and altcoins \(like CRV\) present in the pool. The value of a TFI - LP token would be the pool’s theoretical value divided by the number of TFI - LP tokens. Initially the pool would issue a unit of TFI - LP for every unit of stablecoin lent to the pool.

**Example**: Lender\_1 lends 2 Mn TUSD to the pool and receives 2 Mn TFI - LP tokens on day 1. The value of the pool at the end of day 1 is 2 Mn TUSD.

Borrower\_1 withdraws a loan of 1 Mn TUSD at the end of day 10 for 30 days at an APR of 12%. The value of the pool at the end of Day 10 is still 2 Mn TUSD.

At this point, right at the beginning of day 11, the pool has 1 Mn TUSD and 1,009,863.01 loan tokens, but the value of the pool is still equal to 2 Mn TUSD.

At the end of day 25, 15 days have passed since the loan was withdrawn by Borrower\_1. At this point the value of the loan tokens have changed. 

The value of the 1,009,863.01 loan tokens at the end of Day 25 would be \(1,000,000 + \(15/30\)x9,863.01\) 1,004,931.50 TUSD. 

The total value of the pool would be equal to \(1,004,931.50 + 1,000,000\) 2,004,931.50 TUSD which is the sum of the value of stablecoins \(1,000,000 TUSD\) and loan tokens \(1,004,931.50 TUSD\). Number of pool tokens in circulation is still equal to 2 Mn, and therefore the price of a TFI - LP token would be equal to \(2,004,931.50 TUSD / 2,000,000\) 1.002465 TUSD.

Just before the end of day 40 the value of loan tokens would be almost equal to 1,009,863.01 TUSD and therefore the value of the pool would be 2,009,863.01. Price of TFI - LP tokens would almost be equal to \(2,009,863.01 TUSD / 2,000,000\) 1.004931 TUSD.

### Why is there a difference between the calculated TFI - LP price and its price on Uniswap? <a id="why-is-there-a-difference-between-the-calculated-tfi-lp-price-and-its-price-on-uniswap"></a>

The TFI - LP price is calculated based on a lot of assumptions, one of the key assumptions being that the loans will be repaid successfully within the term. Other market participants may have a different sentiment regarding the nature of pool tokens and may or may not agree with the price calculated by the TrueFi lending pool. There are several market factors that may govern the price of TFI - LP tokens and the TrueFi platform does not have any control over them.

However, you can always exit the pool by withdrawing your share of the loan tokens that represent still outstanding loans, hold on to the loan tokens and redeem them for TUSD upon completion of the loan terms, respectively. 

### How many TFI - LP tokens will I get for lending to the TrueFi lending pool? <a id="how-many-tfi-lp-tokens-will-i-get-for-lending-to-the-truefi-lending-pool"></a>

For lending a certain amount of stablecoins to the TrueFi lending pool, the number of TFI - LP tokens you get will have the same monetary value as the value of stablecoins you have lent. The value of TFI - LP tokens is calculated in the same way as described above.

Number of TFI - LP tokens you get

= Deposit amount in TUSD x \(number of outstanding pool tokens / current estimated value of pool\)

**Example**: Continuing with the previous example, Lender\_1 lends 2 Mn TUSD to the pool and receives 1 Mn TFI - LP tokens on day 1. At this point and until any loans are withdrawn from the pool, for every unit of TUSD a lender lends to the pool they would get a unit of TFI - LP token.

Borrower\_1 withdraws a loan of 1 Mn TUSD at the end of day 10 for 30 days at an APR of 12%. The value of the pool at the end of Day 10 is still 2 Mn TUSD.

At this point right at the beginning of day 11 if someone wants to lend TUSD they would still be able to get almost the same amount of TFI - LP tokens. But as the loan progresses the value of the pool gradually increases due to the increase in value of the loan tokens.

At the end of day 25, 15 days have passed since the loan was withdrawn by Borrower\_1. The value of the loan tokens held by the pool is 1,004,931.50 TUSD and the value of the pool is 2,004,931.50 TUSD. The number of pool tokens in circulation is still equal to 2 Mn, and the price of a TFI - LP token is 1.002465 TUSD.

At this point if a lender wants to lend TUSD to the pool, the number of TFI - LP tokens for every unit of TUSD that the lender would receive would be equal to \(1 x 2,000,000/ 2,004,931.5\) 0.9975 TFI - LP tokens. If a lender were to lend 2,004,931.5 TUSD he/she would get \(2,004,931.5 TUSD x \(2,000,000 / 2,004,931.50 TUSD\)\) 2 Mn TFI - LP tokens.

Please note that the additional influx of stablecoins to the lending pool does not erode any value from the existing lenders since the price of the TFI - LP token is still equal to 1.002465 and they still hold the same number of tokens as they had previously. New value of the pool is equal to the sum of the old value, and the value of new stablecoins added, which is \(2,004,931.50 TUSD + 2,004,931.50 TUSD\) 4,009,863 TUSD. Number of pool tokens in circulation is equal to the sum of old tokens and new tokens received which is \(2,000,000 + 2,000,000\) 4 Mn TFI - LP tokens. This makes the price of a TFI - LP token same as \(4,009,863 / 4,000,000\) 1.002465 TUSD.

#### Are there any fees for lending to the Lending Pools?

No, there are no fees for lending to the lending pools as a lender.

### How can I exit the lending pools? <a id="how-can-i-exit-the-lending-pools"></a>

You can exchange your TFI - LP tokens for a proportionate share of all tokens present in the pool. You can view the tokens held by the pool and your share of the token holdings in the Pool page.

While exercising this option, you must keep in mind that the loan tokens you withdraw from the pool are non-tradable and non-transferable and can only be held by you in your wallet. You can redeem the loan tokens for an equivalent amount of TUSD after the completion of the respective loan terms.

You can also exit the pool by selling your TFI - LP tokens to the TrueFi Lending Pool for TUSD if there is enough TUSD in the pool to support the transaction. This is also called liquid exit. 

### **What is Liquid Exit?**

**‌**Liquid exit addresses a key community request which is the ability to exit the TrueFi Lending Pool directly into TUSD. With Liquid Exit, the Lending Pool will act as a liquidity provider and accept TFI - LP tokens in exchange for TUSD. The pool will allow TFI - LP token holders to redeem their tokens for TUSD for an exit fee.

The exit fee is inversely proportional to the amount of available TUSD in the pool. For example, when there is a large amount of TUSD in the pool, the fee is low. When there is a small amount of TUSD in the pool, the fee is high. This fee is earned by the pool for the existing TFI - LP token holders.

The exit fee charged to you for an exit would be made available to you in the UI. If you feel that the fee charged is too high then you can wait till the pool is more liquid and try again later. ****

![](https://lh5.googleusercontent.com/0sR85-5paw_9Jo0yI3DgzHT8Yr22gWnyg9z_ILyfj4mESUTgQ9xHRAo2P0pN3XfR1sLxj3qwR2Es40uDrPL4ieOXB1OE_ldw0EwU7zuXBkLFAWDX1fKLsBKTemog13lg2EoBx1bs)

**‌**There are two situations in which the pool will not let you withdraw via Liquid Exit:

1\) If there is no TUSD in the lending pool and no TUSD deployed in Curve.

2\) If the pool needs to liquidate its position in Curve and will incur a loss of more than 10 basis points.

### What are the risks involved in lending to the TrueFi lending pool? <a id="what-are-the-risks-involved-in-lending-to-the-truefi-lending-pool"></a>

While borrowers are usually willing to pay higher rates for uncollateralized loans, these higher yields do not come without risks. Compared with collateralized lending, uncollateralized lending has two major risks:

* Potentially increased risk of loss: Protocols that require collateral are protected by that collateral in case of default. While this allows such platforms to be less selective in approving loans, uncollateralized loans come with a much higher standard of trust that must be met by a borrower. In case of default on an uncollateralized loan, a delinquent borrower will have been assessed for creditworthiness before the loan was made and will face both reputational damage and legal action.
* Potentially lower liquidity: While instant withdrawals are becoming a norm for new protocols, uncollateralized lending may not offer the same flexibility. Most borrowers for uncollateralized loans are interested in fixed-rate, fixed-term loans for predictable repayment. This means lenders who fund such loans need to be comfortable locking up their assets for the duration of the loan. TrueFi offers an alternative: the ability to withdraw their proportion of the pool tokens which would consist of stablecoins like TUSD and loan tokens that you hold to maturity. You can redeem the loan tokens for TUSD at the end of loan terms.

### Who is responsible for taking legal actions against delinquent borrowers? <a id="who-is-responsible-for-taking-legal-actions-against-delinquent-borrowers"></a>

Initially, TrustToken Inc. will be responsible for pursuing legal action against a delinquent borrower In the future, this responsibility may be transferred to a non-profit organization.

### How can lenders or TFI - LP token holders farm TRU?  <a id="how-can-lenders-or-tfi-lp-token-holders-farm-tru"></a>

TFI - LP token holders or lenders can farm TRU by staking their TFI - LP tokens on the [Farm](https://app.truefi.io/farm) page. 

### How can individual loan tokens be exchanged back for TUSD post maturity of the loans?  <a id="how-can-individual-loan-tokens-be-exchanged-back-for-tusd-post-maturity-of-the-loans"></a>

You can redeem individual loan tokens for TUSD on the TrueFi app. Please visit the page for the loan token and you should be able to see a Redeem button if you are connected with the wallet which holds the loan tokens. 

