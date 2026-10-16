# Exponentially Weighted Moving Average (EWMA) VaR Calculation

1. A typical example of a moving average is the covariance formula:

$$\operatorname{COV}(X, Y) = \frac{1}{n} \sum_{i=1}^{n} (x_i - \mu_x)(y_i - \mu_y)$$

## Why weighed

- The Normal calculation method weighed every day the same, but usually past data matters less that more recent data, thus, we add coefficients to the day returns

$$\operatorname{COV}(X, Y) = \frac{1}{\left( \frac{1 - \lambda^n}{1 - \lambda} \right)} \sum_{i=1}^{n} \lambda^{i-1} (x_i - \mu_x)(y_i - \mu_y)
= \frac{1 - \lambda}{1 - \lambda^n} \sum_{i=1}^{n} \lambda^{i-1} (x_i - \mu_x)(y_i - \mu_y)
$$
with $0 < \lambda < 1$
