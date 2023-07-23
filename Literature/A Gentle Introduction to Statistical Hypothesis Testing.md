Last Updated on April 10, 2020

Data must be interpreted in order to add meaning.

We can interpret data by assuming a specific structure our outcome and use statistical methods to confirm or reject the assumption. The assumption is called a hypothesis and the statistical tests used for this purpose are called statistical hypothesis tests.

Whenever we want to make claims about the distribution of data or whether one set of results are different from another set of results in applied machine learning, we must rely on statistical hypothesis tests.

In this tutorial, you will discover statistical hypothesis testing and how to interpret and carefully state the results from statistical tests.

After completing this tutorial, you will know:

-   Statistical hypothesis tests are important for quantifying answers to questions about samples of data.
-   The interpretation of a statistical hypothesis test requires a correct understanding of p-values and critical values.
-   Regardless of the significance level, the finding of hypothesis tests may still contain errors.

**Kick-start your project** with my new book [Statistics for Machine Learning](https://machinelearningmastery.com/statistics_for_machine_learning/), including _step-by-step tutorials_ and the _Python source code_ files for all examples.

Let’s get started.

-   **Update May/2018**: Added note about “reject” vs “failure to reject”, improved language on this issue.
-   **Update Jun/2018**: Fixed typo in the explanation of type I and type II errors.
-   **Update Jun/2019**: Added examples of tests and links to Python tutorials.

![A Gentle Introduction to Statistical Hypothesis Tests](https://machinelearningmastery.com/wp-content/uploads/2018/05/A-Gentle-Introduction-to-Statistical-Hypothesis-Tests.jpg)

A Gentle Introduction to Statistical Hypothesis Tests  
Photo by [Kevin Verbeem](https://www.flickr.com/photos/kevinverbeem/33597498581/), some rights reserved.

## Tutorial Overview

This tutorial is divided into five parts; they are:

1.  Statistical Hypothesis Testing
2.  Statistical Test Interpretation
3.  Errors in Statistical Tests
4.  Examples of Hypothesis Tests
5.  Python Tutorials

### Need help with Statistics for Machine Learning?

Take my free 7-day email crash course now (with sample code).

Click to sign-up and also get a free PDF Ebook version of the course.

## Statistical Hypothesis Testing

Data alone is not interesting. It is the interpretation of the data that we are really interested in.

In statistics, when we wish to start asking questions about the data and interpret the results, we use statistical methods that provide a confidence or likelihood about the answers. In general, this class of methods is called [statistical hypothesis testing](https://en.wikipedia.org/wiki/Statistical_hypothesis_testing), or significance tests.

The term “[_hypothesis_](https://machinelearningmastery.com/what-is-a-hypothesis-in-machine-learning/)” may make you think about science, where we investigate a hypothesis. This is along the right track.

In statistics, a hypothesis test calculates some quantity under a given assumption. The result of the test allows us to interpret whether the assumption holds or whether the assumption has been violated.

Two concrete examples that we will use a lot in machine learning are:

-   A test that assumes that data has a normal distribution.
-   A test that assumes that two samples were drawn from the same underlying population distribution.

The assumption of a statistical test is called the null hypothesis, or hypothesis 0 (H0 for short). It is often called the default assumption, or the assumption that nothing has changed.

A violation of the test’s assumption is often called the first hypothesis, hypothesis 1 or H1 for short. H1 is really a short hand for “_some other hypothesis_,” as all we know is that the evidence suggests that the H0 can be rejected.

-   **Hypothesis 0 (H0)**: Assumption of the test holds and is failed to be rejected at some level of significance.
-   **Hypothesis 1 (H1)**: Assumption of the test does not hold and is rejected at some level of significance.

Before we can reject or fail to reject the null hypothesis, we must interpret the result of the test.

## Statistical Test Interpretation

The results of a statistical hypothesis test must be interpreted for us to start making claims.

This is a point that may cause a lot of confusion for beginners and experienced practitioners alike.

There are two common forms that a result from a statistical hypothesis test may take, and they must be interpreted in different ways. They are the p-value and [critical values](https://machinelearningmastery.com/critical-values-for-statistical-hypothesis-testing/).

### Interpret the p-value

We describe a finding as statistically significant by interpreting the p-value.

For example, we may perform a normality test on a data sample and find that it is unlikely that sample of data deviates from a Gaussian distribution, failing to reject the null hypothesis.

A statistical hypothesis test may return a value called p or the [p-value](https://en.wikipedia.org/wiki/P-value). This is a quantity that we can use to interpret or quantify the result of the test and either reject or fail to reject the null hypothesis. This is done by comparing the p-value to a threshold value chosen beforehand called the significance level.

The [significance level](https://en.wikipedia.org/wiki/Statistical_significance) is often referred to by the Greek lower case letter alpha.

A common value used for alpha is 5% or 0.05. A smaller alpha value suggests a more robust interpretation of the null hypothesis, such as 1% or 0.1%.

The p-value is compared to the pre-chosen alpha value. A result is statistically significant when the p-value is less than alpha. This signifies a change was detected: that the default hypothesis can be rejected.

-   **If p-value > alpha**: Fail to reject the null hypothesis (i.e. not significant result).
-   **If p-value <= alpha**: Reject the null hypothesis (i.e. significant result).

For example, if we were performing a test of whether a data sample was normal and we calculated a p-value of .07, we could state something like:

> The test found that the data sample was normal, failing to reject the null hypothesis at a 5% significance level.

The significance level can be inverted by subtracting it from 1 to give a confidence level of the hypothesis given the observed sample data.

<table><tbody><tr><td data-settings="show"></td><td><div><p>confidence level = 1 - significance level</p></div></td></tr></tbody></table>

Therefore, statements such as the following can also be made:

> The test found that the data was normal, failing to reject the null hypothesis at a 95% confidence level.

### “Reject” vs “Failure to Reject”

The p-value is probabilistic.

This means that when we interpret the result of a statistical test, we do not know what is true or false, only what is likely.

Rejecting the null hypothesis means that there is sufficient statistical evidence that the null hypothesis does not look likely. Otherwise, it means that there is not sufficient statistical evidence to reject the null hypothesis.

We may think about the statistical test in terms of the dichotomy of rejecting and accepting the null hypothesis. The danger is that if we say that we “_accept_” the null hypothesis, the language suggests that the null hypothesis is true. Instead, it is safer to say that we “_fail to reject_” the null hypothesis, as in, there is insufficient statistical evidence to reject it.

When reading “_reject_” vs “_fail to reject_” for the first time, it is confusing to beginners. You can think of it as “_reject_” vs “_accept_” in your mind, as long as you remind yourself that the result is probabilistic and that even an “_accepted_” null hypothesis still has a small probability of being wrong.

### Common p-value Misinterpretations

This section highlights some [common misinterpretations of the p-value](https://en.wikipedia.org/wiki/Misunderstandings_of_p-values) in the results of statistical tests.

#### True or False Null Hypothesis

The interpretation of the p-value does not mean that the null hypothesis is true or false.

It does mean that we have chosen to reject or fail to reject the null hypothesis at a specific statistical significance level based on empirical evidence and the chosen statistical test.

You are limited to making probabilistic claims, not crisp binary or true/false claims about the result.

#### p-value as Probability

A common misunderstanding is that the p-value is a probability of the null hypothesis being true or false given the data.

In probability, this would be written as follows:

This is incorrect.

Instead, the p-value can be thought of as the probability of the data given the pre-specified assumption embedded in the statistical test.

Again, using probability notation, this would be written as:

It allows us to reason about whether or not the data fits the hypothesis. Not the other way around.

The p-value is a measure of how likely the data sample would be observed if the null hypothesis were true.

#### Post-Hoc Tuning

It does not mean that you can re-sample your domain or tune your data sample and re-run the statistical test until you achieve a desired result.

It also does not mean that you can choose your p-value after you run the test.

This is called p-hacking or hill climbing and will mean that the result you present will be fragile and not representative. In science, this is at best unethical, and at worst fraud.

### Interpret Critical Values

Some tests do not return a p-value.

Instead, they might return a list of [critical values](https://en.wikipedia.org/wiki/Critical_value) and their associated significance levels, as well as a test statistic.

These are usually nonparametric or distribution-free statistical hypothesis tests.

The choice of returning a p-value or a list of critical values is really an implementation choice.

The results are interpreted in a similar way. Instead of comparing a single p-value to a pre-specified significance level, the test statistic is compared to the critical value at a chosen significance level.

-   **If test statistic < critical value**: Fail to reject the null hypothesis.
-   **If test statistic >= critical value**: Reject the null hypothesis.

Again, the meaning of the result is similar in that the chosen significance level is a probabilistic decision on rejection or fail to reject the base assumption of the test given the data.

Results are presented in the same way as with a p-value, as either significance level or confidence level. For example, if a normality test was calculated and the test statistic was compared to the critical value at the 5% significance level, results could be stated as:

> The test found that the data sample was normal, failing to reject the null hypothesis at a 5% significance level.

Or:

> The test found that the data was normal, failing to reject the null hypothesis at a 95% confidence level.

## Errors in Statistical Tests

The interpretation of a statistical hypothesis test is probabilistic.

That means that the evidence of the test may suggest an outcome and be mistaken.

For example, if alpha was 5%, it suggests that (at most) 1 time in 20 that the null hypothesis would be mistakenly rejected or failed to be rejected because of the statistical noise in the data sample.

Given a small p-value (reject the null hypothesis) either means that the null hypothesis false (we got it right) or it is true and some rare and unlikely event has been observed (we made a mistake). If this type of error is made, it is called a **false positive**. We falsely believe the rejection of the null hypothesis.

Alternately, given a large p-value (fail to reject the null hypothesis), it may mean that the null hypothesis is true (we got it right) or that the null hypothesis is false and some unlikely event occurred (we made a mistake). If this type of error is made, it is called a **false negative**. We falsely believe the null hypothesis or assumption of the statistical test.

Each of these two types of error has a specific name.

-   **Type I Error**: The incorrect rejection of a true null hypothesis or a false positive.
-   **Type II Error**: The incorrect failure of rejection of a false null hypothesis or a false negative.

All statistical hypothesis tests have a chance of making either of these types of errors. False findings or false disoveries are more than possible; they are probable.

Ideally, we want to choose a significance level that minimizes the likelihood of one of these errors. E.g. a very small significance level. Although significance levels such as 0.05 and 0.01 are common in many fields of science, harder sciences, [such as physics](http://www.physics.org/article-questions.asp?id=103), are more aggressive.

It is common to use a significance level of 3 \* 10^-7 or 0.0000003, often referred to as 5-sigma. This means that the finding was due to chance with a probability of 1 in 3.5 million independent repeats of the experiments. To use a threshold like this may require a much large data sample.

Nevertheless, these types of errors are always present and must be kept in mind when presenting and interpreting the results of statistical tests. It is also a reason why it is important to have findings independently verified.

## Examples of Hypothesis Tests

There are many types of statistical hypothesis tests.

This section lists some common examples of statistical hypothesis tests and the types of problems that they are used to address:

### Variable Distribution Type Tests (Gaussian)

-   Shapiro-Wilk Test
-   D’Agostino’s K^2 Test
-   Anderson-Darling Test

### Variable Relationship Tests (correlation)

-   Pearson’s Correlation Coefficient
-   Spearman’s Rank Correlation
-   Kendall’s Rank Correlation
-   Chi-Squared Test

### Compare Sample Means (parametric)

-   Student’s t-test
-   Paired Student’s t-test
-   Analysis of Variance Test (ANOVA)
-   Repeated Measures ANOVA Test

### Compare Sample Means (nonparametric)

-   Mann-Whitney U Test
-   Wilcoxon Signed-Rank Test
-   Kruskal-Wallis H Test
-   Friedman Test

For example Python code on how to use each of these tests, see the next section.

## Python Tutorials

This section provides links to Python tutorials on statistical hypothesis testing:

Examples of many tests:

-   [15 Statistical Hypothesis Tests in Python (Cheat Sheet)](https://machinelearningmastery.com/statistical-hypothesis-tests-in-python-cheat-sheet/)

Variable distribution tests:

-   [A Gentle Introduction to Normality Tests in Python](https://machinelearningmastery.com/a-gentle-introduction-to-normality-tests-in-python/)

Evaluating variable relationships:

-   [How to Calculate Correlation Between Variables in Python](https://machinelearningmastery.com/how-to-use-correlation-to-understand-the-relationship-between-variables/)
-   [How to Calculate Nonparametric Rank Correlation in Python](https://machinelearningmastery.com/how-to-calculate-nonparametric-rank-correlation-in-python/)

Comparing sample means:

-   [How to Calculate Parametric Statistical Hypothesis Tests in Python](https://machinelearningmastery.com/parametric-statistical-significance-tests-in-python/)
-   [How to Calculate Nonparametric Statistical Hypothesis Tests in Python](https://machinelearningmastery.com/nonparametric-statistical-significance-tests-in-python/)

## Extensions

This section lists some ideas for extending the tutorial that you may wish to explore.

-   Find an example of a research paper that does not present results using p-values.
-   Find an example of a research paper that presents results with statistical significance, but makes one of the common misinterpretations of p-values.
-   Find an example of a research paper that presents results with statistical significance and correctly interprets and presents the p-value and findings.

If you explore any of these extensions, I’d love to know.

## Further Reading

This section provides more resources on the topic if you are looking to go deeper.

### Articles

-   [Statistical hypothesis testing on Wikipedia](https://en.wikipedia.org/wiki/Statistical_hypothesis_testing)
-   [Statistical significance on Wikipedia](https://en.wikipedia.org/wiki/Statistical_significance)
-   [p-value on Wikipedia](https://en.wikipedia.org/wiki/P-value)
-   [Critical value on Wikipedia](https://en.wikipedia.org/wiki/Critical_value)
-   [Type I and type II errors on Wikipedia](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors)
-   [Data dredging on Wikipedia](https://en.wikipedia.org/wiki/Data_dredging)
-   [Misunderstandings of p-values on Wikipedia](https://en.wikipedia.org/wiki/Misunderstandings_of_p-values)
-   [What does the 5 sigma mean?](http://www.physics.org/article-questions.asp?id=103)

## Summary

In this tutorial, you discovered statistical hypothesis testing and how to interpret and carefully state the results from statistical tests.

Specifically, you learned:

-   Statistical hypothesis tests are important for quantifying answers to questions about samples of data.
-   The interpretation of a statistical hypothesis test requires a correct understanding of p-values.
-   Regardless of the significance level, the finding of hypothesis tests may still contain errors.

Do you have any questions?  
Ask your questions in the comments below and I will do my best to answer.

## Get a Handle on Statistics for Machine Learning!

[![Statistical Methods for Machine Learning](https://machinelearningmastery.com/wp-content/uploads/2022/11/SMML-220.png)](https://machinelearningmastery.com/statistics_for_machine_learning/)

#### Develop a working understanding of statistics

...by writing lines of code in python

Discover how in my new Ebook:  
[Statistical Methods for Machine Learning](https://machinelearningmastery.com/statistics_for_machine_learning/)

It provides **self-study tutorials** on topics like:  
_Hypothesis Tests, Correlation, Nonparametric Stats, Resampling_, and much more...

#### Discover how to Transform Data into Knowledge

Skip the Academics. Just Results.

[See What's Inside](https://machinelearningmastery.com/statistics_for_machine_learning/)