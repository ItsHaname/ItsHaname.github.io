<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Lab - Home Lab Setup</title>
  <style>
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
      0%, 100% { transform: scale(1); box-shadow: 0 0 20px rgba(59, 130, 246, 0.3); }
      50% { transform: scale(1.05); box-shadow: 0 0 40px rgba(59, 130, 246, 0.6); }
    }

  @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

   @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
    }
    @keyframes glow {
      0%, 100% { text-shadow: 0 0 10px #60a5fa, 0 0 20px #60a5fa; }
      50% { text-shadow: 0 0 20px #60a5fa, 0 0 40px #60a5fa, 0 0 60px #3b82f6; }
    }

   * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

  body {
      background: #0a0e1a;
      color: #e2e8f0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      min-height: 100vh;
      padding: 20px;
    }

  .container {
      max-width: 1400px;
      margin: 0 auto;
      position: relative;
    }

   /* Particles background */
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
      opacity: 0.4;
    }

   .particle {
      position: absolute;
      width: 3px;
      height: 3px;
      background: #3b82f6;
      border-radius: 50%;
      animation: float 4s infinite ease-in-out;
    }

   /* Hero Section */
    .lab-hero {
      text-align: center;
      margin-bottom: 60px;
      padding: 60px 20px;
      background: linear-gradient(135deg, rgba(0, 20, 40, 0.9), rgba(15, 23, 42, 0.8));
      border-radius: 30px;
      border: 3px solid transparent;
      background-clip: padding-box;
      position: relative;
      overflow: hidden;
    }

   .lab-hero::before {
      content: '';
      position: absolute;
      top: -3px;
      left: -3px;
      right: -3px;
      bottom: -3px;
      background: linear-gradient(45deg, #3b82f6, #60a5fa, #2563eb, #1e40af);
      background-size: 300% 300%;
      animation: gradientBG 4s ease infinite;
      border-radius: 30px;
      z-index: -1;
    }

  .lab-badge {
      display: inline-block;
      padding: 12px 35px;
      background: linear-gradient(135deg, #3b82f6, #2563eb);
      color: white;
      font-size: 1.2em;
      font-weight: 700;
      border-radius: 50px;
      margin-bottom: 25px;
      box-shadow: 0 10px 30px rgba(59, 130, 246, 0.5);
      letter-spacing: 2px;
    }

  .lab-title {
      font-size: 4em;
      color: transparent;
      background: linear-gradient(90deg, #3b82f6, #60a5fa, #2563eb, #60a5fa, #3b82f6);
      background-size: 300% auto;
      -webkit-background-clip: text;
      background-clip: text;
      animation: gradientBG 3s ease infinite, glow 2s ease-in-out infinite;
      margin: 20px 0;
      font-weight: 900;
      letter-spacing: 3px;
      text-transform: uppercase;
    }

   .lab-subtitle {
      font-size: 1.8em;
      color: #60a5fa;
      margin: 20px 0;
      font-style: italic;
      letter-spacing: 2px;
    }

   .lab-subtitle::after {
      content: '_';
      animation: blink 1s infinite;
      color: #3b82f6;
    }

   /* Terminal Section */
    .terminal-section {
      background: rgba(10, 14, 26, 0.95);
      border: 2px solid #22c55e;
      border-radius: 15px;
      padding: 25px;
      margin: 40px 0;
      font-family: 'Courier New', monospace;
      box-shadow: 0 0 30px rgba(34, 197, 94, 0.3);
    }

  .terminal-header {
      display: flex;
      gap: 8px;
      margin-bottom: 20px;
    }

   .terminal-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
    }

   .terminal-dot.red { background: #ff5f56; }
    .terminal-dot.yellow { background: #ffbd2e; }
    .terminal-dot.green { background: #27c93f; }

  .terminal-text {
      color: #10b981;
      line-height: 2;
    }

   .terminal-text .prompt {
      color: #22c55e;
      font-weight: bold;
    }

   .terminal-text .command {
      color: #10b981;
    }

   /* Lab Infrastructure Grid */
    .infrastructure-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
      margin: 60px 0;
      perspective: 1000px;
    }

  .infra-card {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(30, 41, 59, 0.8));
      border: 2px solid transparent;
      border-radius: 20px;
      padding: 35px;
      transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
      text-decoration: none;
      color: inherit;
      display: block;
      animation: slideIn 0.8s ease-out backwards;
      transform-style: preserve-3d;
      overflow: hidden;
    }

  .infra-card::before {
      content: '';
      position: absolute;
      top: -2px;
      left: -2px;
      right: -2px;
      bottom: -2px;
      background: linear-gradient(45deg, #3b82f6, #60a5fa, #2563eb, #1e40af);
      background-size: 300% 300%;
      animation: gradientBG 6s ease infinite;
      border-radius: 20px;
      z-index: -1;
      opacity: 0;
      transition: opacity 0.5s;
    }

  .infra-card:hover::before {
      opacity: 1;
    }

   .infra-card::after {
      content: '';
      position: absolute;
      top: 50%;
      left: 50%;
      width: 0;
      height: 0;
      border-radius: 50%;
      background: rgba(59, 130, 246, 0.3);
      transform: translate(-50%, -50%);
      transition: width 0.6s, height 0.6s;
    }

  .infra-card:hover::after {
      width: 500px;
      height: 500px;
    }

  .infra-card:hover {
      transform: translateY(-15px) rotateX(5deg) rotateY(5deg);
      box-shadow: 0 25px 60px rgba(59, 130, 246, 0.6);
    }

   .infra-card:nth-child(1) { animation-delay: 0.1s; }
    .infra-card:nth-child(2) { animation-delay: 0.2s; }
    .infra-card:nth-child(3) { animation-delay: 0.3s; }
    .infra-card:nth-child(4) { animation-delay: 0.4s; }

  .infra-icon {
      font-size: 3.5em;
      margin-bottom: 20px;
      display: inline-block;
      filter: drop-shadow(0 0 15px currentColor);
    }

  .infra-card h3 {
      color: #60a5fa;
      margin: 20px 0;
      font-size: 2em;
      font-weight: 700;
      position: relative;
      z-index: 1;
      text-shadow: 0 0 10px rgba(96, 165, 250, 0.5);
    }

  .infra-description {
      color: #94a3b8;
      font-size: 1em;
      line-height: 1.7;
      margin: 15px 0;
      position: relative;
      z-index: 1;
    }

   .infra-specs {
      margin-top: 20px;
      padding-top: 20px;
      border-top: 1px solid rgba(34, 197, 94, 0.2);
      position: relative;
      z-index: 1;
    }

  .spec-item {
      display: flex;
      align-items: center;
      gap: 10px;
      color: #cbd5e1;
      font-size: 0.9em;
      margin: 8px 0;
    }

  .spec-icon {
      color: #3b82f6;
      font-weight: bold;
    }

  .section-title {
      color: #60a5fa;
      text-align: center;
      margin: 60px 0 40px 0;
      font-size: 2.5em;
      text-shadow: 0 0 20px rgba(96, 165, 250, 0.5);
    }
    /* Lab Topology */
    .topology-section {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(30, 41, 59, 0.8));
      border: 2px solid #3b82f6;
      border-radius: 20px;
      padding: 40px;
      margin: 50px 0;
    }

   .topology-section h2 {
      color: #60a5fa;
      margin-bottom: 30px;
      font-size: 2em;
    }

  .topology-tree {
      font-family: 'Courier New', monospace;
      color: #60a5fa;
      font-size: 1.1em;
      line-height: 1.8;
      white-space: pre;
    }

   
.topology-tree .folder {
      color: #3b82f6;
      font-weight: bold;
    }

  .topology-tree .file {
      color: #94a3b8;
    }

    /* Coming Soon */
  .coming-soon {
      text-align: center;
      padding: 60px 20px;
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.3), rgba(30, 41, 59, 0.2));
      border-radius: 20px;
      border: 2px dashed #3b82f6;
      margin: 50px 0;
    }

   .coming-soon h2 {
      color: #60a5fa;
      font-size: 2.5em;
      margin-bottom: 20px;
      animation: glow 2s ease-in-out infinite;
    }

  .coming-soon p {
      color: #94a3b8;
      font-size: 1.2em;
    }

  @media (max-width: 768px) {
      .lab-title {
        font-size: 2.5em;
      }
      
  .lab-subtitle {
        font-size: 1.3em;
      }
      
  .infrastructure-grid {
        grid-template-columns: 1fr;
      }
      
   .infra-card:hover {
        transform: translateY(-10px);
      }
    }
  </style>
</head>
<body>
  <div class="particles" id="particles"></div>
  
  <div class="container">
    <!-- Hero Section -->
    <div class="lab-hero">
      <div class="lab-badge">MY OWN LAB</div>
      <div class="lab-title">Home Lab Setup</div>
      <div class="lab-subtitle">Raspberry Pi • Docker • Arch Linux</div>
    </div>

    <!-- Terminal Info -->
   <div class="terminal-section">
      <div class="terminal-header">
        <div class="terminal-dot red"></div>
        <div class="terminal-dot yellow"></div>
        <div class="terminal-dot green"></div>
      </div>
      <div class="terminal-text">
        <span class="prompt">haname@homelab:~$</span> <span class="command">cat lab_overview.txt</span><br>
        → Infrastructure: Raspberry Pi 4 + Docker Containers + Arch Linux VMs<br>
        → Objectif: Reconnaissance, Exploitation, Post-Exploitation, Persistence<br>
        → Réseau: 10.10.10.0/24 (Lab Network)<br>
        → Status: Building...<span style="animation: blink 1s infinite;">_</span>
      </div>
    </div>

    <!-- Infrastructure Grid -->
   <h2 class="section-title">🖥️ Infrastructure</h2>

   <div class="infrastructure-grid">
         <div class="infra-card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Raspberry_Pi_official_logo.svg" alt="Raspberry Pi" style="width: 120px; height: 120px; object-fit: contain; margin-bottom: 20px;">
        <h3>Raspberry Pi</h3>
      </div>

  <div class="infra-card">
        <img src="https://www.docker.com/wp-content/uploads/2022/03/vertical-logo-monochromatic.png" alt="Docker" style="width: 120px; height: 120px; object-fit: contain; margin-bottom: 20px; filter: brightness(0) saturate(100%) invert(50%) sepia(98%) saturate(2476%) hue-rotate(180deg) brightness(98%) contrast(101%);">
        <h3>Docker Containers</h3>
      </div>

<div class="infra-card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Archlinux-icon-crystal-64.svg" alt="Arch Linux" style="width: 120px; height: 120px; object-fit: contain; margin-bottom: 20px;">
        <h3>Arch Linux</h3>
      </div>

   <div class="infra-card">
        <div class="infra-icon">🔬</div>
        <h3>Other Labs</h3>
      </div>

   </div>

    <!-- Coming Soon -->
   <div class="coming-soon">
      <h2>🚀 Lab en Construction</h2>
      <p>Les machines, challenges et write-ups seront ajoutés progressivement.</p>
      <p style="margin-top: 15px; color: #60a5fa;">Documentation technique et notes pratiques à venir...</p>
    </div>

  <!-- Footer -->
  <div style="text-align: center; margin-top: 80px; padding: 40px; background: linear-gradient(135deg, rgba(15, 23, 42, 0.8), rgba(10, 14, 26, 0.9)); border-radius: 20px; border: 2px solid #1e4d7b;">
      <p style="color: #94a3b8; font-size: 1.1em; line-height: 1.8;">
        🏠 Home Lab: <span style="color: #60a5fa; font-weight: bold;">Raspberry Pi + Docker + Arch Linux</span><br>
        🎯 Objectif: <span style="color: #3b82f6; font-weight: bold;">Hands-on Cybersecurity Practice</span><br>
        📡 Réseau: <span style="color: #60a5fa; font-weight: bold;">10.10.10.0/24</span>
      </p>
    </div>

  </div>

  <script>
    // Create animated particles
    document.addEventListener('DOMContentLoaded', function() {
      const particlesDiv = document.getElementById('particles');
      
      for (let i = 0; i < 30; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + '%';
        particle.style.top = Math.random() * 100 + '%';
        particle.style.animationDelay = Math.random() * 4 + 's';
        particle.style.animationDuration = (Math.random() * 3 + 3) + 's';
        particlesDiv.appendChild(particle);
      }
    });
  </script>
</body>
</html>
