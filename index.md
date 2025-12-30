---
layout: default
title: Accueil
nav: home
---

<style>
@keyframes matrixRain {
  0% { transform: translateY(-100vh); }
  100% { transform: translateY(100vh); }
}

@keyframes floatUpDown {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
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

@keyframes cyberiaGlitch {
  0% { text-shadow: 2px 2px 0px #ff00ff, -2px -2px 0px #00ffff; }
  25% { text-shadow: -2px 2px 0px #ff00ff, 2px -2px 0px #00ffff; }
  50% { text-shadow: 2px -2px 0px #00ffff, -2px 2px 0px #ff00ff; }
  75% { text-shadow: -2px -2px 0px #00ffff, 2px 2px 0px #ff00ff; }
  100% { text-shadow: 2px 2px 0px #ff00ff, -2px -2px 0px #00ffff; }
}

@keyframes terminalFlicker {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
  51% { opacity: 0.9; }
}

body {
  background: #0a0a0f;
  min-height: 100vh;
  margin: 0;
  position: relative;
  overflow-x: hidden;
  font-family: 'Courier New', 'Consolas', monospace;
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
  animation: matrixRain linear infinite;
}

.binary-digit.float {
  animation: floatUpDown 3s ease-in-out infinite;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
  position: relative;
  z-index: 1;
}

.cyberia-header {
  text-align: center;
  margin-bottom: 40px;
  padding: 30px;
  background: rgba(0, 0, 0, 0.7);
  border: 2px solid #ff00ff;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  animation: terminalFlicker 3s infinite;
}

.cyberia-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: repeating-linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.15) 0px,
    rgba(0, 0, 0, 0.15) 1px,
    transparent 1px,
    transparent 2px
  );
  pointer-events: none;
}

.cyberia-title {
  font-size: 4.5em;
  color: #00ffff;
  text-shadow: 0 0 10px #00ffff;
  margin: 0;
  font-weight: 900;
  letter-spacing: 8px;
  text-transform: uppercase;
  animation: cyberiaGlitch 0.5s infinite;
  position: relative;
}

.cyberia-subtitle {
  font-size: 1.8em;
  color: #ff00ff;
  margin: 10px 0 0 0;
  text-shadow: 0 0 5px #ff00ff;
  letter-spacing: 3px;
  position: relative;
}

.cyberia-subtitle::after {
  content: '_';
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

.cyber-header {
  text-align: center;
  margin-bottom: 60px;
}

.neon-title {
  font-size: 3em;
  text-align: center;
  color: transparent;
  background: linear-gradient(90deg, #ff00ff, #00ffff, #ff6b9d);
  background-size: 200% auto;
  -webkit-background-clip: text;
  background-clip: text;
  animation: gradientBG 3s ease infinite;
  margin: 40px 0 10px 0;
  font-weight: 900;
  letter-spacing: 2px;
}

.subtitle {
  font-size: 1.5em;
  color: #8b949e;
  text-align: center;
  margin-bottom: 40px;
  font-style: italic;
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
  text-shadow: -1px 0 #ff00ff;
  animation: glitch-1 2s infinite linear alternate-reverse;
}

.glitch-text:after {
  left: -2px;
  text-shadow: -1px 0 #00ffff;
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
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin: 60px 0;
}

.holo-card {
  background: rgba(0, 0, 0, 0.85);
  border: 1px solid rgba(0, 255, 255, 0.3);
  border-radius: 5px;
  padding: 25px;
  text-align: center;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: relative;
  overflow: hidden;
  text-decoration: none;
  color: inherit;
  display: block;
  font-family: 'Courier New', monospace;
}

.holo-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.1), transparent);
  transition: left 0.5s;
}

.holo-card:hover::before {
  left: 100%;
}

.holo-card:hover {
  transform: translateY(-5px);
  border-color: #ff00ff;
  box-shadow: 0 0 20px rgba(255, 0, 255, 0.3);
}

.holo-card h3 {
  color: #00ffff;
  margin: 0 0 15px 0;
  font-size: 1.4em;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.holo-card p {
  color: #c9d1d9;
  margin: 0;
  line-height: 1.6;
  font-size: 0.95em;
}

.welcome-text {
  text-align: center;
  font-size: 1.2em;
  color: #8b949e;
  margin: 50px 0;
  padding: 30px;
  background: rgba(0, 0, 0, 0.7);
  border-radius: 5px;
  border-left: 4px solid #ff00ff;
  animation: slideIn 1s ease-out;
  font-family: 'Courier New', monospace;
}

.mission-statement {
  text-align: center;
  font-size: 1.1em;
  color: #00ffff;
  margin: 40px 0;
  padding: 20px;
  background: rgba(0, 0, 0, 0.5);
  border-radius: 5px;
  border: 1px solid rgba(0, 255, 255, 0.2);
  font-family: 'Courier New', monospace;
}

.mission-statement strong {
  color: #ff00ff;
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
  background: rgba(0, 0, 0, 0.8);
  border: 1px solid #00ffff;
  border-radius: 0;
  color: #00ffff;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s;
  animation: pulse 2s infinite;
  font-family: 'Courier New', monospace;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.floating-badge:hover {
  background: #ff00ff;
  color: black;
  transform: translateY(-3px);
  box-shadow: 0 0 20px rgba(255, 0, 255, 0.5);
  animation: none;
  border-color: #ff00ff;
}

.cyber-footer {
  text-align: center;
  margin-top: 80px;
  padding-top: 30px;
  border-top: 1px solid rgba(255, 0, 255, 0.3);
  color: #8b949e;
  font-size: 0.9em;
  font-family: 'Courier New', monospace;
}

.terminal-line {
  color: #00ff00;
  font-family: 'Courier New', monospace;
  margin: 10px 0;
  padding-left: 20px;
  position: relative;
}

.terminal-line::before {
  content: '>';
  position: absolute;
  left: 0;
  color: #ff00ff;
}

@media (max-width: 1024px) {
  .hologram-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .cyberia-title {
    font-size: 2.8em;
    letter-spacing: 4px;
  }
  
  .cyberia-subtitle {
    font-size: 1.2em;
  }
  
  .neon-title {
    font-size: 2em;
  }
  
  .subtitle {
    font-size: 1.2em;
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
// Create binary rain background with moving 0 and 1
document.addEventListener('DOMContentLoaded', function() {
  const binaryContainer = document.createElement('div');
  binaryContainer.className = 'binary-background';
  document.body.appendChild(binaryContainer);
  
  // Create falling binary digits (matrix rain style)
  for (let i = 0; i < 120; i++) {
    const digit = document.createElement('div');
    digit.className = 'binary-digit';
    digit.textContent = Math.random() > 0.5 ? '1' : '0';
    
    // Random position
    digit.style.left = Math.random() * 100 + 'vw';
    
    // Random size
    const size = Math.random() * 18 + 12;
    digit.style.fontSize = size + 'px';
    
    // Random animation speed
    const duration = Math.random() * 10 + 5;
    const delay = Math.random() * 5;
    digit.style.animationDuration = duration + 's';
    digit.style.animationDelay = delay + 's';
    
    // Random opacity
    digit.style.opacity = Math.random() * 0.2 + 0.05;
    
    // Cyberia colors (magenta and cyan)
    const colors = [
      'rgba(255, 0, 255, 0.15)',
      'rgba(0, 255, 255, 0.15)',
      'rgba(255, 107, 157, 0.15)',
      'rgba(0, 255, 0, 0.15)'
    ];
    digit.style.color = colors[Math.floor(Math.random() * colors.length)];
    
    binaryContainer.appendChild(digit);
  }
  
  // Create floating binary digits (up and down movement)
  for (let i = 0; i < 40; i++) {
    const floatDigit = document.createElement('div');
    floatDigit.className = 'binary-digit float';
    floatDigit.textContent = Math.random() > 0.5 ? '1' : '0';
    
    // Random position
    floatDigit.style.left = Math.random() * 100 + 'vw';
    floatDigit.style.top = Math.random() * 100 + 'vh';
    
    // Random size
    const floatSize = Math.random() * 22 + 14;
    floatDigit.style.fontSize = floatSize + 'px';
    
    // Random animation delay
    floatDigit.style.animationDelay = Math.random() * 2 + 's';
    
    // Random opacity
    floatDigit.style.opacity = Math.random() * 0.3 + 0.1;
    
    // Cyberia colors - brighter for floating ones
    const floatColors = [
      'rgba(255, 0, 255, 0.3)',
      'rgba(0, 255, 255, 0.3)',
      'rgba(255, 107, 157, 0.3)'
    ];
    floatDigit.style.color = floatColors[Math.floor(Math.random() * floatColors.length)];
    
    binaryContainer.appendChild(floatDigit);
  }
  
  // Add subtle floating animation to cards
  const cards = document.querySelectorAll('.holo-card');
  cards.forEach((card, index) => {
    card.style.animationDelay = (index * 0.1) + 's';
    card.style.animation = 'slideIn 0.8s ease-out forwards';
    card.style.opacity = '0';
  });
  
  // Add some terminal-style text effects
  const cyberiaHeader = document.querySelector('.cyberia-header');
  const terminalText = [
    "CONNECTION ESTABLISHED",
    "WELCOME TO CYBERIA NEXUS",
    "ACCESSING KNOWLEDGE DATABASE...",
    "USER: HANAME | CLEARANCE: LEVEL 7",
    "NAVIGATION SYSTEMS ONLINE"
  ];
  
  let lineIndex = 0;
  function addTerminalLine() {
    if (lineIndex < terminalText.length) {
      const line = document.createElement('div');
      line.className = 'terminal-line';
      line.textContent = terminalText[lineIndex];
      line.style.opacity = '0';
      line.style.animation = 'slideIn 0.5s forwards';
      line.style.animationDelay = (lineIndex * 0.3) + 's';
      cyberiaHeader.appendChild(line);
      lineIndex++;
      setTimeout(addTerminalLine, 300);
    }
  }
  
  setTimeout(addTerminalLine, 1000);
});
</script>

<div class="container">

  <div class="cyberia-header">
    <div class="cyberia-title">CYBERIA</div>
    <div class="cyberia-subtitle">Cafe & Club</div>
    <!-- Terminal lines will be added by JavaScript -->
  </div>

  <div class="cyber-header">
    <div class="neon-title">WELCOME TO MY CYBERSPACE</div>
    <div class="subtitle">A digital notebook for everything I learn</div>
    <div class="glitch-text" data-text="CYBERSECURITY KNOWLEDGE BASE">CYBERSECURITY KNOWLEDGE BASE</div>
  </div>

  <div class="mission-statement">
    <p>In this website, I document <strong>every concept I learn</strong>, <strong>every challenge I solve</strong>, and <strong>every skill I develop</strong> in cybersecurity.<br>
    From academic notes to hands-on labs, this is my personal knowledge repository.</p>
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
    <p>Salut — je suis <strong style="color: #ff00ff;">Haname</strong>, étudiante en cybersécurité à la FSSM.<br>
    Bienvenue sur mon site où je partage mon parcours, mes parcours (paths) TryHackMe, la formation FSSM, et mes laboratoires personnels.</p>
  </div>

  <div class="badge-container">
    <a href="{{ site.baseurl }}/tryhackme" class="floating-badge">TRYHACKME</a>
    <a href="https://github.com/ItsHaname" class="floating-badge" target="_blank">GITHUB</a>
    <a href="#" class="floating-badge">TWITTER</a>
    <a href="#" class="floating-badge">LINKEDIN</a>
  </div>

  <div class="cyber-footer">
    <div class="terminal-line">© 2025 CYBERIA NEXUS — HANAME — FSSM</div>
    <div class="terminal-line">CONNECTION: ACTIVE — PROTOCOL: SSH-2.0</div>
  </div>

</div>
