---
alias: 
tags: 
title: D’Agostino’s $K^2$ Test
date created: 2023-09-13 13:07:53
date modified: 2023-09-13 13:08:37
---

# D’Agostino’s $K^2$ Test

Tests whether a data sample has a Gaussian distribution.

## Assumptions

- Observations in each sample are independent and identically distributed (iid).

## Hypothesis Formulation

- H0: the sample has a Gaussian distribution.
- H1: the sample does not have a Gaussian distribution.

## Code Implementation

```python
# Example of the D'Agostino's K^2 Normality Test
from scipy.stats import normaltest
data = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]
stat, p = normaltest(data)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably Gaussian')
else:
	print('Probably not Gaussian')
```

## References