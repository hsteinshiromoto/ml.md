---
alias: 
tags: 
title: Anderson-Darling Test
date created: 2023-09-13 13:10:30
date modified: 2023-09-13 13:11:09
---

# Anderson-Darling Test

Tests whether a data sample has a Gaussian distribution.

## Assumptions

- Observations in each sample are independent and identically distributed (iid).

## Hypothesis Formulation

- H0: the sample has a Gaussian distribution.
- H1: the sample does not have a Gaussian distribution.

```python
# Example of the Anderson-Darling Normality Test
from scipy.stats import anderson
data = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]
result = anderson(data)
print('stat=%.3f' % (result.statistic))
for i in range(len(result.critical_values)):
	sl, cv = result.significance_level[i], result.critical_values[i]
	if result.statistic < cv:
		print('Probably Gaussian at the %.1f%% level' % (sl))
	else:
		print('Probably not Gaussian at the %.1f%% level' % (sl))
```