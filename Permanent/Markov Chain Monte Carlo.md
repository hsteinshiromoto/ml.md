---
alias: [MCMC]
tags: []
date created: 2023-10-20 10:31:02
---

# Markov Chain Monte Carlo

## Introduction

_Markov Chain [[Monte Carlo]]_ (MCMC) is a statistical and computational method used for approximating complex probability distributions. It's particularly useful when you want to sample from or estimate the properties of a probability distribution when you can't easily do so analytically. MCMC is widely used in fields such as statistics, machine learning, Bayesian inference, and physics, among others.

At the heart of MCMC is the concept of a Markov chain. A Markov chain is a sequence of random variables where each variable depends only on the previous one, and not on earlier values. In the context of MCMC, this sequence represents a sequence of samples from the target probability distribution.

## How it Works

The basic idea of Markov Chain Monte Carlo can be summarized as follows:

1. **Define the Target Distribution**: Start with a probability distribution from which you want to sample or for which you want to estimate properties. This could be a posterior distribution in Bayesian statistics, a likelihood function, or any other complex distribution.
2. **Proposal Distribution**: Choose a proposal distribution that is easier to sample from than the target distribution. The proposal distribution suggests where to move in the sample space.
3. **Generate a Markov Chain**: Start with an initial value and use the proposal distribution to generate a candidate sample. Accept or reject this candidate based on a criterion that ensures that the Markov chain eventually converges to the target distribution. A common criterion is the Metropolis-Hastings algorithm, which involves comparing the ratio of the target distribution and the proposal distribution.
4. **Repeat**: Continue generating candidate samples, accepting or rejecting them, and updating the Markov chain until you have collected a sufficient number of samples.
5. **Convergence**: As the Markov chain progresses, it approaches a state where the samples it generates closely approximate the target distribution. This state is called "convergence."
6. **Estimate Properties**: Once you have a sufficiently large number of samples from the converged Markov chain, you can use these samples to estimate properties of the target distribution, such as the mean, variance, or quantiles.

MCMC is a powerful technique for dealing with high-dimensional and complex probability distributions. One of the most well-known MCMC algorithms is the Metropolis-Hastings algorithm, and its extension, the Gibbs sampler. Another widely used algorithm is the Hamiltonian Monte Carlo (HMC), which incorporates concepts from physics to improve sampling efficiency.

MCMC is an essential tool in Bayesian statistics, and it's used in Bayesian parameter estimation, model fitting, and Bayesian inference. It allows researchers to make probabilistic inferences about model parameters and predictions based on data and prior knowledge.