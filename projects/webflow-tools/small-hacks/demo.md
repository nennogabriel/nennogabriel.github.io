---
layout: default
title: Small Hacks Demo - Webflow Tools
permalink: /projects/webflow-tools/small-hacks/demo/
---

<div class="demo-page">
  <div class="breadcrumb">
    <a href="{{ '/' | relative_url }}">Home</a> > 
    <a href="{{ '/projects/webflow-tools/' | relative_url }}">Webflow Tools</a> > 
    <a href="{{ '/projects/webflow-tools/small-hacks/' | relative_url }}">Small Hacks</a> > 
    Demo
  </div>

  <h1>🧪 Small Hacks Demo</h1>

  <div class="demo-intro">
    <p>
      This page demonstrates the Small Hacks in action. You can test each functionality and see how it works in real-time.
      <strong>Note:</strong> The hacks are already implemented on this page for demonstration purposes.
    </p>
  </div>

  <div class="demo-section">
    <h2>🔗 External Links Auto-Target Demo</h2>
    
    <div class="demo-description">
      <p>
        The following links demonstrate the external links auto-target functionality. 
        External links (starting with "http") should automatically open in a new tab, 
        while internal links stay in the same tab.
      </p>
    </div>

    <div class="demo-content">
      <div class="link-test-grid">
        <div class="link-group">
          <h3>External Links (should open in new tab)</h3>
          <ul class="demo-links">
            <li><a href="https://webflow.com">Webflow Official Site</a></li>
            <li><a href="https://github.com">GitHub</a></li>
            <li><a href="https://developer.mozilla.org">MDN Web Docs</a></li>
            <li><a href="http://example.com">Example.com (HTTP)</a></li>
          </ul>
        </div>

        <div class="link-group">
          <h3>Internal Links (should stay in same tab)</h3>
          <ul class="demo-links">
            <li><a href="{{ '/' | relative_url }}">Home Page</a></li>
            <li><a href="{{ '/projects/webflow-tools/' | relative_url }}">Webflow Tools</a></li>
            <li><a href="{{ '/projects/webflow-tools/small-hacks/' | relative_url }}">Small Hacks</a></li>
            <li><a href="#demo-section">Link to section on this page</a></li>
          </ul>
        </div>
      </div>

      <div class="demo-controls">
        <h3>Dynamic Content Test</h3>
        <p>Click the button below to add new external links dynamically. The hack should automatically apply to these new links too.</p>
        <button id="add-links-btn" class="demo-btn">Add Dynamic External Links</button>
        <div id="dynamic-links-container"></div>
      </div>
    </div>

    <div class="demo-status">
      <h3>Status Check</h3>
      <div id="status-container">
        <div class="status-item">
          <span class="status-label">External Links Found:</span>
          <span id="external-count" class="status-value">-</span>
        </div>
        <div class="status-item">
          <span class="status-label">Links with target="_blank":</span>
          <span id="target-blank-count" class="status-value">-</span>
        </div>
        <div class="status-item">
          <span class="status-label">Hack Status:</span>
          <span id="hack-status" class="status-value">-</span>
        </div>
      </div>
      <button id="refresh-status-btn" class="demo-btn secondary">Refresh Status</button>
    </div>
  </div>

  <div class="demo-section coming-soon">
    <h2>⚡ More Demos Coming Soon</h2>
    <p>
      As new hacks are added to the Small Hacks collection, their demos will appear here. 
      Stay tuned for more interactive demonstrations!
    </p>
  </div>

  <div class="back-link">
    <a href="{{ '/projects/webflow-tools/small-hacks/' | relative_url }}">&larr; Back to Small Hacks</a>
  </div>
</div>

<style>
.demo-page {
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

.demo-intro {
  background-color: #e3f2fd;
  border: 1px solid #2196f3;
  border-radius: 8px;
  padding: 1rem;
  margin-bottom: 2rem;
}

.demo-section {
  background-color: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 2rem;
}

.demo-section.coming-soon {
  background-color: #f8f9fa;
  border-style: dashed;
  text-align: center;
}

.demo-description {
  background-color: #f8f9fa;
  padding: 1rem;
  border-radius: 6px;
  margin-bottom: 1.5rem;
}

.link-test-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.link-group {
  background-color: #f8f9fa;
  padding: 1rem;
  border-radius: 6px;
}

.link-group h3 {
  margin-top: 0;
  color: #0366d6;
}

.demo-links {
  list-style: none;
  padding: 0;
}

.demo-links li {
  margin-bottom: 0.5rem;
}

.demo-links a {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: #fff;
  border: 1px solid #e1e4e8;
  border-radius: 4px;
  text-decoration: none;
  color: #0366d6;
  transition: all 0.2s ease;
}

.demo-links a:hover {
  background-color: #f1f3f4;
  border-color: #0366d6;
}

.demo-controls {
  background-color: #fff3cd;
  border: 1px solid #ffc107;
  border-radius: 6px;
  padding: 1rem;
  margin-bottom: 2rem;
}

.demo-controls h3 {
  margin-top: 0;
  color: #856404;
}

.demo-btn {
  background-color: #0366d6;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.9rem;
  font-weight: 500;
  transition: background-color 0.2s ease;
}

.demo-btn:hover {
  background-color: #0256cc;
}

.demo-btn.secondary {
  background-color: #6c757d;
}

.demo-btn.secondary:hover {
  background-color: #5a6268;
}

#dynamic-links-container {
  margin-top: 1rem;
  padding: 1rem;
  background-color: #f8f9fa;
  border-radius: 4px;
  min-height: 50px;
}

.demo-status {
  background-color: #d4edda;
  border: 1px solid #28a745;
  border-radius: 6px;
  padding: 1rem;
}

.demo-status h3 {
  margin-top: 0;
  color: #155724;
}

#status-container {
  margin-bottom: 1rem;
}

.status-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 0;
  border-bottom: 1px solid #c3e6cb;
}

.status-item:last-child {
  border-bottom: none;
}

.status-label {
  font-weight: 500;
  color: #155724;
}

.status-value {
  font-weight: bold;
  color: #0f5132;
  background-color: #a3d9a4;
  padding: 0.25rem 0.5rem;
  border-radius: 4px;
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
  .demo-page {
    padding: 1rem;
  }
  
  .link-test-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  
  .status-item {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.25rem;
  }
}
</style>

<script>
// External Links Auto-Target Hack (Demo Implementation)
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
  document.addEventListener('DOMContentLoaded', function() {
    setExternalLinksTarget();
    updateStatus();
  });
  
  // Run when new content is added (for dynamic content)
  const observer = new MutationObserver(function() {
    setExternalLinksTarget();
    updateStatus();
  });
  observer.observe(document.body, {
    childList: true,
    subtree: true
  });

  // Demo functionality
  let dynamicLinkCounter = 0;

  function updateStatus() {
    const externalLinks = document.querySelectorAll('a[href^="http"]');
    const targetBlankLinks = document.querySelectorAll('a[target="_blank"]');
    
    document.getElementById('external-count').textContent = externalLinks.length;
    document.getElementById('target-blank-count').textContent = targetBlankLinks.length;
    
    const hackWorking = externalLinks.length === targetBlankLinks.length && externalLinks.length > 0;
    const statusElement = document.getElementById('hack-status');
    statusElement.textContent = hackWorking ? '✅ Working' : '❌ Not Working';
    statusElement.style.backgroundColor = hackWorking ? '#28a745' : '#dc3545';
  }

  function addDynamicLinks() {
    dynamicLinkCounter++;
    const container = document.getElementById('dynamic-links-container');
    
    const linkDiv = document.createElement('div');
    linkDiv.style.marginBottom = '0.5rem';
    linkDiv.innerHTML = `
      <strong>Dynamic Set ${dynamicLinkCounter}:</strong>
      <a href="https://example${dynamicLinkCounter}.com" style="margin-left: 0.5rem; color: #0366d6;">Dynamic External Link ${dynamicLinkCounter}</a>
    `;
    
    container.appendChild(linkDiv);
  }

  // Event listeners
  document.addEventListener('DOMContentLoaded', function() {
    document.getElementById('add-links-btn').addEventListener('click', addDynamicLinks);
    document.getElementById('refresh-status-btn').addEventListener('click', updateStatus);
  });
})();
</script>