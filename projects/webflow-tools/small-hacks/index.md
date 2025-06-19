---
layout: default
title: Small Hacks - Webflow Tools
permalink: /projects/webflow-tools/small-hacks/
---

<div class="project-detail">
  <div class="breadcrumb">
    <a href="{{ '/' | relative_url }}">Home</a> > 
    <a href="{{ '/projects/webflow-tools/' | relative_url }}">Webflow Tools</a> > 
    Small Hacks
  </div>

  <h1>Small Hacks</h1>

  <div class="project-meta">
    <span class="status active">Active</span>
    <span class="category">JavaScript Utilities</span>
  </div>

  <div class="project-overview">
    <h2>Overview</h2>
    <p>
      Small Hacks is a collection of lightweight JavaScript solutions that enhance Webflow functionality with minimal code.
      These hacks solve common problems and add useful features that aren't built into Webflow by default.
    </p>
  </div>

  <div class="quick-links">
    <h2>Quick Access</h2>
    <div class="link-grid">
      <a href="{{ '/projects/webflow-tools/small-hacks/demo/' | relative_url }}" class="quick-link demo">
        <div class="link-icon">🧪</div>
        <div class="link-content">
          <h3>Live Demo</h3>
          <p>Test all hacks in action</p>
        </div>
      </a>
      <a href="#external-links" class="quick-link docs">
        <div class="link-icon">📖</div>
        <div class="link-content">
          <h3>Documentation</h3>
          <p>Implementation guides</p>
        </div>
      </a>
    </div>
  </div>

  <div class="hacks-list">
    <h2>Available Hacks</h2>

    <div class="hack-item" id="external-links">
      <div class="hack-header">
        <h3>🔗 External Links Auto-Target</h3>
        <span class="hack-status ready">Ready</span>
      </div>
      
      <div class="hack-description">
        <p>
          Automatically opens external links (starting with "http") in a new tab/window. 
          This hack improves user experience by keeping visitors on your site while allowing them to explore external resources.
        </p>
      </div>

      <div class="hack-features">
        <h4>Features:</h4>
        <ul>
          <li>Automatically detects external links (href starting with "http")</li>
          <li>Adds <code>target="_blank"</code> and <code>rel="noopener noreferrer"</code></li>
          <li>Works with dynamically added content</li>
          <li>Lightweight and performance-optimized</li>
          <li>No configuration required</li>
        </ul>
      </div>

      <div class="hack-implementation">
        <h4>Implementation:</h4>
        <div class="code-block">
          <div class="code-header">
            <span>JavaScript</span>
            <button class="copy-btn" onclick="copyCode('external-links-code')">Copy</button>
          </div>
          <pre id="external-links-code"><code>// External Links Auto-Target Hack
(function() {
  'use strict';
  
  function setExternalLinksTarget() {
    // Select all links that start with http (external links)
    const externalLinks = document.querySelectorAll('a[href^="http"]');
    
    externalLinks.forEach(link => {
      // Skip if already has target set
      if (!link.hasAttribute('target')) {
        link.setAttribute('target', '_blank');
        link.setAttribute('rel', 'noopener noreferrer');
      }
    });
  }
  
  // Run on page load
  document.addEventListener('DOMContentLoaded', setExternalLinksTarget);
  
  // Run when new content is added (for dynamic content)
  const observer = new MutationObserver(setExternalLinksTarget);
  observer.observe(document.body, {
    childList: true,
    subtree: true
  });
})();</code></pre>
        </div>
      </div>

      <div class="hack-usage">
        <h4>How to Use in Webflow:</h4>
        <ol>
          <li>Copy the JavaScript code above</li>
          <li>In Webflow Designer, go to Project Settings > Custom Code</li>
          <li>Paste the code in the "Footer Code" section (before &lt;/body&gt; tag)</li>
          <li>Publish your site</li>
          <li>All external links will now open in new tabs automatically</li>
        </ol>
      </div>
    </div>

    <div class="hack-item coming-soon">
      <div class="hack-header">
        <h3>⚡ More Hacks Coming Soon</h3>
        <span class="hack-status planning">Planning</span>
      </div>
      
      <div class="hack-description">
        <p>Additional small hacks are being developed, including:</p>
        <ul>
          <li>Smooth scroll enhancements</li>
          <li>Form validation helpers</li>
          <li>Image lazy loading optimizations</li>
          <li>Custom cursor effects</li>
          <li>And more...</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="back-link">
    <a href="{{ '/projects/webflow-tools/' | relative_url }}">&larr; Back to Webflow Tools</a>
  </div>
</div>

<style>
.project-detail {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

.breadcrumb {
  margin-bottom: 1rem;
  color: #586069;
  font-size: 0.9rem;
}

.breadcrumb a {
  color: #0366d6;
  text-decoration: none;
}

.breadcrumb a:hover {
  text-decoration: underline;
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

.quick-links {
  margin-bottom: 2.5rem;
}

.link-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}

.quick-link {
  display: flex;
  align-items: center;
  padding: 1rem;
  border: 2px solid #e1e4e8;
  border-radius: 8px;
  text-decoration: none;
  color: inherit;
  transition: all 0.2s ease;
}

.quick-link:hover {
  border-color: #0366d6;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.quick-link.demo {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-color: transparent;
}

.quick-link.docs {
  background-color: #f8f9fa;
}

.link-icon {
  font-size: 2rem;
  margin-right: 1rem;
}

.link-content h3 {
  margin: 0 0 0.25rem 0;
  font-size: 1.1rem;
}

.link-content p {
  margin: 0;
  font-size: 0.9rem;
  opacity: 0.8;
}

.hacks-list {
  margin-bottom: 2.5rem;
}

.hack-item {
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 2rem;
  background-color: #fff;
}

.hack-item.coming-soon {
  background-color: #f8f9fa;
  border-style: dashed;
}

.hack-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  flex-wrap: wrap;
}

.hack-header h3 {
  margin: 0;
  color: #24292e;
}

.hack-status {
  padding: 0.25rem 0.75rem;
  border-radius: 12px;
  font-size: 0.75rem;
  font-weight: bold;
  text-transform: uppercase;
}

.hack-status.ready {
  background-color: #28a745;
  color: white;
}

.hack-status.planning {
  background-color: #ffc107;
  color: #212529;
}

.hack-description {
  margin-bottom: 1.5rem;
}

.hack-features, .hack-implementation, .hack-usage {
  margin-bottom: 1.5rem;
}

.hack-features h4, .hack-implementation h4, .hack-usage h4 {
  color: #0366d6;
  margin-bottom: 0.5rem;
}

.code-block {
  background-color: #f6f8fa;
  border: 1px solid #e1e4e8;
  border-radius: 6px;
  overflow: hidden;
}

.code-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 1rem;
  background-color: #e1e4e8;
  font-size: 0.875rem;
  font-weight: 600;
}

.copy-btn {
  background-color: #0366d6;
  color: white;
  border: none;
  padding: 0.25rem 0.5rem;
  border-radius: 4px;
  cursor: pointer;
  font-size: 0.75rem;
}

.copy-btn:hover {
  background-color: #0256cc;
}

pre {
  margin: 0;
  padding: 1rem;
  overflow-x: auto;
  font-family: 'Monaco', 'Menlo', 'Ubuntu Mono', monospace;
  font-size: 0.875rem;
  line-height: 1.4;
}

code {
  background-color: #f1f3f4;
  padding: 0.125rem 0.25rem;
  border-radius: 3px;
  font-family: 'Monaco', 'Menlo', 'Ubuntu Mono', monospace;
  font-size: 0.875rem;
}

.hack-usage ol {
  padding-left: 1.5rem;
}

.hack-usage li {
  margin-bottom: 0.5rem;
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
  
  .hack-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
  
  .link-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<script>
function copyCode(elementId) {
  const codeElement = document.getElementById(elementId);
  const text = codeElement.textContent;
  
  navigator.clipboard.writeText(text).then(function() {
    // Show feedback
    const btn = event.target;
    const originalText = btn.textContent;
    btn.textContent = 'Copied!';
    btn.style.backgroundColor = '#28a745';
    
    setTimeout(() => {
      btn.textContent = originalText;
      btn.style.backgroundColor = '#0366d6';
    }, 2000);
  });
}
</script>