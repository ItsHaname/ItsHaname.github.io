---
layout: default
title: Accueil
nav: home
---

<link rel="icon" href="https://raw.githubusercontent.com/ItsHaname/ItsHaname.github.io/main/logo" type="image/png">

<style>
/* --- TES ANIMATIONS EXISTANTES --- */
@keyframes matrixRain { 0% { transform: translateY(-100vh); } 100% { transform: translateY(100vh); } }
@keyframes floatUpDown { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }
@keyframes gradientBG { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
@keyframes slideIn { from { opacity: 0; transform: translateY(-20px); } to { opacity: 1; transform: translateY(0); } }
@keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.05); } 100% { transform: scale(1); } }
@keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
@keyframes glitch-1 { 0% { clip-path: inset(40% 0 61% 0); } 100% { clip-path: inset(92% 0 1% 0); } }
@keyframes glitch-2 { 0% { clip-path: inset(25% 0 58% 0); } 100% { clip-path: inset(75% 0 1% 0); } }

/* --- STYLE DE LA PAGE --- */
body {
  background: #0a0e1a;
  min-height: 100vh;
  margin: 0;
  position: relative;
  overflow-x: hidden;
}

.binary-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: -1;
}

.binary-digit {
  position: absolute;
  font-family: 'Courier New', monospace;
  font-size: 16px;
  color: rgba(59, 130, 246, 0.15);
  opacity: 0;
  animation: matrixRain linear infinite;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
  position: relative;
  z-index: 1;
}

/* --- STYLE DES IMAGES (OPTIMISÉ) --- */
.image-section {
  width: 85%; /* Taille parfaite pour tes yeux */
  max-width: 1400px;
  margin: 60px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.cyber-img {
  display: block;
  width: 100%;
  height: auto;
  margin-bottom: 50px;
  border-radius: 15px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
  transition: all 0.4s ease-in-out;
  border: 1px solid rgba(59, 130, 246, 0.2);
}

.cyber-img:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 50px rgba(0, 217, 255, 0.3);
  filter: brightness(1.1);
}

/* --- AUTRES STYLES --- */
.cyberia-header {
  text-align: center;
  margin-bottom: 60px;
  padding: 40px 20px;
  background: rgba(0, 20, 40, 0.6);
  border-radius: 30px;
  border: 3px solid #1e4d7b;
  box-shadow: 0 0 40px rgba(30, 77, 123, 0.5);
}

.cyberia-title { font-size: 5em; color: #ff6b4a; text-shadow: 0 0 10px #ff6b4a; font-weight: 900; letter-spacing: 10px; text-transform: uppercase; font-style: italic; }
.cyberia-line { width: 100%; height: 3px; background: linear-gradient(90deg, transparent, #1e4d7b, #3b82f6, #1e4d7b, transparent); margin: 20px auto; max-width: 500px; }
.cyberia-subtitle { font-size: 1.8em; color: #60a5fa; letter-spacing: 4px; font-style: italic; }

.hologram-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; margin: 60px 0; }
.holo-card { background: rgba(15, 23, 42, 0.85); border: 1px solid rgba(59, 130, 246, 0.3); border-radius: 15px; padding: 30px; text-align: center; text-decoration: none; color: inherit; transition: 0.4s; }
.holo-card:hover { transform: translateY(-10px); border-color: #60a5fa; box-shadow: 0 15px 35px rgba(59, 130, 246, 0.3); }

.floating-badge { display: inline-block; padding: 12px 25px; background: rgba(15, 23, 42, 0.8); border: 1px solid #1e40af; border-radius: 25px; color: #60a5fa; text-decoration: none; animation: pulse 2s infinite; margin: 5px; }

@media (max-width: 768px) {
  .hologram-grid { grid-template-columns: 1fr; }
  .cyberia-title { font-size: 3em; }
  .image-section { width: 95%; }
}
</style>

<div class="container">
  <div class="cyberia-header">
    <div class="cyberia-title">CYBERIA</div>
    <div class="cyberia-line"></div>
    <div class="cyberia-subtitle">Cafe & Club</div>
  </div>

  <div class="hologram-grid">
    <a href="/about/me" class="holo-card"><h3>À PROPOS</h3><p>Mon parcours et mes passions</p></a>
    <a href="/fssm/" class="holo-card"><h3>FSSM</h3><p>Formation académique</p></a>
    <a href="/tryhackme/" class="holo-card"><h3>TRYHACKME</h3><p>Badges et write-ups</p></a>
    <a href="/my-lab/" class="holo-card"><h3>MON LAB</h3><p>Environnement de test</p></a>
  </div>

  <div class="image-section">
    <img class="cyber-img" src="https://github.com/user-attachments/assets/5b6bcc1a-6f76-46fd-88fb-34b43fbaa0e5" />
    <img class="cyber-img" src="https://github.com/user-attachments/assets/8d54004b-3bcb-4f57-b5a0-310241f73b75" />
    <img class="cyber-img" src="https://github.com/user-attachments/assets/972ed0ac-d641-4f54-bd52-c4f9b4380774" />
    <img class="cyber-img" src="https://github.com/user-attachments/assets/39848e20-ce8b-49cb-ab3a-5679691abe8c" />
  </div>

  <div style="text-align: center; margin: 30px 0;">
    <div style="display: inline-block; background: rgba(15, 23, 42, 0.7); border: 1px solid #3b82f6; border-radius: 10px; padding: 15px 30px;">
      <div style="color: #94a3b8; font-size: 0.9em; letter-spacing: 2px;">👁️ VISITEURS</div>
      <div style="color: #60a5fa; font-size: 2em; font-weight: 700;" id="visitorCount">0</div>
    </div>
  </div>

  <div class="badge-container" style="text-align:center;">
    <a href="/tryhackme/" class="floating-badge">TRYHACKME</a>
    <a href="https://github.com/ItsHaname" class="floating-badge" target="_blank">GITHUB</a>
  </div>
</div>

<script>
// Script pour la pluie binaire et le compteur
document.addEventListener('DOMContentLoaded', function() {
  const binaryContainer = document.createElement('div');
  binaryContainer.className = 'binary-background';
  document.body.appendChild(binaryContainer);
  for (let i = 0; i < 50; i++) {
    const digit = document.createElement('div');
    digit.className = 'binary-digit';
    digit.textContent = Math.random() > 0.5 ? '1' : '0';
    digit.style.left = Math.random() * 100 + 'vw';
    digit.style.animationDuration = (Math.random() * 10 + 5) + 's';
    digit.style.opacity = Math.random() * 0.2;
    binaryContainer.appendChild(digit);
  }
  let visits = parseInt(localStorage.getItem('cyberiaVisits') || '0') + 1;
  localStorage.setItem('cyberiaVisits', visits);
  document.getElementById('visitorCount').textContent = visits;
});
</script>
