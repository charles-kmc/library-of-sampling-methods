---
title: "Importance Sampling"
description: "Weighted samples for expectation estimation. Great for rare events."
difficulty: "★★☆"
type: "Advanced Method"
icon: "⚖️"
category: "basic"
order: 3
---

# Importance Sampling

Importance sampling is a technique for estimating properties of a distribution while sampling from a different distribution.

## Key Concepts
- Weighted samples
- Great for rare events
- Estimates expectations

## Algorithm
1. Sample from proposal q(x)
2. Compute weights w(x) = p(x)/q(x)
3. Estimate E[f(x)] = Σ w(x)f(x)/Σ w(x)

[Read the full tutorial...](#)