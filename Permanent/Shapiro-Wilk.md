---
alias: 
tags: 
title: Shapiro-Wilk
date created: 2023-09-13 13:04:56
date modified: 2023-09-13 21:21:41
---

# Shapiro-Wilk

Tests whether a data sample has a [[Gaussian distribution]].

## Assumptions

- Observations in each sample are independent and identically distributed (iid).

## Hypothesis Formulations

- H0: the sample has a Gaussian distribution.
- H1: the sample does not have a Gaussian distribution.

## Code Implementation

```python
from scipy.stats import shapiro

data = [0.873, 2.817, 0.121, -0.945, -0.055, -1.436, 0.360, -1.478, -1.637, -1.869]

stat, p = shapiro(data)

print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably Gaussian')
else:
	print('Probably not Gaussian')
```