# Session 10: Credit Risk

## Learning Object


- Credit risk 
- Bond pricing 
- Default risk and pricing 
- The probability of default

## Credit Risk

Credit Risk: It is the risk that one party in a financial transaction will  fail to pay the other party in that transaction.

## Bonds

Bond-holders (Investors) who hold the bond until the maturity, receive cash in the form of interest payments (coupon payments) during the bond’s life and, at maturity, cash on the repayment of the face value. 

Interest rate has two functions: 

1. It is the rate at which present sums can be converted to  equivalent future sum. 
2. It is the rate at which the promised future sum can be  converted to equivalent present values.  

### Bond Pricing

- A firm’s long-term debt obligation can be in the form of long-term notes or bond with a maturity period and date. 
- An investment in debt securities will offer regular periodic interest payments (Coupon) and the debt repayments (the face value) at the  maturity. 

$$
V_o=\sum^T_{t=1}\dfrac{c}{(1+R_t)^t}+\dfrac{N}{(1+R_T)^T}
$$

> 各期利息的贴现和 + 面值的贴现

where: 

- $V_0$ : Current market value of the asset 
- $c$ : Interest payment (often called coupon payment) at time t 
- $t$ : number periods to maturity 
- $N$ : Face value (principal repayment or notional amount) at maturity 
- $R_t$ : Annual discount rate 
- $T$ : Maturity (expiry) 

If the coupon payments are certain (no default probability), the appropriate discount rate will be equal to the *risk free rate*. 

> **Example**
>
> **Question**
>
> Linda Corp. issued 3-year bonds with a face value of \$100 each and a coupon rate of 10%. The cash flows to a bond holder will be interest (coupon) payment of \$10 per year for 3 years, followed by payment of \$100 at the end of third year. If the required rate of return is 10% per year, what would be the value of bonds? 
>
> **Answer**
>
> The value of the bond is given by 
> $$
> \begin{align}
> P_0 &= \$10/1.1 +\$10/(1.1)^2 +\$10/(1.1)^3 +  
> \$100/(1.1)^3 \\[1ex]
> &= \$9.09 + \$8.264 + \$7.513 + \$75.131 \\[1ex]
> &= \$100.00
> \end{align}
> $$
>
> The market value of the Bond is \$100
>
> ---
>
> If the market rates change after the bond has been issued, it will affect the attractiveness of the bond to potential investors. 
>
> - If market interest rates decrease, the bond will become more attractive and the price of existing bond will increase. 
>
>   - Required rate of return falls to 8% per year 
>     $$
>     \begin{align}
>     P_0 &= $10/1.08 +$10/(1.08)^2 +$10/(1.08)^3 +  
>     $100/(1.08)^3 \\[1ex]
>     &= $105.15 
>                     
>     \end{align}
>     $$
>
> - If market interest rates increase, the bond will be less attractive and the price of existing bond will fall. 
>
>   - Required rate of return rises from 10% to 12% per year. 
>     $$
>     \begin{align}
>     P_0 &= \$10/1.12 +\$10/(1.12)^2 +\$10/(1.12)^3 +  
>     \$100/(1.12)^3 \\[1ex]
>     &= \$95.20
>     \end{align}
>     $$

## Default and Recovery


- Zero coupon bond - pays no coupon payments and typically sells at a discount. 

    - A risk-free zero coupon bond with a notional of \$100, maturity of 1 year, risk-free rate of 5%, will sell at \$95.24. 
      $$
      V_t=\dfrac{$100}{1.05}=$95.24
      $$

- Consider the same zero coupon bond but now there is a 20% chance of default. In the event of default, bondholder receives no payment. 

    - For a risk-neutral investor, the present value of bond will be the weighted average of two scenarios: 
      $$
      V_t=20\%\cdot\dfrac{$0}{1.05}+80\%\dfrac{$100}{1.05}=$76.19
      $$

- In practice, the bondholder usually ==receives some fraction of the anticipated payments in the event of default==. 


      - The loss, as a percentage of anticipated value is called loss given default (LGD)`违约损失率`. 
    
      - Alternatively, the amount paid as a percentage of anticipated value is the recovery rate (RR).
        $$
        \mathit{LGD} = 1- \textrm{Recovery rate}
        $$


> **Example**
>
> Consider the same zero-coupon bond from the previous example. If recovery rate is 40% instead of 0%, what is the present value?
>
> **Solution**
> $$
> V_t=20\%\cdot\dfrac{$40}{1.05}+80\%\cdot\dfrac{$100}{1.05}=$83.81
> $$

### Yield to Maturity (YTM)


- Bonds with different coupon rates or face value can be difficult to compare. 

- Yield or Yield to Maturity (YTM) can be used to **compare the bonds**. 

- YTM is the ==internal rate of return assuming all payments are made==. 

- It is the yield or total return that a bondholder earns by holding the bond till maturity. 

- YTM is the constant discount rate that solves the bond pricing equation:
  $$
  V_0=\sum_{t=1}^T\dfrac{c}{(1+Y)^t}+\dfrac{N}{(1+Y)^T}
  $$
  where: 

  - $Y$: YTM
  - $N$: notional`名义` amount
  - $c$: coupon payments

- In case there are **no coupon payments**, yield calculation is simple:
  $$
  Y=\left(\dfrac{N}{V_0}\right)^{1/T}-1
  $$

- For a **one-year zero coupon bond** with ==probability of default D==, a ==loss given default L==, and discount rate R, the yield (after mathematical derivations) is:
  $$
  Y=\dfrac{R+DL}{1-DL}
  $$
  If probability of default D or loss given default L is zero, the yield or YTM will be equal to the discount rate.

> **Example**
>
> Using the previous example of a one-year zero-coupon bond, assuming the probability of default as 20% and recovery rate of 40%, what is the yield?
>
> **Solution**
> $$
> Y=\dfrac{5\%+20\%\times60\%}{1-20\%\times60\%}=19.32\%
> $$
> Yield of 19.32% is higher than the discount rate of 5%
>
> Why?

### Quantitative Approaches: The Merton Model of Default

Merton’s great insight was to realize that we can view the equity holders as having a **call option** on the value of the firm.
$$
S = \max(\mathit{VE} − B, 0)
$$
Where

- $S$ = value of equity at the end of the year 
- $\mathit{VE}$ = enterprise value 
- $B$ = Strike price 
- Enterprise value = Value of equity plus value of bonds

**Distance to default ($\Delta$)**
$$
\Delta=\dfrac{
-\ln(\dfrac{V}{B})-(r-\dfrac{\sigma_V^2}{2})\cdot T
}{
\sigma_V\sqrt{T}
}
=-d_2
$$

where: 

- $\sigma_V$: implied volatility of the enterprise value
- $(r-\dfrac{\sigma_V^2}{2})\cdot T$: expected risk neutral drift of the enterprise value
- $T$: time to maturity
- $r$: risk-free rate of return 

> **Example**
>
> You are asked to calculate the probability of default over one year for a company with \$100 of debt and a current market capitalization of \$172. The implied volatility of the enterprise value is 40% and the risk-free rate is 8.00%.
> $$
> \begin{align}
> \Delta=\dfrac{
> -\ln(\dfrac{$172+$100}{$100})-(8\%-\dfrac{{(40\%)}^2}{2})\times 1
> }{
> 40\%\sqrt{1}
> }
> =-2.5
> \end{align}
> $$
>
> - The distance to default ($\Delta$) is −2.5 standard deviations. Using a spreadsheet or other application to find the corresponding probability from the normal cumulative distribution 
> - function, we have $P[D] = N(−2.5) = 0.62\%$ (use `=normsdist(-2.5)` in Excel to get P(D))

## Portfolio Credit Risk

- Probability of any k bonds defaulting
  $$
  P[K=k]=\begin{pmatrix} n \\ k\end{pmatrix}p^k(1-p)^{(n-k)}
  $$

  - $P[K=k]$ = probability of k bonds defaulting out of n bonds
  - $P_k$ = probability of default
  - $\begin{pmatrix} n \\ k\end{pmatrix}=\dfrac{n!}{k!(n-k)!}$: if we have n bonds number of ways in which k bonds can default (number of combinations) (排列数的另一种写法，即：$C_{n}^{k}$)

> **Example**
>
> Assume we have four bonds, each with a 10% probability of defaulting over the next year. The event of default for any given bond is independent of the other bonds defaulting. What is the probability that zero, one, two, three, or all of the bonds default? What is the mean number of defaults? The standard deviation?
>
> **Answer**
>
> We can calculate the probability of each possible outcome as follows:
>
> | No. of Defaults | $\begin{pmatrix} n \\ k\end{pmatrix}$ | $p^k(1-p)^{n-k}$ | Probability |
> | --------------- | ------------------------------------- | ---------------- | ----------- |
> | 0               | 1                                     | 65.61%           | 65.61%      |
> | 1               | 4                                     | 7.29%            | 29.16%      |
> | 2               | 6                                     | 0.81%            | 4.86%       |
> | 3               | 4                                     | 0.09%            | 0.36%       |
> | 4               | 1                                     | 0.01%            | 0.01%       |
>
> - Mean number of defaults $= np = 4.10 = 0.40 $
> - Variance of defaults $= np(1-p) = 4\times.10\%(1-.10) =  0.36 $
> - Standard deviation of defaults $= 0.60$
