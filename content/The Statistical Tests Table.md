---
alias: 
tags: 
title: The Statistical Tests Table
date created: 2023-09-13 10:26:59
date modified: 2023-09-13 13:04:41
---

# The Statistical Tests Table

| Test Name | H$_0$ | Data Type | Is Parametric | Number of Groups |
|:----------|:-|:----------|:--------------|:-----------------|
| [[Shapiro-Wilk]] | The sample has not Gaussian distribution | Numerical | Y | 1                 |
| [[DAgostino]] | The sample has not Gaussian distribution | Numerical | Y | 1
| [[Anderson-Darling]] | The sample has not Gaussian distribution| Numerical | Y | 1 |
| [[Pearson Correlation Coefficient]] | The groups are not correlated | Numerical | Y | 2 |
| [[Spearman Rank Correlation]] | The groups are not correlated | Categorical | N | 2 |
| [[Kendall’s Rank Correlation]] | The groups are not correlated | Categorical | N | 2 |
| [[Chi-Squared Test]] | The groups are not correlated | Numerical | N | 2+ |
| [[Augmented Dickey-Fuller]] | Time series is not autoregressive | Numerical | Y | 1 |
| [[Kwiatkowski-Phillips-Schmidt-Shin]] | Times series trend is stationary | Numerical | Y | 1 |
| [[Student t test]] | The sample mean of 2 samples are the same | Numerical | Y | 2 |
| [[Paired Student t]] | The sample mean of 2 paired samples are the same  | Numerical | Y | 1 |
| [[AnOVa]] | The sample mean of 2+ samples are the same | Numerical | Y | 2+ |
| [[Repeated Measures AnOVa]] |  The sample mean of 2+  paired samples are the same | Numerical | Y | 2+ |
| [[Mann-Whitney U]] |  The distributions of 2 independent samples are the same | Numerical | N | 2 |
| [[Wilcoxon Signed-Rank]] |  The distributions of 2  paired samples are the same | Numerical | N | 2+ |
| [[Kruskal-Wallis H]] |  The distributions of 2+ independent samples are the same | Numerical | N | 2+ |
| [[Friedman]] | The distributions of 2+ paired samples are the same | Numerical | N | 2+ |
| [[Binomial test]] | The outcome of a binary variable does not differ from a hypothetical value | Numerical | Y | 1 |
| [[McNemar]] | The marginal frequency of two binary outcomes does not differ significantly | Numerical | Y | 2 |
