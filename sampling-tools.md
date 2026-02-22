---
layout: default
title: Sampling Tools
---

<!-- Navigation Bar (from default layout) -->

<div class="tools-hero">
  <h1>🔧 Sampling Tools</h1>
  <p>A comprehensive collection of sampling algorithms, dynamically loaded from our library</p>
</div>

<!-- Group tools by category -->
{% assign basic_tools = site.tools | where: "category", "basic" | sort: "order" %}
{% assign mcmc_tools = site.tools | where: "category", "mcmc" | sort: "order" %}
{% assign advanced_tools = site.tools | where: "category", "advanced" | sort: "order" %}

<!-- Basic Methods Section -->
<section class="tools-section">
  <h2>📦 Basic Methods</h2>
  <p class="section-description">Fundamental sampling techniques for simple distributions</p>
  
  <div class="tools-grid">
    <!-- {% assign tools = site.start | sort: 'order' %}   -->
    {% assign tools = site.start | sort: 'order' %}  
    {% for tool in basic_tools %}
    <div class="tool-card" data-aos="fade-up">
      <div class="tool-card-header">
        <span class="tool-icon">{{ tool.icon }}</span>
        <span class="tool-difficulty">{{ tool.difficulty }}</span>
      </div>
      <h3>{{ tool.title }}</h3>
      <p>{{ tool.description }}</p>
      <div class="tool-card-footer">
        <span class="tool-type">{{ tool.type }}</span>
        <a href="{{ site.baseurl }}{{ tool.url }}" class="tool-link">
          Learn More Here ... <i class="fas fa-arrow-right"></i>
        </a>
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<!-- MCMC Methods Section -->
<section class="tools-section">
  <h2>🔄 Markov Chain Monte Carlo</h2>
  <p class="section-description">Powerful methods for sampling from complex, high-dimensional distributions</p>
  
  <div class="tools-grid">
    {% for tool in mcmc_tools %}
    <div class="tool-card" data-aos="fade-up" data-aos-delay="{{ forloop.index | times: 50 }}">
      <div class="tool-card-header">
        <span class="tool-icon">{{ tool.icon }}</span>
        <span class="tool-difficulty">{{ tool.difficulty }}</span>
      </div>
      <h3>{{ tool.title }}</h3>
      <p>{{ tool.description }}</p>
      <div class="tool-card-footer">
        <span class="tool-type">{{ tool.type }}</span>
        <a href="{{ site.baseurl }}{{ tool.url }}" class="tool-link">
          Learn More <i class="fas fa-arrow-right"></i>
        </a>
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<!-- Advanced Methods Section -->
<section class="tools-section">
  <h2>🚀 Advanced Methods</h2>
  <p class="section-description">State-of-the-art sampling algorithms for challenging problems</p>
  
  <div class="tools-grid">
    {% for tool in advanced_tools %}
    <div class="tool-card" data-aos="fade-up" data-aos-delay="{{ forloop.index | times: 50 }}">
      <div class="tool-card-header">
        <span class="tool-icon">{{ tool.icon }}</span>
        <span class="tool-difficulty">{{ tool.difficulty }}</span>
      </div>
      <h3>{{ tool.title }}</h3>
      <p>{{ tool.description }}</p>
      <div class="tool-card-footer">
        <span class="tool-type">{{ tool.type }}</span>
        <a href="{{ site.baseurl }}{{ tool.url }}" class="tool-link">
          Learn More <i class="fas fa-arrow-right"></i>
        </a>
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<!-- Stats Section -->
<div class="tools-stats">
  <div class="stat-card">
    <span class="stat-number">{{ site.tools | size }}</span>
    <span class="stat-label">Total Algorithms</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ basic_tools | size }}</span>
    <span class="stat-label">Basic Methods</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ mcmc_tools | size }}</span>
    <span class="stat-label">MCMC Methods</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ advanced_tools | size }}</span>
    <span class="stat-label">Advanced Methods</span>
  </div>
</div>

<style>
.tools-hero {
  text-align: center;
  margin: 3rem 0;
  padding: 2rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 10px;
  color: white;
}

.tools-hero h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.tools-hero p {
  font-size: 1.2rem;
  opacity: 0.95;
}

.tools-section {
  margin: 4rem 0;
}

.tools-section h2 {
  color: #333;
  font-size: 2rem;
  margin-bottom: 0.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 3px solid #667eea;
  display: inline-block;
}

.section-description {
  color: #666;
  margin-bottom: 2rem;
  font-size: 1.1rem;
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.tool-card {
  background: white;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  border: 1px solid #f0f0f0;
  position: relative;
  overflow: hidden;
}

.tool-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #667eea, #764ba2);
  transform: scaleX(0);
  transition: transform 0.3s ease;
}

.tool-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(102, 126, 234, 0.2);
}

.tool-card:hover::before {
  transform: scaleX(1);
}

.tool-card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.tool-icon {
  font-size: 2rem;
}

.tool-difficulty {
  background: #f0f0f0;
  padding: 0.3rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  color: #666;
}

.tool-card h3 {
  color: #333;
  margin-bottom: 0.8rem;
  font-size: 1.3rem;
}

.tool-card p {
  color: #666;
  margin-bottom: 1.5rem;
  line-height: 1.6;
  font-size: 0.95rem;
}

.tool-card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: auto;
}

.tool-type {
  background: #667eea;
  color: white;
  padding: 0.3rem 1rem;
  border-radius: 20px;
  font-size: 0.8rem;
}

.tool-link {
  color: #667eea;
  text-decoration: none;
  font-weight: 500;
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  transition: gap 0.3s ease;
}

.tool-link:hover {
  gap: 0.5rem;
  color: #764ba2;
}

.tools-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1.5rem;
  margin: 3rem 0;
  padding: 2rem;
  background: white;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.stat-card {
  text-align: center;
  padding: 1rem;
}

.stat-number {
  display: block;
  font-size: 2.5rem;
  font-weight: bold;
  color: #667eea;
  margin-bottom: 0.3rem;
}

.stat-label {
  color: #666;
  font-size: 0.95rem;
}

@media (max-width: 768px) {
  .tools-hero h1 {
    font-size: 2rem;
  }
  
  .tools-section h2 {
    font-size: 1.5rem;
  }
  
  .tools-grid {
    grid-template-columns: 1fr;
  }
  
  .tools-stats {
    grid-template-columns: 1fr 1fr;
  }
}

/* Animation */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.tool-card {
  animation: fadeInUp 0.5s ease-out forwards;
}
</style>

<!-- Add AOS animation library (optional) -->
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>
  AOS.init({
    duration: 800,
    once: true
  });
</script>