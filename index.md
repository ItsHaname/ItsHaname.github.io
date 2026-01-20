---
layout: default
title: Accueil
nav: home
---
<link rel="icon" href="https://raw.githubusercontent.com/ItsHaname/ItsHaname.github.io/main/logo" type="image/png">
<style>
/* Gardez TOUS vos styles CSS existants... */

/* AJOUTEZ CE STYLE POUR LE LOGO SVG */
.cyberia-logo {
  display: inline-block;
  max-width: 600px;
  width: 100%;
  margin: 0 auto;
  transition: all 0.3s ease;
  cursor: pointer;
}

.cyberia-logo:hover {
  filter: drop-shadow(0 0 15px rgba(0, 255, 255, 0.7));
  transform: scale(1.02);
}

/* MODIFIEZ le conteneur header pour qu'il contienne bien le SVG */
.cyberia-header {
  text-align: center;
  margin-bottom: 60px;
  padding: 30px 20px;
  position: relative;
  background: rgba(0, 20, 40, 0.6);
  border-radius: 30px;
  border: 3px solid #1e4d7b;
  box-shadow: 0 0 40px rgba(30, 77, 123, 0.5), inset 0 0 30px rgba(30, 77, 123, 0.2);
  overflow: hidden;
}

/* Ajoutez un effet de scan line sur le header */
.cyberia-header::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, rgba(59, 130, 246, 0.6), transparent);
  animation: scanLine 3s linear infinite;
}

@keyframes scanLine {
  0% { top: 0; }
  100% { top: 100%; }
}

/* Rendez le texte existant invisible puisqu'on utilise maintenant le SVG */
.cyberia-title,
.cyberia-subtitle,
.cyberia-line {
  display: none;
}

/* ... gardez tout le reste de votre CSS existant ... */
</style>

<script>
// Gardez TOUT votre JavaScript existant...

// Ajoutez cet effet interactif pour le logo
document.addEventListener('DOMContentLoaded', function() {
  const logo = document.querySelector('.cyberia-logo');
  if (logo) {
    logo.addEventListener('click', function() {
      // Effet de flash au clic
      this.style.filter = 'drop-shadow(0 0 25px #ff00ff) brightness(1.3)';
      setTimeout(() => {
        this.style.filter = '';
      }, 500);
      
      // Message dans la console (optionnel)
      console.log('⚡ CYBERIA Cafe & Club - Access granted ⚡');
    });
    
    // Effet de pulsation subtile
    setInterval(() => {
      logo.style.transform = 'scale(1.01)';
      setTimeout(() => {
        logo.style.transform = 'scale(1)';
      }, 1000);
    }, 5000);
  }
});
</script>

<div class="container">
  <!-- REMPLACEZ VOTRE ANCIEN HEADER PAR CE LOGO SVG -->
  <div class="cyberia-header">
    <div class="cyberia-logo">
      <svg viewBox="0 0 500 150" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <!-- Dégradé cyber bleu marine -->
          <linearGradient id="cyberGradient" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" stop-color="#3b82f6"/>
            <stop offset="50%" stop-color="#60a5fa"/>
            <stop offset="100%" stop-color="#2563eb"/>
          </linearGradient>
          
          <!-- Dégradé pour le sous-titre -->
   <linearGradient id="subGradient" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" stop-color="#94a3b8"/>
            <stop offset="100%" stop-color="#cbd5e1"/>
          </linearGradient>
          
          <!-- Filtre glow -->
   <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
            <feGaussianBlur stdDeviation="3" result="blur"/>
            <feMerge>
              <feMergeNode in="blur"/>
              <feMergeNode in="SourceGraphic"/>
            </feMerge>
          </filter>
        </defs>
        
        <!-- Fond décoratif (lignes de circuit) -->
<path d="M50,40 L450,40" stroke="rgba(59,130,246,0.2)" stroke-width="1" stroke-dasharray="5,3"/>
        <path d="M50,110 L450,110" stroke="rgba(59,130,246,0.2)" stroke-width="1" stroke-dasharray="5,3"/>
        
        <!-- Texte CYBERIA (style cyberpunk) -->
  <text x="250" y="70" text-anchor="middle" font-family="'Orbitron', 'Arial Black', sans-serif" 
              font-size="55" font-weight="900" fill="url(#cyberGradient)" filter="url(#glow)"
              letter-spacing="4" style="text-transform: uppercase;">
          CYBERIA
          <!-- Animation de couleur subtile -->
          <animate attributeName="fill" values="url(#cyberGradient);#ff6b4a;url(#cyberGradient)" 
                   dur="8s" repeatCount="indefinite"/>
        </text>
        
        <!-- Ligne de séparation avec effet néon -->
  <line x1="150" y1="85" x2="350" y2="85" stroke="#60a5fa" stroke-width="2" 
              stroke-dasharray="8,4" opacity="0.8">
          <animate attributeName="stroke-dashoffset" from="0" to="20" dur="2s" repeatCount="indefinite"/>
        </line>
        
        <!-- Sous-titre Cafe & Club -->
  <text x="250" y="115" text-anchor="middle" font-family="'Rajdhani', 'Courier New', monospace" 
              font-size="28" font-weight="500" fill="url(#subGradient)" letter-spacing="6">
          Cafe & Club
          <!-- Animation de brillance -->
          <animate attributeName="opacity" values="0.8;1;0.8" dur="3s" repeatCount="indefinite"/>
        </text>
        
        <!-- Points de connexion cyber (effets décoratifs) -->
 <circle cx="140" cy="70" r="3" fill="#3b82f6">
          <animate attributeName="r" values="3;5;3" dur="2s" repeatCount="indefinite"/>
        </circle>
        <circle cx="360" cy="70" r="3" fill="#3b82f6">
          <animate attributeName="r" values="5;3;5" dur="2s" repeatCount="indefinite" begin="1s"/>
        </circle>
        
        <!-- Signal d'onde (effet radar) -->
  <circle cx="250" cy="85" r="10" stroke="#60a5fa" stroke-width="1" fill="none" opacity="0">
          <animate attributeName="r" values="10;100" dur="4s" repeatCount="indefinite"/>
          <animate attributeName="opacity" values="0.5;0" dur="4s" repeatCount="indefinite"/>
        </circle>
      </svg>
    </div>
  </div>
  
  <!-- GARDEZ TOUT LE RESTE DE VOTRE CODE EXISTANT -->
  <div class="cyber-header">
    <div class="neon-title">WELCOME TO MY CYBERSPACE</div>
    <div class="subtitle">A digital notebook for everything I learn</div>
    <div class="glitch-text" data-text="CYBERSECURITY KNOWLEDGE BASE">CYBERSECURITY KNOWLEDGE BASE</div>
  </div>
  
  <!-- ... tout le reste de votre contenu Markdown ... -->
<div class="subtitle">A digital notebook for everything I learn</div>
    <div class="glitch-text" data-text="CYBERSECURITY KNOWLEDGE BASE">CYBERSECURITY KNOWLEDGE BASE</div>
  </div>
  <div class="mission-statement">
    <p>In this website, I document <strong>every concept I learn</strong>, <strong>every challenge I solve</strong>, and <strong>every skill I develop</strong> in cybersecurity.<br>
    From academic notes to hands-on labs, this is my personal knowledge repository.</p>
  </div>
  <div class="hologram-grid">
    <a href="/about/me" class="holo-card">
      <h3>À PROPOS</h3>
      <p>Mon parcours, passions et motivation dans la cybersécurité</p>
    </a>
    
   <a href="/fssm/" class="holo-card">
      <h3>FSSM</h3>
      <p>Formation académique, projets et compétences acquises</p>
    </a>
    
   <a href="/tryhackme/" class="holo-card">
      <h3>TRYHACKME</h3>
      <p>Paths complétés, badges et write-ups de challenges</p>
    </a>
    
  <a href="/my-lab/" class="holo-card">
      <h3>MON LAB</h3>
      <p>Environnement de test, machines virtuelles et expériences</p>
   </a>
  </div>
  <div class="welcome-text">
    <p>Salut — je suis <strong style="color: #3b82f6;">Haname</strong>, étudiante en cybersécurité à la FSSM.<br>
    Bienvenue sur mon site où je partage mon parcours, mes parcours (paths) TryHackMe, la formation FSSM, et mes laboratoires personnels.</p>
  </div>
  <!-- COMPTEUR SIMPLE -->
<div style="text-align: center; margin: 30px 0;">
  <div style="display: inline-block; background: rgba(15, 23, 42, 0.7); border: 1px solid #3b82f6; border-radius: 10px; padding: 15px 30px; box-shadow: 0 0 15px rgba(59, 130, 246, 0.3);">
    <div style="color: #94a3b8; font-size: 0.9em; margin-bottom: 8px; letter-spacing: 2px;">👁️ VISITEURS</div>
    <div style="color: #60a5fa; font-size: 2em; font-weight: 700; text-shadow: 0 0 10px #60a5fa;" id="visitorCount">0</div>
  </div>
</div>

<script>
let visits = parseInt(localStorage.getItem('cyberiaVisits') || '0');
visits++;
localStorage.setItem('cyberiaVisits', visits);
document.getElementById('visitorCount').textContent = visits;
</script>
  <div class="badge-container">
    <a href="/tryhackme/" class="floating-badge">TRYHACKME</a>
    <a href="https://github.com/ItsHaname" class="floating-badge" target="_blank">GITHUB</a>
    <a href="#" class="floating-badge">TWITTER</a>
    <a href="#" class="floating-badge">LINKEDIN</a>
  </div>
  <div class="cyber-footer">
    © 2025 CYBERIA — HANAME — FSSM — Personal Knowledge Repository
  </div>
</div>
