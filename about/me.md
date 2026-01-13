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

@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

@keyframes slideInUp {
    from { opacity: 0; transform: translateY(50px); }
    to { opacity: 1; transform: translateY(0); }
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
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    color: #e2e8f0;
    overflow-x: hidden;
}

/* Fond avec dégradés subtils */
body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: 
        radial-gradient(circle at 10% 20%, rgba(59, 130, 246, 0.1) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(37, 99, 235, 0.05) 0%, transparent 40%);
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
    color: rgba(59, 130, 246, 0.15);
    animation: matrixRain linear infinite;
}

/* --- LAYOUT --- */
.about-container {
    max-width: 1500px; /* Élargi au maximum */
    margin: 0 auto;
    padding: 80px 50px;
    position: relative;
    z-index: 2;
}

.main-layout {
    display: grid;
    grid-template-columns: 420px 1fr; /* Sidebar plus équilibrée */
    gap: 80px;
    align-items: start;
}

/* --- SIDEBAR (GAUCHE) --- */
.profile-sidebar {
    position: sticky;
    top: 40px;
}

.profile-card {
    background: rgba(15, 23, 42, 0.7);
    backdrop-filter: blur(15px);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 40px;
    padding: 60px 40px;
    text-align: center;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.7);
}

.profile-image-wrapper {
    width: 250px;
    height: 250px;
    margin: 0 auto 30px;
    position: relative;
}

.profile-image {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    border: 4px solid #3b82f6;
    overflow: hidden;
    animation: float 6s ease-in-out infinite;
    box-shadow: 0 0 40px rgba(59, 130, 246, 0.3);
}

.profile-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.profile-name {
    font-size: 3em;
    font-weight: 800;
    letter-spacing: -1px;
    background: linear-gradient(135deg, #fff 0%, #3b82f6 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

.profile-info {
    margin-top: 40px;
    text-align: left;
    background: rgba(30, 41, 59, 0.5);
    padding: 25px;
    border-radius: 20px;
}

.info-row {
    display: flex;
    justify-content: space-between;
    padding: 15px 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.info-label { color: #94a3b8; font-weight: 500; }
.info-value { color: #60a5fa; font-weight: 600; }

/* --- CONTENT AREA (DROITE) --- */
.content-area {
    display: flex;
    flex-direction: column;
    gap: 40px;
}

.content-header h1 {
    font-size: 5.5em; /* Titre massif pour Cyberia */
    font-weight: 900;
    line-height: 0.85;
    letter-spacing: -4px;
    margin-bottom: 20px;
    background: linear-gradient(to right, #ffffff, #3b82f6, #2563eb);
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: gradientShift 5s linear infinite;
}

.content-tagline {
    font-size: 1.8em;
    color: #94a3b8;
    font-weight: 300;
}

.content-tagline::after {
    content: '_';
    animation: blink 1s infinite;
    color: #3b82f6;
}

/* Grandes sections de contenu */
.content-section {
    background: rgba(15, 23, 42, 0.5);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.05);
    border-left: 5px solid #3b82f6; /* Accentuation latérale */
    border-radius: 30px;
    padding: 60px;
    transition: transform 0.3s ease, background 0.3s ease;
}

.content-section:hover {
    background: rgba(15, 23, 42, 0.7);
    transform: translateX(10px);
}

.content-section h2 {
    font-size: 2.5em;
    color: #60a5fa;
    margin-bottom: 30px;
    font-weight: 700;
}

.content-section p {
    font-size: 1.25em;
    line-height: 1.8;
    color: #cbd5e1;
    margin-bottom: 20px;
}

/* Grille de Focus élargie */
.focus-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* 2 colonnes pour remplir l'espace */
    gap: 30px;
    margin-top: 40px;
}

.focus-item {
    background: rgba(30, 41, 59, 0.4);
    border: 1px solid rgba(59, 130, 246, 0.2);
    border-radius: 25px;
    padding: 40px;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.focus-item:hover {
    background: rgba(59, 130, 246, 0.1);
    border-color: #3b82f6;
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.focus-item h3 {
    font-size: 1.5em;
    color: #fff;
    margin-bottom: 15px;
}

.highlight {
    color: #60a5fa;
    font-weight: 700;
    padding: 0 5px;
    background: rgba(59, 130, 246, 0.1);
}

/* RESPONSIVE */
@media (max-width: 1200px) {
    .main-layout { grid-template-columns: 1fr; }
    .profile-sidebar { position: relative; top: 0; }
    .content-header h1 { font-size: 4em; }
}

@media (max-width: 768px) {
    .focus-grid { grid-template-columns: 1fr; }
    .about-container { padding: 40px 20px; }
    .content-section { padding: 30px; }
}
</style>

<div class="binary-background" id="binaryBg"></div>

<div class="about-container">
    <div class="main-layout">
        <aside class="profile-sidebar">
            <div class="profile-card">
                <div class="profile-image-wrapper">
                    <div class="profile-image">
                        <img src="https://github.com/user-attachments/assets/6c553521-15b0-4d1a-aa6f-798d79f1c896" alt="Hanane">
                    </div>
                </div>
                
  <h2 class="profile-name">HANANE</h2>
                <p style="color: #94a3b8; font-size: 1.1em;">Network Security & Cybersecurity Student</p>
                
   <div class="profile-info">
                    <div class="info-row">
                        <span class="info-label">Location</span>
                        <span class="info-value">Marrakech, MA</span>
                    </div>
                    <div class="info-row">
                        <span class="info-label">University</span>
                        <span class="info-value">FSSM</span>
                    </div>
                    <div class="info-row">
                        <span class="info-label">Status</span>
                        <span class="info-value">Active Learner</span>
                    </div>
                </div>
            </div>
        </aside>
 <main class="content-area">
            <div class="content-header">
                <h1>WELCOME TO<br>CYBERIA.</h1>
                <p class="content-tagline">Scanning the horizon of offensive security</p>
            </div>

 <section class="content-section">
                <h2>01. Background</h2>
                <p>
                    I'm <span class="highlight">Hanane</span>, a cybersecurity student at FSSM, Cadi Ayyad University. 
                    I specialize in <span class="highlight">vulnerability analysis</span> and <span class="highlight">offensive tactics</span>.
                </p>
                <p>
                    This space is my digital laboratory, where I document technical challenges, 
                    academic research, and my evolution in the cybersecurity landscape.
                </p>
            </section>

   <section class="content-section">
                <h2>02. Learning Path</h2>
                <div class="focus-grid">
                    <div class="focus-item">
                        <h3>Academic Projects</h3>
                        <p>In-depth look into Networking and Security courses (NSC program).</p>
                    </div>
                <div class="focus-item">
                        <h3>TryHackMe</h3>
                        <p>Detailed write-ups and methodologies for solving CTF machines.</p>
                    </div>
 <div class="focus-item">
                        <h3>Home Lab</h3>
                        <p>Virtual environments built for malware analysis and testing.</p>
                    </div>
 <div class="focus-item">
                        <h3>Future Goals</h3>
                        <p>Pursuing professional certifications and deeper binary exploitation skills.</p>
                    </div>
                </div>
            </section>
        </main>
    </div>
</div>

<script>
function createBinaryBackground() {
    const container = document.getElementById('binaryBg');
    const numberOfDigits = 60;

    for (let i = 0; i < numberOfDigits; i++) {
        const digit = document.createElement('div');
        digit.className = 'binary-digit';
        digit.textContent = Math.random() > 0.5 ? '0' : '1';
        digit.style.left = Math.random() * 100 + '%';
        digit.style.fontSize = (Math.random() * 10 + 15) + 'px';
        digit.style.animationDuration = (Math.random() * 8 + 7) + 's';
        digit.style.animationDelay = Math.random() * 5 + 's';
        digit.style.opacity = Math.random() * 0.3;
        container.appendChild(digit);
    }
}
createBinaryBackground();
</script>
