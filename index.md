---
layout: default
title: Home
---
<div class="welcome-section" style="background-image: url('{{ site.baseurl }}/assets/images/background.png');">
  <div class="welcome-overlay">
    <div class="container">
      <h2>Welcome to the Sampling Algorithms Lab</h2>
      <p>We develop and study sampling methods for machine learning, Bayesian inference, and computational science.</p>
    </div>
  </div><br>
  <div class="quick-links">
    <a href="{{ site.baseurl }}/start" class="quick-link">
      <span class="quick-icon">🚀</span>
      <span>Get Started</span>
    </a>
    <a href="{{ site.baseurl }}/sampling-tools" class="quick-link">
      <span class="quick-icon">🔧</span>
      <span>Sampling Tools</span>
    </a>
    <a href="{{ site.baseurl }}/examples" class="quick-link">
      <span class="quick-icon">💡</span>
      <span>Examples</span>
    </a>
    <a href="{{ site.baseurl }}/projects" class="quick-link">
      <span class="quick-icon">📚</span>
      <span>Projects</span>
    </a>
  </div>
</div>


<!-- Latest Tutorials -->
<div class="latest-tutorials">
  <h2>📖 Latest Tutorials</h2>
  <div class="tutorial-preview">
    {% for post in site.posts limit:2 %}
    <div class="preview-card">
      <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More →</a>
    </div>
    {% endfor %}
  </div>
</div>

<!-- Add the CSS styles (same as before) -->
<style>
/* Copy all the styles from the previous message */
.top-nav {
  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 1.5rem;
  background: white;
  border-bottom: 2px solid #f0f0f0;
  margin-bottom: 2rem;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.nav-link {
  color: #333;
  text-decoration: none;
  font-size: 1.1rem;
  font-weight: 500;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.nav-link:hover {
  color: #667eea;
  background: #f8f9fa;
}

.hero-section {
  text-align: center;
  margin-bottom: 3rem;
}

.hero-section h1 {
  font-size: 2.5rem;
  color: #333;
  margin-bottom: 0.5rem;
}

.subtitle {
  font-size: 1.2rem;
  color: #666;
  margin-bottom: 2rem;
}


.welcome-section {
  text-align: center;
  width: 100%;
  margin: 0 0 4rem 0;   /* top=0, right=0, bottom=4rem, left=0 */
}

.welcome-section h2 {
  font-size: 2rem;
  color: #fcfcfc;
  margin-bottom: 1rem;
}

.welcome-section p {
  color: #fcfcfc;
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

.quick-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.quick-link {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  color: #333;
  padding: 1.5rem;
  border-radius: 10px;
  background: #f8f9fa;
  transition: all 0.3s ease;
  min-width: 150px;
}

.quick-link:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
  background: #667eea;
  color: white;
}

.quick-icon {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.latest-tutorials {
  margin: 4rem 0;
}

.latest-tutorials h2 {
  font-size: 2rem;
  color: #333;
  margin-bottom: 2rem;
  text-align: center;
}

.tutorial-preview {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.preview-card {
  background: white;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  border: 1px solid #f0f0f0;
}

.preview-card h3 {
  margin-bottom: 0.5rem;
}

.preview-card h3 a {
  color: #667eea;
  text-decoration: none;
}

.post-meta {
  color: #999;
  font-size: 0.9rem;
  margin-bottom: 1rem;
}

.read-more {
  display: inline-block;
  margin-top: 1rem;
  color: #667eea;
  text-decoration: none;
  font-weight: 500;
}

@media (max-width: 768px) {
  .top-nav {
    gap: 1rem;
    padding: 1rem;
    flex-wrap: wrap;
  }
  
  .quick-links {
    gap: 1rem;
  }
  
  .quick-link {
    min-width: 120px;
    padding: 1rem;
  }
}
</style>