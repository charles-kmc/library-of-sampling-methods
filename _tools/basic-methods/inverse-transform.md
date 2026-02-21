---
title: "Inverse Transform Sampling"
description: "The simplest approach when you have the CDF. Works for any 1D distribution."
difficulty: "★☆☆"
type: "Basic Method"
icon: "🎲"
category: "basic"
order: 1
---

# Inverse Transform Sampling

Inverse transform sampling is a fundamental method for generating random numbers from any probability distribution given its cumulative distribution function (CDF).

## Key Concepts
- Uses the inverse of the CDF
- Works for any 1D distribution
- Requires the CDF to be invertible

## Algorithm
1. Generate u ~ Uniform(0,1)
2. Return x = F⁻¹(u)

[Read the full tutorial...](#)