---
layout: default
title: Accueil
nav: home
---

<style>
@keyframes matrixRain {
  0% { background-position: 0% 0%; }
  100% { background-position: 0% 100%; }
}

@keyframes float {
  0%, 100% { transform: translateY(0) rotate(0deg); opacity: 0.1; }
  50% { opacity: 0.3; }
}

@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes slideIn {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.05); }
  100% { transform: scale(1); }
}

body {
  background: 
    linear-gradient(135deg, #0a0a0f 0%, #1a1a2e 100%),
    repeating-linear-gradient(0deg, 
      transparent, 
      transparent 2px, 
      rgba(0, 170, 255, 0.03) 2px, 
      rgba(0, 170, 255, 0.03) 4px);
  animation: matrixRain 20s linear infinite;
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
  color: rgba(0, 170, 255, 0.15);
  opacity: 0;
  animation: float linear infinite;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
  position: relative;
  z-index: 1;
}

.cyber-header {
  text-align: center;
  margin-bottom: 60px;
}

.neon-title {
  font-size: 4em;
  text-align: center;
  color: transparent;
  background: linear-gradient(90deg, #ff6b9d, #8a8dff, #58a6ff);
  background-size: 200% auto;
  -webkit-background-clip: text;
  background-clip: text;
  animation: gradientBG 3s ease infinite;
  margin: 20px 0 10px 0;
  font-weight: 900;
  letter-spacing: 2px;
}

.glitch-text {
  font-size: 1.8em;
  font-weight: bold;
  color: #fff;
  position: relative;
  display: inline-block;
  margin: 10px 0 40px 0;
}

.glitch-text:before,
.glitch-text:after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.glitch-text:before {
  left: 2px;
  text-shadow: -1px 0 #ff6b9d;
  animation: glitch-1 2s infinite linear alternate-reverse;
}

.glitch-text:after {
  left: -2px;
  text-shadow: -1px 0 #8a8dff;
  animation: glitch-2 3s infinite linear alternate-reverse;
}

@keyframes glitch-1 {
  0% { clip-path: inset(40% 0 61% 0); }
  100% { clip-path: inset(92% 0 1% 0); }
}

@keyframes glitch-2 {
  0% { clip-path: inset(25% 0 58% 0); }
  100% { clip-path: inset(75% 0 1% 0); }
}

.hologram-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  margin: 60px 0;
}

.holo-card {
  background: rgba(13, 17, 23, 0.85);
  border: 1px solid rgba(138, 141, 255, 0.3);
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: relative;
  overflow: hidden;
  text-decoration: none;
  color: inherit;
  display: block;
  backdrop-filter: blur(10px);
}

.holo-card:before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, #ff6b9d, #8a8dff, transparent);
  z-index: -1;
  opacity: 0;
  transition: opacity 0.4s;
}

.holo-card:hover:before {
  opacity: 0.5;
}

.holo-card:hover {
  transform: translateY(-10px) scale(1.02);
  border-color: #8a8dff;
  box-shadow: 0 15px 35px rgba(138, 141, 255, 0.2);
}

.holo-card h3 {
  color: #ff6b9d;
  margin: 0 0 15px 0;
  font-size: 1.5em;
  font-weight: 600;
}

.holo-card p {
  color: #c9d1d9;
  margin: 0;
  line-height: 1.6;
}

.welcome-text {
  text-align: center;
  font-size: 1.2em;
  color: #8b949e;
  margin: 50px 0;
  padding: 30px;
  background: rgba(13, 17, 23, 0.7);
  border-radius: 15px;
  border-left: 4px solid #ea4aaa;
  animation: slideIn 1s ease-out;
}

.badge-container {
  display: flex;
  gap: 20px;
  justify-content: center;
  margin: 40px 0;
  flex-wrap: wrap;
}

.floating-badge {
  display: inline-block;
  padding: 12px 25px;
  background: rgba(22, 27, 34, 0.8);
  border: 1px solid #30363d;
  border-radius: 25px;
  color: #58a6ff;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s;
  animation: pulse 2s infinite;
  backdrop-filter: blur(5px);
}

.floating-badge:hover {
  background: #58a6ff;
  color: white;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(88, 166, 255, 0.3);
  animation: none;
}

.cyber-footer {
  text-align: center;
  margin-top: 80px;
  padding-top: 30px;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  color: #586069;
  font-size: 0.9em;
}

.scan-line {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, 
    transparent, 
    rgba(138, 141, 255, 0.8), 
    transparent);
  animation: scan 4s linear infinite;
  z-index: 1000;
  pointer-events: none;
}

@keyframes scan {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100vh); }
}

@media (max-width: 768px) {
  .neon-title {
    font-size: 2.5em;
  }
  
  .glitch-text {
    font-size: 1.4em;
  }
  
  .hologram-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
  
  .badge-container {
    gap: 10px;
  }
  
  .floating-badge {
    padding: 10px 20px;
    font-size: 0.9em;
  }
}
</style>

<script>
// Create binary rain background
document.addEventListener('DOMContentLoaded', function() {
  const binaryContainer = document.createElement('div');
  binaryContainer.className = 'binary-background';
  document.body.appendChild(binaryContainer);
  
  // Create more binary digits for full background
  for (let i = 0; i < 150; i++) {
    const digit = document.createElement('div');
    digit.className = 'binary-digit';
    digit.textContent = Math.random() > 0.5 ? '1' : '0';
    
    // Random position
    digit.style.left = Math.random() * 100 + 'vw';
    digit.style.top = Math.random() * 100 + 'vh';
    
    // Random size
    const size = Math.random() * 20 + 10;
    digit.style.fontSize = size + 'px';
    
    // Random animation
    const duration = Math.random() * 20 + 10;
    const delay = Math.random() * 10;
    digit.style.animation = `float ${duration}s linear infinite`;
    digit.style.animationDelay = delay + 's';
    
    // Random opacity
    digit.style.opacity = Math.random() * 0.2 + 0.05;
    
    // Random color variation
    const colors = [
      'rgba(0, 170, 255, 0.15)',
      'rgba(138, 141, 255, 0.15)',
      'rgba(255, 107, 157, 0.15)',
      'rgba(88, 166, 255, 0.15)'
    ];
    digit.style.color = colors[Math.floor(Math.random() * colors.length)];
    
    binaryContainer.appendChild(digit);
  }
  
  // Create scan line
  const scanLine = document.createElement('div');
  scanLine.className = 'scan-line';
  document.body.appendChild(scanLine);
  
  // Add subtle floating animation to cards
  const cards = document.querySelectorAll('.holo-card');
  cards.forEach((card, index) => {
    card.style.animationDelay = (index * 0.1) + 's';
    card.style.animation = 'slideIn 0.8s ease-out forwards';
    card.style.opacity = '0';
  });
});
</script>

<div class="scan-line"></div>

<div class="container">

  <div class="cyber-header">
    <div class="neon-title">HANAME</div>
    <div class="glitch-text" data-text="CYBERSECURITY STUDENT">CYBERSECURITY STUDENT</div>
  </div>

  <div class="hologram-grid">
    <a href="{{ site.baseurl }}/about" class="holo-card">
      <h3>À PROPOS</h3>
      <p>Mon parcours, passions et motivation dans la cybersécurité</p>
    </a>
    
    <a href="{{ site.baseurl }}/fssm" class="holo-card">
      <h3>FSSM</h3>
      <p>Formation académique, projets et compétences acquises</p>
    </a>
    
    <a href="{{ site.baseurl }}/tryhackme" class="holo-card">
      <h3>TRYHACKME</h3>
      <p>Paths complétés, badges et write-ups de challenges</p>
    </a>
    
    <a href="{{ site.baseurl }}/my-lab" class="holo-card">
      <h3>MON LAB</h3>
      <p>Environnement de test, machines virtuelles et expériences</p>
    </a>
  </div>

  <div class="welcome-text">
    <p>Salut — je suis <strong style="color: #ff6b9d;">Haname</strong>, étudiante en cybersécurité à la FSSM.<br>
    Bienvenue sur mon site où je partage mon parcours, mes parcours (paths) TryHackMe, la formation FSSM, et mes laboratoires personnels.</p>
  </div>

  <div class="badge-container">
    <a href="{{ site.baseurl }}/tryhackme" class="floating-badge">TRYHACKME</a>
    <a href="https://github.com/ItsHaname" class="floating-badge" target="_blank">GITHUB</a>
    <a href="#" class="floating-badge">TWITTER</a>
    <a href="#" class="floating-badge">LINKEDIN</a>
  </div>

  <div class="cyber-footer">
    © 2025 HANAME — CYBERSECURITY STUDENT — FSSM
  </div>

</div>
