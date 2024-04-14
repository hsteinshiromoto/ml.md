---
alias: 
tags: 
title: Paired Student’s T-test
date created: 2023-09-13 13:34:36
date modified: 2023-09-13 13:35:15
---

# Paired Student’s T-test

Tests whether the means of two paired samples are significantly different.

## Assumptions

- Observations in each sample are independent and identically distributed (iid).
- Observations in each sample are normally distributed.
- Observations in each sample have the same variance.
- Observations across each sample are paired.

## Hypothesis Formulation

- H0: the means of the samples are equal.
- H1: the means of the samples are unequal.

## Code Implementation

```python
# Example of the Paired Student's t-test
from scipy.stats import ttest_rel
data1 = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]
data2 = [1.142, -0.432, -0.938, -0.729, -0.846, -0.157, 0.500, 1.183, -1.075, -0.169]
stat, p = ttest_rel(data1, data2)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably the same distribution')
else:
	print('Probably different distributions')
```