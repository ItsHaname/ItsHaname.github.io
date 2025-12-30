---
layout: default
title: Accueil
nav: home
---

<style>
.cyber-container { max-width: 800px; margin: auto; padding: 20px; }
.cyber-header { text-align: center; margin-bottom: 40px; }
.cyber-name { color: #ff6b9d; font-size: 2.5em; margin-bottom: 5px; }
.cyber-subtitle { color: #8a8dff; font-size: 1.2em; }
.cyber-nav { display: flex; justify-content: center; gap: 20px; margin: 30px 0; flex-wrap: wrap; }
.cyber-nav a { color: #58a6ff; text-decoration: none; padding: 8px 16px; border: 1px solid #30363d; border-radius: 6px; transition: 0.3s; }
.cyber-nav a:hover { background: #1a1f29; }
.cyber-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin: 40px 0; }
.cyber-card { background: #0d1117; border: 1px solid #30363d; border-radius: 10px; padding: 20px; transition: 0.3s; }
.cyber-card:hover { border-color: #8a8dff; transform: translateY(-5px); }
.cyber-card h3 { color: #ff6b9d; margin-top: 0; }
.cyber-badges { display: flex; gap: 15px; justify-content: center; margin: 30px 0; flex-wrap: wrap; }
.cyber-badge { background: #161b22; color: #c9d1d9; padding: 8px 16px; border-radius: 20px; border: 1px solid #30363d; }
.cyber-footer { text-align: center; margin-top: 50px; color: #8b949e; font-size: 0.9em; }
@media (max-width: 600px) { .cyber-nav { flex-direction: column; align-items: center; } .cyber-grid { grid-template-columns: 1fr; } }
</style>

<div class="cyber-container">

<div class="cyber-header">
  <h1 class="cyber-name">🛡️ Haname</h1>
  <p class="cyber-subtitle">Étudiante en Cybersécurité – FSSM</p>
</div>

<div class="cyber-nav">
  <a href="#about">À propos</a>
  <a href="#fssm">FSSM</a>
  <a href="#tryhackme">TryHackMe</a>
  <a href="#lab">Mon Lab</a>
</div>

<div class="cyber-grid">
  <div class="cyber-card">
    <h3>📖 À propos</h3>
    <p>Mon parcours, mes passions et ma motivation dans la cybersécurité.</p>
  </div>
  <div class="cyber-card">
    <h3>🎓 FSSM</h3>
    <p>Formation académique, projets et compétences acquises.</p>
  </div>
  <div class="cyber-card">
    <h3>🔐 TryHackMe</h3>
    <p>Paths complétés, badges et write-ups de challenges.</p>
  </div>
  <div class="cyber-card">
    <h3>🖥️ Mon Lab</h3>
    <p>Environnement de test, machines virtuelles et expériences.</p>
  </div>
</div>

<p style="text-align: center; font-size: 1.1em; margin: 30px 0;">
  Salut — je suis <strong>Haname</strong>, étudiante passionnée par la sécurité informatique.<br>
  Bienvenue sur mon blog où je partage mon apprentissage et mes découvertes.
</p>

<div class="cyber-badges">
  <span class="cyber-badge">🔐 TryHackMe</span>
  <span class="cyber-badge">💻 GitHub</span>
  <span class="cyber-badge">🐦 Twitter</span>
  <span class="cyber-badge">🔗 LinkedIn</span>
</div>

<div class="cyber-footer">
  © 2025 Haname — Cybersecurity Student — FSSM
</div>

</div>
