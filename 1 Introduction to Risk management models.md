# Introduction to Risk management models

[TOC]

## Assignment

| **Assessment Task**                                          | **Weight** | Due Date    |
| ------------------------------------------------------------ | ---------- | ----------- |
| [Group Assignment- Part 1](https://vucollaborate.vu.edu.au/d2l/le/content/1372708/viewContent/7455899/View) | 15%        | Session 3   |
| [Class Test](https://vucollaborate.vu.edu.au/d2l/le/content/1372708/viewContent/7455900/View) | 15%        | Session 6   |
| [Group Assignment- Part 2](https://vucollaborate.vu.edu.au/d2l/le/content/1372708/viewContent/7455902/View) | 20%        | Session 9   |
| [Final Exam - Paper based](https://vucollaborate.vu.edu.au/d2l/le/content/1372708/viewContent/7455901/View) | 50%        | Exam period |

## Timetable

| Week | Session |
| ---- | ------- |
| 1    | 1, 2, 3 |
| 2    | 4, 5, 6 |
| 3    | 7, 8, 9 |
| 4    | 10, 11  |

## Teaching Staff Details

Dr Guneratne Wickremasinghe: Guneratne.Wickremasinghe@vu.edu.au

Unit Lecturer Professor Jing Zhongbo: zbjing@cufe.edu.cn 

## What is Risk?

- Investors face uncertainty ==relating to the profit or loss== from the investment, i.e. the future value of the return is uncertain (unknown). 
- The ==quantification of the uncertainty== is known as risk – the possibility of negative/positive return
- Risk relative to ==expectations==: The chance that the actual return on an investment will be different from the expected return is risk.

## Absolute, Relative and Conditional Risk

- **Absolute risk**: Portfolio should not lose more than 5% of its value in a year.
- **Relative risk**: Default risk of CCC rated bonds as compared to AAA rated bonds. 
- **Conditional risk**: Probability that a mutual fund will be down more than 8% if ASX200 is down more than 10%.

> **Absolute risk** of a disease is your risk of developing the disease over a time period.
>
> **Relative risk** is used to ==compare== the risk ==in two different groups== of people.

## Intrinsic Risk vs. Extrinsic Risk

- Intrinsic `固有的` Risk - Inherent uncertainty that we ==cannot reduce== despite the level of information.
- Extrinsic `外在的` Risk - Due to ==lack of information== or ==information asymmetry== (can be reduced).

Financial Risk Management is about ==managing intrinsic risk== and ==reducing extrinsic risk==.

## Type of Financial Risks

- Market risk
- Credit risk
- Liquidity risk
- Operational risk
- Business risk / Enterprise risk

### Market Risk

Changes in the value of investment (loss) due to the changes in market prices or rates.

#### Interest rate risk

The risk of a decline in earnings due to the **movements of Interest rate**

**Banks:** Most of the items of banks’ balance sheets generate revenues and costs are interest rate driven.  Since interest rates are unstable, so are earnings.

**Individual:** Any one who lends or borrows is subject to interest rate risk. The **lender** earning a variable rate has the risk of seeing **revenues reduced** by a **decline** in interest rate. The borrower paying a variable rate bears a **high costs** when **interest rates increases**. 

#### Equity price risk

Arises due to the volatility of the share prices.

**Systematic Risk**: Sensitivity of the share price to broad market factors

**Unsystematic risk**: Sensitivity of the stock price to unique factors of the 
entity

#### Foreign exchange risk

- **Return on foreign assets** is depend on the probable price change, dividend gains and the **change in the foreign exchange rate**.
- An adverse foreign exchange rate could reduce the return on foreign investment.
- The variability in return on security caused by currency fluctuations`波动` is called as the foreign exchange risk. 
- Exchange rate risk is sometime called “Currency Risk”.

### Credit Risk

Loss suffered by a party whereby the counterpart **fails to meet its financial obligations** to the party under the contract.

- Default Risk: Non-payment of interest or principal`本金`
- Sovereign`主权` Risk: Default by the government
- Bankruptcy Risk: Insolvency`破产`, insufficient`不足` collateral`抵押`
- Downgrade`降级` Risk: Lost credit worthiness

### Liquidity Risk

The lack of marketability of an investment that **cannot be bought or sold quickly** enough to prevent or minimize a loss 

- Funding liquidity risk 
- Trading liquidity risk

### Operational Risk

Risk arising from all aspects of business activities

- Legal risk
- Systems risk
- Model risk

## Enterprise Risk Management

- Overseeing all the above risks
- Prepare summary reports
- Assess overall business risk

### Main tasks of a financial risk manager

- Defining risk
- Monitoring risk
- Controlling risk
- Communicating risk

## Measures of Risk

- Shares: Standard Deviation, Beta, Value at Risk (VaR) 
- Bonds: Duration, convexity
- Options: Delta, Gamma, Vega, Theta

## Share

### What are Shares?

- A share represents the ownership.
- Two types of shares: Common and Preference.
- Depending on the type of share, share holders have the right to vote and have dividend.
- No guarantee on repayment of principle investment in case of liquidation like the debt holders. 
- High risk, high return

### Share issues

Shares can be issued through

- a public placement ( which include listing in a stock exchange and inviting general public to 
  participate the share issue) or
- a private placement (if it is not listed in a stock exchange).
- Share purchase plans
- Rights issues
- Bonus issues

### Type of Markets for Shares

**Primary market**: Issuing company receives the sale proceeds

**Secondary market**: A shareholder reveives the sale proceeds (buy a share from buy from stock exchange from another sharehold)

### Returns

Returns is the reward for undertaking investments

Measurement of historical Return is important to investors because: 

1. It is a measure of past performance 
2. Can help manage risk by estimating future returns.

#### Returns Measurement

$$
\text{Return for a share} =\dfrac{P_s-P_b+D}{P_b}
$$

where:

- $P_s$ = selling price
- $P_b$ = buying price
- $D$ = dividend

$$
\text{Return for the market}=\dfrac{I_t-I_{t-1}}{I_{t-1}}
$$

where: 

- $I_t$ = market index at time t
- $I_{t-1}$=market index at time t-1

##### Market model

$$
R_{it}=\alpha_i+\beta_iR_{mt}+\varepsilon_{it}
$$

where:

- $R_{it}$=return for share I for time t
- $\α_i$= intercept
- $\β_i$= beta coefficient for share i
- $R_{mt}$= return for market for time t
- $\varepsilon_{it}$ = residual

**Testing the significance of beta**

- Compare the p-value for the beta (slope of the market model)  from the Excel output with either 1% or 5%
- If the p-value for the beta is less than either 1% or 5%, the beta coefficient is statistically significant. 
