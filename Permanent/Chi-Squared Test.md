---
alias: 
tags: 
title: Chi-Squared Test
date created: 2023-09-13 13:19:09
date modified: 2023-09-13 13:19:46
---

# Chi-Squared Test

Tests whether two categorical variables are related or independent.

## Assumptions

- Observations used in the calculation of the contingency table are independent.
- 25 or more examples in each cell of the contingency table.

## Hypothesis Formulation

- H0: the two samples are independent.
- H1: there is a dependency between the samples.

```python
# Example of the Chi-Squared Test
from scipy.stats import chi2_contingency
table = [[10, 20, 30],[6,  9,  17]]
stat, p, dof, expected = chi2_contingency(table)
print('stat=%.3f, p=%.3f' % (stat, p))
if p > 0.05:
	print('Probably independent')
else:
	print('Probably dependent')
```