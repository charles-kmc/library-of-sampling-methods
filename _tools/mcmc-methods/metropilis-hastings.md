---
title: "Metropolis-Hastings"
description: "The classic MCMC algorithm. The workhorse of Bayesian inference."
difficulty: "★★☆"
type: "MCMC"
icon: "🔄"
category: "mcmc"
order: 1
---

# Metropolis-Hastings

Metropolis-Hastings is a Markov Chain Monte Carlo method for sampling from complex distributions.

## Key Concepts
- Random walk exploration
- Acceptance probability
- Detailed balance

## Algorithm
1. Propose new state x' ~ q(x'|x)
2. Compute acceptance ratio α
3. Accept with probability min(1,α)

[Read the full tutorial...](#)