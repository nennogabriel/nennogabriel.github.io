---
layout: default
title: Webflow Tools
permalink: /projects/webflow-tools/
---

<div class="project-detail">
  <h1>{{ page.title }}</h1>

  <div class="project-meta">
    <span class="status active">Active Development</span>
    <span class="category">Web Development Tools Collection</span>
  </div>

  <div class="project-overview">
    <h2>Overview</h2>
    <p>
      Webflow Tools is a comprehensive collection of micro-projects and utilities designed to enhance the Webflow development experience.
      Each tool focuses on solving specific challenges and improving productivity for Webflow developers.
    </p>
  </div>

  <div class="micro-projects">
    <h2>Micro Projects</h2>
    
    <div class="project-grid">
      <div class="micro-project-card">
        <h3>
          <a href="{{ '/projects/webflow-tools/small-hacks/' | relative_url }}">Small Hacks</a>
        </h3>
        <p class="project-description">
          A collection of small JavaScript hacks and tricks to enhance Webflow functionality. 
          Includes automatic external link handling, UI improvements, and productivity shortcuts.
        </p>
        <div class="project-tags">
          <span class="tag">JavaScript</span>
          <span class="tag">Hacks</span>
          <span class="tag">Productivity</span>
        </div>
        <div class="project-status">
          <span class="status-badge active">Active</span>
        </div>
      </div>

      <div class="micro-project-card">
        <h3>
          <a href="{{ '/projects/webflow-tools/cookie-consent/' | relative_url }}">Cookie Consent</a>
        </h3>
        <p class="project-description">
          A customizable and GDPR-compliant cookie consent solution specifically designed for Webflow sites.
          Easy to implement and fully customizable to match your site's design.
        </p>
        <div class="project-tags">
          <span class="tag">GDPR</span>
          <span class="tag">Privacy</span>
          <span class="tag">Compliance</span>
        </div>
        <div class="project-status">
          <span class="status-badge planning">Planning</span>
        </div>
      </div>

      <div class="micro-project-card">
        <h3>
          <span class="coming-soon-title">More Tools Coming Soon</span>
        </h3>
        <p class="project-description">
          Additional micro-projects are in development. Each tool will focus on solving specific Webflow challenges
          and improving the overall development experience.
        </p>
        <div class="project-tags">
          <span class="tag">Coming Soon</span>
        </div>
        <div class="project-status">
          <span class="status-badge planning">In Planning</span>
        </div>
      </div>
    </div>
  </div>

  <div class="tech-stack">
    <h2>Technologies Used</h2>
    <div class="tech-tags">
      <span class="tech-tag">JavaScript</span>
      <span class="tech-tag">HTML/CSS</span>
      <span class="tech-tag">Webflow</span>
      <span class="tech-tag">GDPR Compliance</span>
    </div>
  </div>

  <div class="back-link">
    <a href="{{ '/' | relative_url }}">&larr; Back to Home</a>
  </div>
</div>

<style>
.project-detail {
  max-width: 1000px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

.project-meta {
  margin-bottom: 2rem;
}

.status {
  display: inline-block;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: bold;
  margin-right: 1rem;
}

.status.active {
  background-color: #28a745;
  color: white;
}

.category {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: #f1f3f4;
  border-radius: 20px;
  font-size: 0.875rem;
  color: #586069;
}

.project-overview, .micro-projects, .tech-stack {
  margin-bottom: 2.5rem;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

.micro-project-card {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 1.5rem;
  background-color: #f8f9fa;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.micro-project-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.micro-project-card h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.micro-project-card h3 a {
  color: #0366d6;
  text-decoration: none;
}

.micro-project-card h3 a:hover {
  text-decoration: underline;
}

.coming-soon-title {
  color: #586069;
  font-style: italic;
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
  margin-bottom: 0;
}

.status-badge {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  border-radius: 12px;
  font-size: 0.75rem;
  font-weight: bold;
  text-transform: uppercase;
}

.status-badge.active {
  background-color: #28a745;
  color: white;
}

.status-badge.planning {
  background-color: #ffc107;
  color: #212529;
}

.tech-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech-tag {
  background-color: #0366d6;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  font-size: 0.875rem;
}

.back-link {
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid #e1e4e8;
}

.back-link a {
  color: #0366d6;
  text-decoration: none;
  font-weight: 500;
}

.back-link a:hover {
  text-decoration: underline;
}

@media (max-width: 768px) {
  .project-detail {
    padding: 1rem;
  }

  .project-grid {
    grid-template-columns: 1fr;
  }

  .tech-tags {
    flex-direction: column;
  }

  .tech-tag {
    text-align: center;
  }
}
</style>