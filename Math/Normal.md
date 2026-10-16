# Parametric VaR estimation

## What is VaR (Value at Risk)
- Var is the the biggest amount of money you can lose while staying in the confidence bound (usually 95% or 99%)
- For example: If a portfolio has a VaR of 1 million at 99%. It means that there is a 1% chance that the portfolio loses more that 1 million.

## Normal Distribution
- Assumption: 1 day return are assumed to be normally distibuted.
It consists in finding the parameters of the normal distribution, we need the mean, and one of the two other parameters (2 out of 3) :
### 1. The mean $\mu$:
- It determines the position of the bell on the x-axis, the peak of the bell curve
- mean, mode and median are all equal

### 2. Standart Deviation $\sigma$: 
- Measures the spread, dispersion
- Larger $\sigma$ create a wider bell

### 3. Variance $\sigma^2$
- square of the $\sigma$
- determines the scale of the bell

## Normal VaR Calculation
- let $\Sigma$ be the covariance matrix of the portfolio
Then $\sigma_{portfolio}=\sqrt{v\Sigma v'}$ with $v=<v_1, ..., v_n>$ being the vector of dollar values invested in each financial asset
#### Correlations are easier to work with, hence we decompose the covariance matrix $\Sigma$:
-  correlations R and standard deviation $\sigma=<\sigma _1, ..., \sigma _n>$
- This gives: $\sigma_{\text{portfolio}} = \sqrt{\sigma_v R \sigma_v'}$, where $\sigma_v = (v_1\sigma_1,\, v_2\sigma_2,\, \ldots,\, v_n\sigma_n)$.
