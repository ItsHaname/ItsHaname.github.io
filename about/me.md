---
layout: default
title: About
nav: about
---

<style>
/* --- ANIMATIONS --- */
@keyframes matrixRain {
    0% { transform: translateY(-100vh); }
    100% { transform: translateY(100vh); }
}

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

/* --- BASE STYLES --- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: #050810;
    min-height: 100vh;
    font-family: 'Inter', -apple-system, sans-serif;
    color: #e2e8f0;
    overflow-x: hidden;
}

/* Fond dynamique */
body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: 
        radial-gradient(circle at 15% 15%, rgba(59, 130, 246, 0.15) 0%, transparent 50%),
        radial-gradient(circle at 85% 85%, rgba(37, 99, 235, 0.1) 0%, transparent 50%);
    z-index: 0;
}

.binary-background {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    pointer-events: none;
    z-index: 1;
}

.binary-digit {
    position: absolute;
    font-family: 'Courier New', monospace;
    color: rgba(59, 130, 246, 0.12);
    animation: matrixRain linear infinite;
}

/* --- LAYOUT ULTRA-LARGE --- */
.about-container {
    width: 95%;            /* Utilise presque toute la largeur */
    max-width: 1800px;     /* Limite maximum très haute pour les écrans géants */
    margin: 0 auto;
    padding: 60px 20px;
    position: relative;
    z-index: 2;
}

.main-layout {
    display: grid;
    grid-template-columns: 450px 1fr; /* Sidebar fixe, le reste prend TOUT l'espace */
    gap: 50px;
    align-items: start;
}

/* --- SIDEBAR --- */
.profile-sidebar {
    position: sticky;
    top: 40px;
}

.profile-card {
    background: rgba(15, 23, 42, 0.8);
    backdrop-filter: blur(20px);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 40px;
    padding: 60px 40px;
    text-align: center;
    box-shadow: 0 0 50px rgba(0, 0, 0, 0.5);
}

.profile-image {
    width: 280px;
    height: 280px;
    margin: 0 auto 30px;
    border-radius: 50%;
    border: 5px solid #3b82f6;
    overflow: hidden;
    animation: float 6s ease-in-out infinite;
    box-shadow: 0 0 30px rgba(59, 130, 246, 0.4);
}

.profile-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* --- CONTENU --- */
.content-area {
    display: flex;
    flex-direction: column;
    gap: 40px;
}

.content-header h1 {
    font-size: 7vw; /* Taille basée sur la largeur de l'écran (très grand) */
    font-weight: 900;
    line-height: 1;
    letter-spacing: -5px;
    background: linear-gradient(to right, #fff, #3b82f6, #60a5fa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 20px;
}

/* Sections de contenu larges */
.content-section {
    width: 100%; /* Prend toute la largeur de la colonne de droite */
    background: rgba(15, 23, 42, 0.5);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.05);
    border-radius: 35px;
    padding: 70px; /* Plus de padding interne pour faire respirer */
    transition: all 0.4s ease;
}

.content-section:hover {
    background: rgba(15, 23, 42, 0.7);
    border-color: rgba(59, 130, 246, 0.5);
    transform: scale(1.01); /* Effet d'agrandissement subtil */
}

.content-section h2 {
    font-size: 3em;
    color: #3b82f6;
    margin-bottom: 30px;
}

.content-section p {
    font-size: 1.4em; /* Texte plus grand pour remplir l'espace */
    line-height: 1.7;
    color: #cbd5e1;
}

/* GRILLE DE FOCUS (Passage à 3 colonnes) */
.focus-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); /* S'adapte automatiquement */
    gap: 30px;
    margin-top: 40px;
}

.focus-item {
    background: rgba(30, 41, 59, 0.4);
    border: 1px solid rgba(59, 130, 246, 0.1);
    border-radius: 25px;
    padding: 40px;
    transition: all 0.3s ease;
}

.focus-item:hover {
    background: rgba(59, 130, 246, 0.15);
    border-color: #3b82f6;
    transform: translateY(-10px);
}

.focus-item h3 {
    font-size: 1.8em;
    margin-bottom: 15px;
    color: #fff;
}

/* RESPONSIVE */
@media (max-width: 1400px) {
    .main-layout { grid-template-columns: 1fr; }
    .profile-sidebar { position: relative; top: 0; }
    .content-header h1 { font-size: 10vw; }
}
</style>

<div class="binary-background" id="binaryBg"></div>

<div class="about-container">
    <div class="main-layout">
        <aside class="profile-sidebar">
            <div class="profile-card">
                <div class="profile-image">
                    <img src="https://github.com/user-attachments/assets/6c553521-15b0-4d1a-aa6f-798d79f1c896" alt="Hanane">
                </div>
                <h2 style="font-size: 3.5em; font-weight: 800; color: #fff; margin-bottom: 10px;">HANANE</h2>
                <p style="color: #60a5fa; font-size: 1.3em; font-weight: 600;">CYBERSECURITY ANALYST</p>
                
  <div style="margin-top: 30px; text-align: left; background: rgba(0,0,0,0.2); padding: 20px; border-radius: 20px;">
                    <div style="display:flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid rgba(255,255,255,0.05);">
                        <span>Location:</span> <span style="color:#fff">Marrakech</span>
                    </div>
                    <div style="display:flex; justify-content: space-between; padding: 10px 0;">
                        <span>Univ:</span> <span style="color:#fff">FSSM</span>
                    </div>
                </div>
            </div>
        </aside>
  <main class="content-area">
            <div class="content-header">
                <h1>WELCOME TO<br>CYBERIA.</h1>
                <p style="font-size: 2em; color: #94a3b8;">// The Personal Lab of Hanane</p>
            </div>

   <section class="content-section">
                <h2>01. Background</h2>
                <p>
                    I am a Cybersecurity student at <span style="color: #60a5fa; font-weight: bold;">Cadi Ayyad University</span>. 
                    My work focuses on the intersection of networking and security. I am deeply interested in 
                    how systems fail, how they are breached, and most importantly, how they can be fortified.
                </p>
            </section>

  <section class="content-section">
                <h2>02. Area of Expertise</h2>
                <div class="focus-grid">
                    <div class="focus-item">
                        <h3>Pentesting</h3>
                        <p>Vuln analysis and exploitation walkthroughs.</p>
                    </div>
                    <div class="focus-item">
                        <h3>Networking</h3>
                        <p>Advanced routing, switching, and firewall configuration.</p>
                    </div>
                    <div class="focus-item">
                        <h3>Reverse Eng.</h3>
                        <p>Decompiling and analyzing malware behavior.</p>
                    </div>
                    <div class="focus-item">
                        <h3>Write-ups</h3>
                        <p>Documentation of CTF challenges and THM rooms.</p>
                    </div>
                </div>
            </section>
        </main>
    </div>
</div>

<script>
function createBinaryBackground() {
    const container = document.getElementById('binaryBg');
    for (let i = 0; i < 80; i++) {
        const digit = document.createElement('div');
        digit.className = 'binary-digit';
        digit.textContent = Math.random() > 0.5 ? '0' : '1';
        digit.style.left = Math.random() * 100 + '%';
        digit.style.fontSize = (Math.random() * 10 + 14) + 'px';
        digit.style.animationDuration = (Math.random() * 10 + 5) + 's';
        digit.style.opacity = Math.random() * 0.2;
        container.appendChild(digit);
    }
}
createBinaryBackground();
</script>
