---
layout: default
title: Get Started with Sampling
---

<!-- Navigation Bar -->
<div class="top-nav">
  <a href="{{ site.baseurl }}/" class="nav-link">Home</a>
  <a href="{{ site.baseurl }}/start" class="nav-link active">Start</a>
  <a href="{{ site.baseurl }}/sampling-tools" class="nav-link">Sampling tools</a>
  <a href="{{ site.baseurl }}/examples" class="nav-link">Examples</a>
  <a href="{{ site.baseurl }}/projects" class="nav-link">Projects</a>
</div>

<div class="page-header">
  <h1>🚀 Get Started with Sampling</h1>
  <p>Begin your journey into the world of sampling algorithms</p>
</div>

<div class="learning-path">
  <h2>Learning Path</h2>
  <div class="path-steps">
    <div class="step">
      <div class="step-number">1</div>
      <div class="step-content">
        <h3>What is Sampling?</h3>
        <p>Understand the basics and why sampling matters</p>
        <a href="{{ site.baseurl }}/2026/02/13/intro-to-sampling" class="step-link">Start →</a>
      </div>
    </div>
    
    <div class="step">
      <div class="step-number">2</div>
      <div class="step-content">
        <h3>Probability Refresher</h3>
        <p>Review PDFs, CDFs, and random variables</p>
        <a href="#" class="step-link">Start →</a>
      </div>
    </div>
    
    <div class="step">
      <div class="step-number">3</div>
      <div class="step-content">
        <h3>Your First Sampler</h3>
        <p>Build a simple sampler from scratch</p>
        <a href="#" class="step-link">Start →</a>
      </div>
    </div>
    
    <div class="step">
      <div class="step-number">4</div>
      <div class="step-content">
        <h3>Basic Methods</h3>
        <p>Learn inverse transform and rejection sampling</p>
        <a href="{{ site.baseurl }}/2026/02/13/rejection-sampling" class="step-link">Start →</a>
      </div>
    </div>
  </div>
</div>

<style>
.page-header {
  text-align: center;
  margin: 3rem 0;
}

.page-header h1 {
  font-size: 2.5rem;
  color: #333;
  margin-bottom: 0.5rem;
}

.page-header p {
  font-size: 1.2rem;
  color: #666;
}

.learning-path {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}

.learning-path h2 {
  text-align: center;
  margin-bottom: 3rem;
  color: #333;
}

.path-steps {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.step {
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
  background: white;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.step-number {
  width: 40px;
  height: 40px;
  background: #667eea;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2rem;
  flex-shrink: 0;
}

.step-content {
  flex: 1;
}

.step-content h3 {
  color: #333;
  margin-bottom: 0.5rem;
}

.step-content p {
  color: #666;
  margin-bottom: 1rem;
}

.step-link {
  color: #667eea;
  text-decoration: none;
  font-weight: 500;
}

.active {
  color: #667eea;
  font-weight: 600;
}

@media (max-width: 768px) {
  .step {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>