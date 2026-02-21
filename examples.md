---
layout: default
title: Examples
---

<!-- Navigation Bar (from default layout) -->

<div class="examples-hero">
  <h1>💡 Examples</h1>
  <p>Real-world applications of sampling algorithms, dynamically loaded from our library</p>
</div>

<!-- Filter Bar -->
<div class="filter-bar">
  <button class="filter-btn active" data-filter="all">All</button>
  <button class="filter-btn" data-filter="bayesian">📈 Bayesian</button>
  <button class="filter-btn" data-filter="physics">🧊 Physics</button>
  <button class="filter-btn" data-filter="finance">📉 Finance</button>
  <button class="filter-btn" data-filter="optimization">⛰️ Optimization</button>
</div>

<!-- Group examples by category -->
{% assign bayesian_examples = site.examples | where: "category", "bayesian" | sort: "order" %}
{% assign physics_examples = site.examples | where: "category", "physics" | sort: "order" %}
{% assign finance_examples = site.examples | where: "category", "finance" | sort: "order" %}
{% assign optimization_examples = site.examples | where: "category", "optimization" | sort: "order" %}

<!-- Examples Grid -->
<div class="examples-grid-container">
  <!-- Bayesian Section -->
  <section class="example-category-section" data-category="bayesian">
    <h2>📈 Bayesian Methods</h2>
    <p class="category-description">Examples using Bayesian inference and MCMC</p>
    <div class="examples-grid">
      {% for example in bayesian_examples %}
      <div class="example-card" data-category="{{ example.category }}">
        <div class="example-card-header">
          <span class="example-icon">{{ example.icon }}</span>
          <span class="example-difficulty">{{ example.difficulty }}</span>
        </div>
        <h3>{{ example.title }}</h3>
        <p>{{ example.description }}</p>
        <div class="example-tags">
          {% for tag in example.tags limit:3 %}
          <span class="example-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        <div class="example-card-footer">
          <a href="{{ site.baseurl }}{{ example.url }}" class="example-link">
            View Example <i class="fas fa-arrow-right"></i>
          </a>
          {% if example.colab %}
          <a href="{{ example.colab }}" class="example-colab-icon" title="Run in Colab">
            <i class="fas fa-cloud"></i>
          </a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- Physics Section -->
  <section class="example-category-section" data-category="physics">
    <h2>🧊 Physics & Statistical Mechanics</h2>
    <p class="category-description">Examples from physics and natural sciences</p>
    <div class="examples-grid">
      {% for example in physics_examples %}
      <div class="example-card" data-category="{{ example.category }}">
        <div class="example-card-header">
          <span class="example-icon">{{ example.icon }}</span>
          <span class="example-difficulty">{{ example.difficulty }}</span>
        </div>
        <h3>{{ example.title }}</h3>
        <p>{{ example.description }}</p>
        <div class="example-tags">
          {% for tag in example.tags limit:3 %}
          <span class="example-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        <div class="example-card-footer">
          <a href="{{ site.baseurl }}{{ example.url }}" class="example-link">
            View Example <i class="fas fa-arrow-right"></i>
          </a>
          {% if example.colab %}
          <a href="{{ example.colab }}" class="example-colab-icon" title="Run in Colab">
            <i class="fas fa-cloud"></i>
          </a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- Finance Section -->
  <section class="example-category-section" data-category="finance">
    <h2>📉 Finance & Economics</h2>
    <p class="category-description">Financial applications of Monte Carlo methods</p>
    <div class="examples-grid">
      {% for example in finance_examples %}
      <div class="example-card" data-category="{{ example.category }}">
        <div class="example-card-header">
          <span class="example-icon">{{ example.icon }}</span>
          <span class="example-difficulty">{{ example.difficulty }}</span>
        </div>
        <h3>{{ example.title }}</h3>
        <p>{{ example.description }}</p>
        <div class="example-tags">
          {% for tag in example.tags limit:3 %}
          <span class="example-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        <div class="example-card-footer">
          <a href="{{ site.baseurl }}{{ example.url }}" class="example-link">
            View Example <i class="fas fa-arrow-right"></i>
          </a>
          {% if example.colab %}
          <a href="{{ example.colab }}" class="example-colab-icon" title="Run in Colab">
            <i class="fas fa-cloud"></i>
          </a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- Optimization Section -->
  <section class="example-category-section" data-category="optimization">
    <h2>⛰️ Optimization</h2>
    <p class="category-description">Global optimization using sampling techniques</p>
    <div class="examples-grid">
      {% for example in optimization_examples %}
      <div class="example-card" data-category="{{ example.category }}">
        <div class="example-card-header">
          <span class="example-icon">{{ example.icon }}</span>
          <span class="example-difficulty">{{ example.difficulty }}</span>
        </div>
        <h3>{{ example.title }}</h3>
        <p>{{ example.description }}</p>
        <div class="example-tags">
          {% for tag in example.tags limit:3 %}
          <span class="example-tag">{{ tag }}</span>
          {% endfor %}
        </div>
        <div class="example-card-footer">
          <a href="{{ site.baseurl }}{{ example.url }}" class="example-link">
            View Example <i class="fas fa-arrow-right"></i>
          </a>
          {% if example.colab %}
          <a href="{{ example.colab }}" class="example-colab-icon" title="Run in Colab">
            <i class="fas fa-cloud"></i>
          </a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </section>
</div>

<!-- Stats Section -->
<div class="examples-stats">
  <div class="stat-card">
    <span class="stat-number">{{ site.examples | size }}</span>
    <span class="stat-label">Total Examples</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ bayesian_examples | size }}</span>
    <span class="stat-label">Bayesian</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ physics_examples | size }}</span>
    <span class="stat-label">Physics</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ finance_examples | size }}</span>
    <span class="stat-label">Finance</span>
  </div>
  <div class="stat-card">
    <span class="stat-number">{{ optimization_examples | size }}</span>
    <span class="stat-label">Optimization</span>
  </div>
</div>

<style>
.examples-hero {
  text-align: center;
  margin: 2rem 0 3rem;
  padding: 2rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 10px;
  color: white;
}

.examples-hero h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.examples-hero p {
  font-size: 1.2rem;
  opacity: 0.95;
}

/* Filter Bar */
.filter-bar {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin: 2rem 0 3rem;
}

.filter-btn {
  padding: 0.6rem 1.5rem;
  border: none;
  background: white;
  color: #666;
  border-radius: 30px;
  cursor: pointer;
  font-size: 0.95rem;
  font-weight: 500;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.filter-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(102, 126, 234, 0.2);
}

.filter-btn.active {
  background: #667eea;
  color: white;
}

/* Category Sections */
.example-category-section {
  margin: 4rem 0;
  scroll-margin-top: 100px;
}

.example-category-section h2 {
  color: #333;
  font-size: 2rem;
  margin-bottom: 0.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 3px solid #667eea;
  display: inline-block;
}

.category-description {
  color: #666;
  margin-bottom: 2rem;
  font-size: 1.1rem;
}

/* Examples Grid */
.examples-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.example-card {
  background: white;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  border: 1px solid #f0f0f0;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.example-card::before {
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

.example-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(102, 126, 234, 0.2);
}

.example-card:hover::before {
  transform: scaleX(1);
}

.example-card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.example-icon {
  font-size: 2rem;
}

.example-difficulty {
  background: #f0f0f0;
  padding: 0.3rem 1rem;
  border-radius: 20px;
  font-size: 0.8rem;
  color: #666;
}

.example-card h3 {
  color: #333;
  margin-bottom: 0.8rem;
  font-size: 1.2rem;
}

.example-card p {
  color: #666;
  margin-bottom: 1rem;
  line-height: 1.5;
  font-size: 0.95rem;
  flex-grow: 1;
}

.example-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.example-tag {
  background: #f0f0f0;
  padding: 0.2rem 0.8rem;
  border-radius: 15px;
  font-size: 0.75rem;
  color: #666;
}

.example-card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: auto;
  padding-top: 0.5rem;
  border-top: 1px solid #f0f0f0;
}

.example-link {
  color: #667eea;
  text-decoration: none;
  font-weight: 500;
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  transition: gap 0.3s ease;
}

.example-link:hover {
  gap: 0.5rem;
}

.example-colab-icon {
  color: #f9ab00;
  font-size: 1.2rem;
  transition: transform 0.3s ease;
}

.example-colab-icon:hover {
  transform: scale(1.2);
}

/* Stats Section */
.examples-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1.5rem;
  margin: 4rem 0 2rem;
  padding: 2rem;
  background: white;
  border-radius