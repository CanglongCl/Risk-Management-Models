# Session 6 Forecasting Volatility 


- Importance of volatility 
- ARCH Modelling 
- Exponentially Weighted Moving Average (EWMA) 
- GARCH Modelling

## Importance of Forecasting Volatility

Accurate forecasting of future volatility and correlations of  financial asset returns is essential for: 
1. Derivatives pricing 
2. Optimal asset allocation 
3. Portfolio risk management 
4. Dynamic hedging, and  
5. Value-at-Risk models (as an input)

## Models of changing volatility 

1. Exponentially`几何级数` weighted moving average (EWMA) model  
2. Autoregressive conditional heteroscedasticity (ARCH)  model 
3. Generalized autoregressive conditional heteroscedasticity  (GARCH) model 

Define:

- $\sigma_n$: the volatility of a market variable on day n.
- $σ_n^ 2$: the variance rate
- $u_i$: return during day i where $u_i=\dfrac{S_i-S_{i-1}}{S_{i-1}}$

Unbiased estimate of the variance rate per day, $σ_n^2$, using the most recent m observation on the $u_i$ is
$$
\sigma_n^2=\dfrac{1}{m-1}\sum^m_{i=1}(\mu_{n-i}-\overline\mu)^2
$$
Where $\overline\mu=\dfrac1m\sum_{i=1}^m\mu_{n-i}=0$

**Changing Volatilities Calculation**
$$
\sigma_n^2=\dfrac{1}{m}\sum^m_{i=1}\mu_{n-i}^2
$$
**Weighting Scheme**

To monitor the current level of volatility, it is appropriate to give more weight to recent data
$$
\sigma_n^2=\sum\alpha_iu_{n-i}^2
$$
where

- $\alpha$: the amount of weight given to observation i days ago

**Long-Run Average Volatility**
$$
\sigma_n^2=\gamma V+\sum_{i=1}^m\alpha_i\mu_{n-i}^2
$$
Where 

- $V$ is the long-run volatility and 
- $\gamma$ is the weight assigned to $V$.
- $\gamma+\sum\alpha_i=1$

### ARCH(m) Model

This was first suggested by Engle to capture the **serial correlation** of volatility, Engle (1982) proposed the class of Autoregressive Conditionally Heteroskedastic, or ARCH, models
$$
\sigma_n^2=\omega+\sum_{i=1}^m\alpha_i\mu^2_{n-i}
$$
Where: 

- $\omega=\gamma V$

The EWMA approach is designed to track changes in the volatility. 

Simple formula for updating volatility estimates is:
$$
\sigma_n^2=\lambda\sigma_{n-1}^2+(1-\lambda)\mu_{n-1}^2
$$
where

- $\lambda$ : a constant:  zero <  λ <  1
- $σ_n$ : Volatility for day n
- $σ_{n-1}$ : Volatility for day n-1 
- $u_{n-1}$ : Change in the market variable

#### EWMA Model - Advantages


- The EWMA approach has the attractive feature that relatively little data need to be stored. 
- At any given time, we need to remember only the current estimate of the variance rate and the most recent observation on the value of the market variable. 
- The value of λ governs how responsive the estimate of the daily volatility is to the most recent observations on the $u_i^2$.

### GARCH Model

GARCH Model is used to forecast the ***changing Volatility***

GARCH (p,q) model is given by
$$
\sigma_n^2=\gamma V+\sum\alpha_i\mu_{n-i}^2+\sum\beta_i\sigma_{n-j}^2
$$
where: 

- $γ$ is the weight assigned to $V$ (The long-term Variance)
- $α$ is the weight assigned to $u_{n-1}^2$
- $β$ is the weight assigned to $σ_{n-j}^2$ 

Setting $ω= γV$, it can also written
$$
\sigma_n^2=\omega+\sum\alpha_i\mu_{n-i}^2+\sum\beta_i\sigma_{n-j}^2
$$
