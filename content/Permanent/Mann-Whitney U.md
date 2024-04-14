---
alias: 
tags: 
title: Mann-Whitney U Test
date created: 2023-09-13 13:37:21
date modified: 2023-09-13 13:37:53
---

# Mann-Whitney U Test

Tests whether the distributions of two independent samples are equal or not.

## Assumptions

- Observations in each sample are independent and identically distributed (iid).
- Observations in each sample can be ranked.

## Hypothesis Formulation

- H0: the distributions of both samples are equal.
- H1: the distributions of both samples are not equal.

## Code Implementation

```python
# Example of the Mann-Whitney U Test
from scipy.stats import mannwhitneyu
data1 = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]
data2 = [1.142, -0.432, -0.938, -0.729, -0.846, -0.157, 0.500, 1.183, -1.075, -0.169]
stat, p = mannwhitneyu(data1, data2)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably the same distribution')
else:
	print('Probably different distributions')
```