---
layout: default
title: System Maintenance
nav: lab
---

<style>
/* Arrière-plan binaire global fusionné */
body {
  background-color: #0a0e1a;
  background-image: 
    linear-gradient(rgba(10, 14, 26, 0.9), rgba(10, 14, 26, 0.9)),
    url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'%3E%3Ctext x='10' y='30' fill='rgba(59, 130, 246, 0.05)' font-family='monospace' font-size='12'%3E01101%3C/text%3E%3Ctext x='50' y='70' fill='rgba(59, 130, 246, 0.05)' font-family='monospace' font-size='12'%3E10101%3C/text%3E%3Ctext x='80' y='20' fill='rgba(59, 130, 246, 0.05)' font-family='monospace' font-size='12'%3E01%3C/text%3E%3Ctext x='30' y='90' fill='rgba(59, 130, 246, 0.05)' font-family='monospace' font-size='12'%3E110%3C/text%3E%3C/svg%3E");
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes pulse {
  0%, 100% { box-shadow: 0 0 20px rgba(59, 130, 246, 0.3); }
  50% { box-shadow: 0 0 30px rgba(59, 130, 246, 0.6); }
}

/* Élargissement du conteneur principal */
.article-container {
  max-width: 1200px; /* Augmenté de 900px à 1200px */
  margin: 0 auto;
  padding: 40px 20px;
  animation: fadeIn 0.8s ease-out;
}

.article-header {
  text-align: center;
  margin-bottom: 60px;
  padding: 40px;
  background: rgba(15, 23, 42, 0.85);
  border: 2px solid #3b82f6;
  border-radius: 20px;
  position: relative;
  overflow: hidden;
}

.article-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(59, 130, 246, 0.1), transparent);
  animation: scan 3s infinite;
}

@keyframes scan {
  0% { left: -100%; }
  100% { left: 100%; }
}

.badge-number {
  display: inline-block;
  width: 60px;
  height: 60px;
  line-height: 60px;
  background: linear-gradient(135deg, #3b82f6, #2563eb);
  border-radius: 50%;
  color: white;
  font-size: 2em;
  font-weight: bold;
  margin-bottom: 20px;
  box-shadow: 0 0 20px rgba(59, 130, 246, 0.5);
}

.article-title {
  font-size: 3.5em; /* Légèrement augmenté pour l'affichage large */
  color: #60a5fa;
  margin: 20px 0;
  font-weight: 900;
  letter-spacing: 3px;
  text-shadow: 0 0 20px rgba(96, 165, 250, 0.5);
}

.article-subtitle {
  color: #94a3b8;
  font-size: 1.2em;
  line-height: 1.6;
  max-width: 800px;
  margin: 0 auto;
}

.status-badge {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 10px 20px;
  background: rgba(59, 130, 246, 0.1);
  border: 1px solid #3b82f6;
  border-radius: 20px;
  color: #60a5fa;
  font-size: 0.9em;
  margin-top: 20px;
}

.status-dot {
  width: 8px;
  height: 8px;
  background: #3b82f6;
  border-radius: 50%;
  animation: pulse 2s infinite;
}

.content-section {
  background: rgba(15, 23, 42, 0.7);
  border: 1px solid rgba(59, 130, 246, 0.3);
  border-radius: 15px;
  padding: 50px; /* Padding augmenté pour accompagner l'élargissement */
  margin: 30px 0;
}

.content-section h2 {
  color: #3b82f6;
  font-size: 2.2em;
  margin-bottom: 25px;
  padding-bottom: 15px;
  border-bottom: 2px solid rgba(59, 130, 246, 0.3);
}

.content-section h3 {
  color: #60a5fa;
  font-size: 1.6em;
  margin: 35px 0 20px 0;
}

.content-section p {
  color: #cbd5e1;
  line-height: 1.8;
  margin: 15px 0;
  font-size: 1.1em;
}

.code-block {
  background: rgba(10, 14, 26, 0.8);
  border: 1px solid #1e40af;
  border-radius: 10px;
  padding: 25px;
  margin: 25px 0;
  overflow-x: auto;
}

.code-block pre {
  margin: 0;
  color: #60a5fa;
  font-family: 'Courier New', monospace;
  font-size: 1.1em;
  line-height: 1.8;
}

.command-line {
  color: #3b82f6;
  font-family: 'Courier New', monospace;
  background: rgba(10, 14, 26, 0.6);
  padding: 5px 10px;
  border-radius: 4px;
  font-size: 1.05em;
}

.info-box, .warning-box {
  padding: 25px;
  margin: 25px 0;
  border-radius: 8px;
}

.info-box {
  background: rgba(59, 130, 246, 0.1);
  border-left: 5px solid #3b82f6;
}

.warning-box {
  background: rgba(239, 68, 68, 0.1);
  border-left: 5px solid #ef4444;
}

.step-list li {
  counter-increment: step-counter;
  margin: 40px 0;
  padding-left: 70px;
  position: relative;
}

.step-list li::before {
  content: counter(step-counter);
  position: absolute;
  left: 0;
  top: 0;
  width: 45px;
  height: 45px;
  line-height: 45px;
  text-align: center;
  background: linear-gradient(135deg, #3b82f6, #2563eb);
  color: white;
  border-radius: 50%;
  font-weight: bold;
}

.key-points {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
  margin: 35px 0;
}

.key-point {
  background: rgba(15, 23, 42, 0.6);
  border: 1px solid #1e40af;
  border-radius: 12px;
  padding: 25px;
  transition: all 0.3s;
}

.key-point:hover {
  transform: translateY(-8px);
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.2);
}

.script-container {
  background: rgba(10, 14, 26, 0.9);
  border: 2px solid #3b82f6;
  border-radius: 15px;
  padding: 40px;
  margin: 40px 0;
}

table {
  width: 100%;
  margin: 25px 0;
  font-size: 1.05em;
}

table th, table td {
  padding: 20px;
}

.article-footer {
  text-align: center;
  margin-top: 80px;
  padding: 40px;
  background: rgba(15, 23, 42, 0.5);
  border-radius: 20px;
  border-top: 2px solid rgba(59, 130, 246, 0.3);
}

@media (max-width: 1240px) {
  .article-container { max-width: 95%; }
}

@media (max-width: 768px) {
  .article-title { font-size: 2.2em; }
  .content-section { padding: 25px; }
}
</style>

<div class="article-container">
  <div class="article-header">
    <div class="badge-number">2</div>
    <h1 class="article-title">SYSTEM MAINTENANCE</h1>
    <p class="article-subtitle">Essential commands and practices to keep your Arch system healthy and running smoothly without breaking things.</p>
    <div class="status-badge">
      <span class="status-dot"></span>
      <span>ARCH LINUX LAB SERIES</span>
    </div>
  </div>

  <div class="content-section">
    <h2>Why Regular Maintenance</h2>
    <p>Arch Linux follows a rolling release model. Unlike Ubuntu or Fedora, Arch requires regular maintenance to stay clean and performant. A weekly 15-minute routine prevents file accumulation and keeps your system stable.</p>
    
   <div class="key-points">
      <div class="key-point">
        <h4>Clean System</h4>
        <p>Remove unused packages and cached files</p>
      </div>
      <div class="key-point">
        <h4>Optimal Performance</h4>
        <p>Keep disk space free and services running</p>
      </div>
      <div class="key-point">
        <h4>Prevent Issues</h4>
        <p>Catch problems before they become critical</p>
      </div>
    </div>
  </div>

  <div class="content-section">
    <h2>Weekly Routine in 9 Steps</h2>
    <ul class="step-list">
      <li>
        <h3>Check Arch News</h3>
        <p>Always visit <span class="command-line">archlinux.org/news</span> before updating. Some updates require manual intervention.</p>
      </li>
      <li>
        <h3>Update System</h3>
        <div class="code-block">
<pre><code># With pacman
sudo pacman -Syu

# With yay (AUR helper)
yay -Syu</code></pre>
        </div>
        <div class="info-box">
          <strong>Important:</strong> Always reboot after kernel updates.
        </div>
      </li>
      <li>
        <h3>Clean Package Cache</h3>
        <div class="code-block">
<pre><code>sudo paccache -r
sudo paccache -ruk0</code></pre>
</div>
        <p>This typically frees 500 MB to 2 GB of space.</p>
      </li>
      <li>
        <h3>Manage Configuration Files</h3>
        <div class="code-block">
<pre><code>sudo DIFFPROG=vimdiff pacdiff</code></pre>
        </div>
        <p>Merge .pacnew and .pacsave files after updates.</p>
      </li>
    </ul>
  </div>

  <div class="article-footer">
    <p class="article-meta">ARCH LINUX LAB SERIES — ARTICLE 2/5</p>
    <p class="article-meta">Published January 16, 2026</p>
    <a href="/my-lab/" class="back-link">← BACK TO LAB</a>
  </div>
</div>
