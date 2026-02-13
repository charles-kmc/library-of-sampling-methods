---
layout: default
title: Home
---

# 🎲 Sampling Algorithms: A Visual Tutorial Series

Welcome to my interactive tutorial series on **sampling algorithms**! Here you'll find detailed explanations, visualizations, and runnable code for various sampling methods used in machine learning, Bayesian statistics, and generative AI.

---

## 🚀 Get Started {#get-started}

New to sampling? Start here with the fundamentals:

<div class="featured-grid">
  <div class="featured-card">
    <h3>🎯 What is Sampling?</h3>
    <p>Understanding the basics: why we sample, what makes a good sample, and where sampling is used in modern computing.</p>
    <a href="/sampling-algo-tutorials/2026/02/13/intro-to-sampling" class="btn">Start Learning →</a>
  </div>
  
  <div class="featured-card">
    <h3>📊 Probability Refresher</h3>
    <p>Quick review of PDFs, CDFs, expectation, variance, and the fundamental theorem of simulation.</p>
    <a href="#" class="btn">Review →</a>
  </div>
  
  <div class="featured-card">
    <h3>🛠️ Your First Sampler</h3>
    <p>Build your first sampling algorithm from scratch in 10 minutes using only NumPy.</p>
    <a href="#" class="btn btn-secondary">Try It →</a>
  </div>
</div>

### Learning Path

<div class="mermaid">
graph LR
    A[Start Here] --> B[Basic Methods]
    B --> C[MCMC Methods]
    C --> D[Advanced Topics]
    D --> E[Generative Models]
    
    style A fill:#28a745,color:white
    style B fill:#17a2b8,color:white
    style C fill:#ffc107,color:black
    style D fill:#dc3545,color:white
    style E fill:#6f42c1,color:white
</div>

---

## 🧰 Sampling Tools {#sampling-tools}

A comprehensive toolkit of sampling algorithms, from basic to advanced:

### Basic Methods

<div class="tools-grid">
  <div class="tool-card">
    <h4>🎲 Inverse Transform</h4>
    <p>The simplest approach when you have the CDF. Works for any 1D distribution.</p>
    <div class="difficulty">★☆☆</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>📦 Rejection Sampling</h4>
    <p>Sample from any distribution using a simpler proposal distribution.</p>
    <div class="difficulty">★★☆</div>
    <a href="/sampling-algo-tutorials/2026/02/13/rejection-sampling" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>⚖️ Importance Sampling</h4>
    <p>Weighted samples for expectation estimation. Great for rare events.</p>
    <div class="difficulty">★★☆</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🎯 Adaptive Rejection</h4>
    <p>Builds a better proposal as sampling progresses.</p>
    <div class="difficulty">★★☆</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
</div>

### Markov Chain Monte Carlo (MCMC)

<div class="tools-grid">
  <div class="tool-card">
    <h4>🔄 Metropolis-Hastings</h4>
    <p>The classic MCMC algorithm. The workhorse of Bayesian inference.</p>
    <div class="difficulty">★★☆</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🔄 Gibbs Sampling</h4>
    <p>Coordinate-wise MCMC. Perfect when conditionals are known.</p>
    <div class="difficulty">★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>⚡ Hamiltonian MC</h4>
    <p>Gradient-based efficient sampling for high dimensions.</p>
    <div class="difficulty">★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🏃‍♂️ Langevin Dynamics</h4>
    <p>Combines gradient descent with noise for sampling.</p>
    <div class="difficulty">★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
</div>

### Advanced Methods

<div class="tools-grid">
  <div class="tool-card">
    <h4>🍰 Slice Sampling</h4>
    <p>Adaptive MCMC that requires no tuning parameters.</p>
    <div class="difficulty">★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🌡️ Parallel Tempering</h4>
    <p>Better mixing for multimodal distributions using temperature swaps.</p>
    <div class="difficulty">★★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🔮 Sequential Monte Carlo</h4>
    <p>Particle filtering for time series and dynamic systems.</p>
    <div class="difficulty">★★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
  
  <div class="tool-card">
    <h4>🎭 Nested Sampling</h4>
    <p>For Bayesian evidence calculation and multimodal problems.</p>
    <div class="difficulty">★★★★</div>
    <a href="#" class="btn-small">Learn →</a>
  </div>
</div>

---

## 💡 Examples {#examples}

See sampling algorithms in action with real-world applications:

<div class="examples-grid">
  <div class="example-card">
    <div class="example-img">📈</div>
    <h3>Bayesian Linear Regression</h3>
    <p>Use MCMC to sample from posterior distributions of regression parameters. Includes uncertainty quantification.</p>
    <div class="example-meta">
      <span class="tag">Metropolis-Hastings</span>
      <span class="tag">PyMC3</span>
      <span class="tag">Regression</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
  
  <div class="example-card">
    <div class="example-img">🧊</div>
    <h3>Ising Model Simulation</h3>
    <p>Sample spin configurations in statistical physics. Models magnetic materials and social networks.</p>
    <div class="example-meta">
      <span class="tag">Gibbs Sampling</span>
      <span class="tag">Physics</span>
      <span class="tag">2D Lattice</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
  
  <div class="example-card">
    <div class="example-img">📉</div>
    <h3>Option Pricing</h3>
    <p>Monte Carlo simulation for financial derivatives. Price European and Asian options.</p>
    <div class="example-meta">
      <span class="tag">Monte Carlo</span>
      <span class="tag">Finance</span>
      <span class="tag">Black-Scholes</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
  
  <div class="example-card">
    <div class="example-img">⛰️</div>
    <h3>Simulated Annealing</h3>
    <p>Global optimization using sampling techniques. Find the minimum of complex functions.</p>
    <div class="example-meta">
      <span class="tag">Optimization</span>
      <span class="tag">Annealing</span>
      <span class="tag">Global Optima</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
  
  <div class="example-card">
    <div class="example-img">🧬</div>
    <h3>Phylogenetic Inference</h3>
    <p>Sample evolutionary trees using MCMC. Reconstruct species relationships.</p>
    <div class="example-meta">
      <span class="tag">MCMC</span>
      <span class="tag">Biology</span>
      <span class="tag">Evolution</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
  
  <div class="example-card">
    <div class="example-img">🗺️</div>
    <h3>SLAM for Robotics</h3>
    <p>Simultaneous Localization and Mapping using particle filters.</p>
    <div class="example-meta">
      <span class="tag">Particle Filter</span>
      <span class="tag">Robotics</span>
      <span class="tag">SMC</span>
    </div>
    <a href="#" class="btn-small">View Example →</a>
  </div>
</div>

### Interactive Demos

Try these live examples in your browser:

- [🎯 2D Distribution Explorer](notebooks/2d_distribution_explorer.ipynb) - Visualize and sample from different 2D distributions
- [🔄 MCMC Animation](notebooks/mcmc_animation.ipynb) - Watch the Markov chain explore the parameter space
- [📊 Acceptance Rate Tuner](notebooks/acceptance_tuner.ipynb) - Find the optimal proposal scale for MH
- [🌡️ Temperature Scheduler](notebooks/temperature_scheduler.ipynb) - Experiment with annealing schedules

---

## 🧠 Generative Models {#generative-models}

Explore how sampling powers modern generative AI:

<div class="genmodels-grid">
  <div class="genmodel-card featured">
    <h3>🎨 Variational Autoencoders (VAEs)</h3>
    <p>Learn how VAEs use the reparameterization trick to sample from latent spaces and generate new data.</p>
    <div class="key-concepts">
      <span class="concept">Reparameterization</span>
      <span class="concept">ELBO</span>
      <span class="concept">Latent Variables</span>
      <span class="concept">Encoder/Decoder</span>
    </div>
    <div class="progress">
      <div class="progress-bar" style="width: 75%"></div>
    </div>
    <p><small>Tutorial 3 of 4 completed</small></p>
    <a href="#" class="btn">Start Tutorial →</a>
  </div>
  
  <div class="genmodel-card">
    <h3>🌌 Generative Adversarial Networks</h3>
    <p>Understanding the sampling process in GANs. How generators create fake data that fools discriminators.</p>
    <div class="key-concepts">
      <span class="concept">Adversarial Training</span>
      <span class="concept">Generator</span>
      <span class="concept">Discriminator</span>
      <span class="concept">Nash Equilibrium</span>
    </div>
    <div class="status">Coming Soon</div>
  </div>
  
  <div class="genmodel-card">
    <h3>🔄 Normalizing Flows</h3>
    <p>Invertible transformations for complex distributions. Exact likelihood computation and sampling.</p>
    <div class="key-concepts">
      <span class="concept">Change of Variables</span>
      <span class="concept">Jacobian</span>
      <span class="concept">Invertible NN</span>
      <span class="concept">RealNVP</span>
    </div>
    <div class="status">Coming Soon</div>
  </div>
  
  <div class="genmodel-card">
    <h3>🧩 Diffusion Models</h3>
    <p>Sampling by reversing a diffusion process. The technology behind DALL-E and Stable Diffusion.</p>
    <div class="key-concepts">
      <span class="concept">Denoising</span>
      <span class="concept">Score Matching</span>
      <span class="concept">Markov Chain</span>
      <span class="concept">DDPM</span>
    </div>
    <div class="status">Coming Soon</div>
  </div>
  
  <div class="genmodel-card">
    <h3>🔮 Energy-Based Models</h3>
    <p>Learn the energy function and sample using MCMC/Langevin dynamics.</p>
    <div class="key-concepts">
      <span class="concept">Energy Function</span>
      <span class="concept">Langevin Dynamics</span>
      <span class="concept">Contrastive Divergence</span>
    </div>
    <div class="status">Coming Soon</div>
  </div>
  
  <div class="genmodel-card">
    <h3>🎭 Boltzmann Machines</h3>
    <p>Stochastic recurrent neural networks for unsupervised learning.</p>
    <div class="key-concepts">
      <span class="concept">Restricted BM</span>
      <span class="concept">Gibbs Sampling</span>
      <span class="concept">Hidden Units</span>
    </div>
    <div class="status">Coming Soon</div>
  </div>
</div>

### Sampling in Modern AI

| Model Type | Sampling Method | Use Case | Example |
|:-----------|:----------------|:---------|:--------|
| **VAE** | Reparameterization Trick | Image generation | Face generation |
| **GAN** | Latent space sampling | Synthetic data | Deepfakes |
| **Diffusion** | Reverse process | High-quality images | DALL-E 2 |
| **Normalizing Flow** | Direct transform | Density estimation | Glow |
| **Energy-Based** | MCMC (Langevin) | Density learning | |

---

## 📊 Quick Reference

### Algorithm Comparison

| Algorithm | Type | Dimension | Acceptance | Best For | Implementation |
|:----------|:-----|:----------|:-----------|:---------|:---------------|
| **Inverse Transform** | Direct | 1D | 100% | Simple distributions | Easy |
| **Rejection Sampling** | Direct | Low | Variable | Known PDFs | Moderate |
| **Metropolis-Hastings** | MCMC | Medium | ~23% | General purpose | Easy |
| **Gibbs** | MCMC | High | 100% | Conditional known | Moderate |
| **HMC** | MCMC | High | ~65% | Differentiable models | Complex |
| **SMC** | Sequential | Dynamic | N/A | Time series | Complex |
| **Slice Sampling** | MCMC | Medium | Adaptive | No tuning | Moderate |

### When to Use What

```python
def choose_sampler(problem):
    """
    Helper function to choose the right sampling algorithm
    """
    if problem['dimension'] == 1:
        if problem.get('has_cdf', False):
            return "Inverse Transform Sampling"
        else:
            return "Rejection Sampling"
    
    elif problem['dimension'] <= 10:
        if problem.get('multimodal', False):
            return "Parallel Tempering"
        else:
            return "Metropolis-Hastings"
    
    else:  # High dimensional
        if problem.get('has_gradients', False):
            return "Hamiltonian Monte Carlo"
        elif problem.get('conditionals_known', False):
            return "Gibbs Sampling"
        else:
            return "Metropolis-Hastings with adaptive proposal"