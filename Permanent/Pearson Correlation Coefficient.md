---
alias: 
tags: 
title: Pearson’s Correlation Coefficient
date created: 2023-09-13 13:12:11
date modified: 2023-09-13 13:12:43
---

# Pearson’s Correlation Coefficient

Tests whether two samples have a linear relationship.

## Assumptions

- Observations in each sample are independent and identically distributed (iid).
- Observations in each sample are normally distributed.
- Observations in each sample have the same variance.

## Hypothesis Formulation

- H0: the two samples are independent.
- H1: there is a dependency between the samples.

## Code Implementation

```python
# Example of the Pearson's Correlation test
from scipy.stats import pearsonr
data1 = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]
data2 = [0.353, 3.517, 0.125, -7.545, -0.555, -1.536, 3.350, -1.578, -3.537, -1.579]
stat, p = pearsonr(data1, data2)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably independent')
else:
	print('Probably dependent')
```