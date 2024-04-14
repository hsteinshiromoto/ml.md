---
alias: 
tags: 
title: Augmented Dickey-Fuller
date created: 2023-09-13 13:20:30
date modified: 2023-09-13 13:32:17
---

# Augmented Dickey-Fuller

Tests whether a time series has a unit root, e.g. has a trend or more generally is autoregressive.

## Assumptions

- Observations in are temporally ordered.

## Hypothesis Formulation

- H0: a unit root is present (series is non-stationary).
- H1: a unit root is not present (series is stationary).

## Code Implementation

```python
# Example of the Augmented Dickey-Fuller unit root test
from statsmodels.tsa.stattools import adfuller
data = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
stat, p, lags, obs, crit, t = adfuller(data)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably not Stationary')
else:
	print('Probably Stationary')
```