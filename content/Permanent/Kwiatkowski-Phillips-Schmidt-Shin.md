---
alias: 
tags: 
title: Kwiatkowski-Phillips-Schmidt-Shin
date created: 2023-09-13 13:21:15
date modified: 2023-09-13 13:34:20
---

# Kwiatkowski-Phillips-Schmidt-Shin

Tests whether a time series is trend stationary or not.

## Assumptions

- Observations in are temporally ordered.

## Hypothesis Formulation

- H0: the time series is trend-stationary.
- H1: the time series is not trend-stationary.

## Code Implementation

```python
# Example of the Kwiatkowski-Phillips-Schmidt-Shin test
from statsmodels.tsa.stattools import kpss
data = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
stat, p, lags, crit = kpss(data)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably Stationary')
else:
	print('Probably not Stationary')
```