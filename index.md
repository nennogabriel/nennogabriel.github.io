---
layout: default
---

<div class="home">
  <h1 class="page-heading">Welcome to My Portfolio</h1>
  
  <p>Hi! I'm Pedro Moreno, a web developer passionate about creating efficient tools and solutions for modern web development.</p>
  
  <h2>Featured Projects</h2>
  
  <div class="project-list">
    <div class="project-item">
      <h3>
        <a href="{{ '/projects/webflow-tools/' | relative_url }}">Webflow Tools</a>
      </h3>
      <p class="project-description">
        A comprehensive collection of tools and utilities designed to enhance Webflow development workflow. 
        This project includes automation scripts, custom components, and productivity enhancers for Webflow developers.
      </p>
      <div class="project-tags">
        <span class="tag">Webflow</span>
        <span class="tag">JavaScript</span>
        <span class="tag">Automation</span>
        <span class="tag">Tools</span>
      </div>
      <p class="project-status">
        <strong>Status:</strong> Active Development
      </p>
    </div>
  </div>
  
  <div class="coming-soon">
    <h3>More Projects Coming Soon</h3>
    <p>I'm constantly working on new tools and solutions. Check back regularly for updates!</p>
  </div>
</div>

<style>
.project-list {
  margin: 2rem 0;
}

.project-item {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  background-color: #f8f9fa;
}

.project-item h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.project-item h3 a {
  color: #0366d6;
  text-decoration: none;
}

.project-item h3 a:hover {
  text-decoration: underline;
}

.project-description {
  color: #586069;
  margin-bottom: 1rem;
  line-height: 1.5;
}

.project-tags {
  margin-bottom: 1rem;
}

.tag {
  display: inline-block;
  background-color: #0366d6;
  color: white;
  padding: 0.25rem 0.5rem;
  border-radius: 4px;
  font-size: 0.875rem;
  margin-right: 0.5rem;
  margin-bottom: 0.25rem;
}

.project-status {
  color: #28a745;
  font-size: 0.9rem;
  margin-bottom: 0;
}

.coming-soon {
  margin-top: 3rem;
  padding: 1.5rem;
  background-color: #f1f3f4;
  border-radius: 8px;
  text-align: center;
}

.coming-soon h3 {
  color: #586069;
  margin-bottom: 0.5rem;
}

.coming-soon p {
  color: #6a737d;
  margin-bottom: 0;
}
</style>