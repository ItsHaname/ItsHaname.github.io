---
layout: default
title: Parcours FSSM
nav: fssm
---
<link rel="icon" href="https://raw.githubusercontent.com/ItsHaname/ItsHaname.github.io/main/logo" type="image/png">
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

@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

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

/* Header CYBERIA */
.cyberia-header {
    text-align: center;
    margin-bottom: 60px;
    padding: 40px 20px;
    background: rgba(0, 20, 40, 0.6);
    border-radius: 30px;
    border: 3px solid #1e4d7b;
    box-shadow: 0 0 40px rgba(30, 77, 123, 0.5), inset 0 0 30px rgba(30, 77, 123, 0.2);
}

.cyberia-title {
    font-size: 5em;
    color: #ff6b4a;
    text-shadow: 
        0 0 10px #ff6b4a,
        0 0 20px #ff6b4a,
        0 0 30px #ff6b4a,
        0 0 40px #ff3300;
    margin: 0;
    font-weight: 900;
    letter-spacing: 10px;
    text-transform: uppercase;
    font-style: italic;
    -webkit-text-stroke: 2px #ff3300;
}

.cyberia-line {
    width: 100%;
    height: 3px;
    background: linear-gradient(90deg, transparent, #1e4d7b, #3b82f6, #1e4d7b, transparent);
    margin: 20px auto;
    max-width: 500px;
    box-shadow: 0 0 15px #3b82f6;
}

.cyberia-subtitle {
    font-size: 1.8em;
    color: #60a5fa;
    margin: 10px 0 0 0;
    text-shadow: 0 0 10px #60a5fa, 0 0 20px #3b82f6, 0 0 30px #2563eb;
    letter-spacing: 4px;
    font-weight: 300;
    font-style: italic;
}

.cyberia-subtitle::after {
    content: '_';
    animation: blink 1s infinite;
    color: #60a5fa;
}

/* FSSM Section */
.fssm-hero {
    text-align: center;
    margin-bottom: 60px;
    padding: 50px 20px;
    background: linear-gradient(135deg, rgba(0, 20, 40, 0.9), rgba(15, 23, 42, 0.8));
    border-radius: 30px;
    border: 3px solid #1e4d7b;
    box-shadow: 0 0 40px rgba(30, 77, 123, 0.5);
}

.semester-badge {
    display: inline-block;
    padding: 15px 40px;
    background: linear-gradient(135deg, #ff6b4a, #ff3300);
    color: white;
    font-size: 1.8em;
    font-weight: 900;
    border-radius: 50px;
    margin-bottom: 30px;
    box-shadow: 0 10px 30px rgba(255, 107, 74, 0.5);
    animation: pulse 3s infinite;
    letter-spacing: 3px;
}

.fssm-title {
    font-size: 4em;
    color: transparent;
    background: linear-gradient(90deg, #3b82f6, #60a5fa, #2563eb, #60a5fa, #3b82f6);
    background-size: 300% auto;
    -webkit-background-clip: text;
    background-clip: text;
    animation: gradientBG 3s ease infinite;
    margin: 30px 0;
    font-weight: 900;
    letter-spacing: 5px;
    text-transform: uppercase;
}

.fssm-subtitle {
    font-size: 1.5em;
    color: #60a5fa;
    margin: 20px 0;
    font-style: italic;
    letter-spacing: 2px;
}

.university-name {
    font-size: 1.2em;
    color: #94a3b8;
    margin-top: 20px;
    text-transform: uppercase;
    letter-spacing: 2px;
}

/* Modules Grid */
.hologram-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin: 60px 0;
}

.holo-card {
    background: rgba(15, 23, 42, 0.85);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 15px;
    padding: 30px;
    text-align: center;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    position: relative;
    overflow: hidden;
    text-decoration: none;
    color: inherit;
    display: block;
    cursor: pointer;
}

.holo-card:before {
    content: '';
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #3b82f6, #60a5fa, transparent);
    z-index: -1;
    opacity: 0;
    transition: opacity 0.4s;
}

.holo-card:hover:before {
    opacity: 0.5;
}

.holo-card:hover {
    transform: translateY(-10px) scale(1.02);
    border-color: #60a5fa;
    box-shadow: 0 15px 35px rgba(59, 130, 246, 0.3);
}

/* Style pour le module Done (S5) */
.holo-card.done {
    background: rgba(16, 185, 129, 0.1);
    border: 1px solid rgba(16, 185, 129, 0.4);
}

.holo-card.done:before {
    background: linear-gradient(45deg, #10b981, #34d399, transparent);
}

.holo-card.done .module-icon {
    color: #10b981;
}

.holo-card.done h3 {
    color: #10b981;
}

.holo-card.done .module-status {
    background: rgba(16, 185, 129, 0.15);
    border: 1px solid rgba(16, 185, 129, 0.4);
    color: #34d399;
}

.holo-card.done .status-dot {
    background: #10b981;
}

.module-icon {
    font-size: 2em;
    margin-bottom: 15px;
    animation: floatUpDown 3s ease-in-out infinite;
    font-weight: 900;
    color: #3b82f6;
    text-shadow: 0 0 10px rgba(59, 130, 246, 0.5);
}

.holo-card h3 {
    color: #3b82f6;
    margin: 0 0 15px 0;
    font-size: 1.5em;
    font-weight: 600;
}

.holo-card p {
    color: #cbd5e1;
    margin: 0;
    line-height: 1.6;
    font-size: 0.95em;
}

.module-status {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(59, 130, 246, 0.15);
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 0.9em;
    color: #60a5fa;
    border: 1px solid rgba(59, 130, 246, 0.3);
    margin-top: 15px;
}

.status-dot {
    width: 8px;
    height: 8px;
    background: #3b82f6;
    border-radius: 50%;
    animation: pulse 2s infinite;
}

/* Section divider */
.semester-divider {
    text-align: center;
    margin: 60px 0 40px 0;
    padding: 20px;
    background: rgba(15, 23, 42, 0.5);
    border-radius: 15px;
    border-top: 2px solid #1e4d7b;
    border-bottom: 2px solid #1e4d7b;
}

.semester-divider h2 {
    color: #94a3b8;
    font-size: 1.5em;
    font-weight: 400;
    letter-spacing: 2px;
    margin: 0;
}

/* Info Section */
.welcome-text {
    text-align: center;
    font-size: 1.2em;
    color: #94a3b8;
    margin: 50px 0;
    padding: 30px;
    background: rgba(15, 23, 42, 0.7);
    border-radius: 15px;
    border-left: 4px solid #3b82f6;
    animation: slideIn 1s ease-out;
}

.cyber-footer {
    text-align: center;
    margin-top: 80px;
    padding: 40px;
    background: linear-gradient(135deg, rgba(15, 23, 42, 0.8), rgba(0, 20, 40, 0.9));
    border-radius: 20px;
    border: 2px solid #1e4d7b;
    color: #94a3b8;
    font-size: 1.1em;
    line-height: 1.8;
}

@media (max-width: 1024px) {
    .hologram-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .cyberia-title {
        font-size: 3em;
        letter-spacing: 5px;
    }
    
    .cyberia-subtitle {
        font-size: 1.2em;
        letter-spacing: 2px;
    }
    
    .fssm-title {
        font-size: 2.5em;
    }
    
    .semester-badge {
        font-size: 1.3em;
        padding: 12px 30px;
    }
    
    .hologram-grid {
        grid-template-columns: 1fr;
        gap: 20px;
    }
}
</style>

<div class="binary-background"></div>

<div class="container">
    <!-- CYBERIA Header -->
    <div class="cyberia-header">
        <div class="cyberia-title">CYBERIA</div>
        <div class="cyberia-line"></div>
        <div class="cyberia-subtitle">Cafe & Club</div>
    </div>
   
   <!-- FSSM Hero Section -->
 <div class="fssm-hero">
        <div class="semester-badge">S6</div>
        <div class="fssm-title">Formation FSSM</div>
        <div class="fssm-subtitle">Cybersecurity & Network Engineering</div>
        <div class="university-name">Faculté des Sciences Semlalia • Marrakech</div>
    </div>
    
 <div class="welcome-text">
        <p><strong style="color: #3b82f6;">Semestre 6</strong> • Janvier - Juin 2025<br>
        Formation spécialisée en Cybersécurité et Réseaux avec 5 modules avancés.</p>
    </div>
   
   <!-- Modules Grid S6 -->
  <div class="hologram-grid">
        <a href="{{ site.baseurl }}/fssm/Iot" class="holo-card">
            <div class="module-icon">M1</div>
            <h3>IoT Analyse et Connexion</h3>
            <p>Internet des objets, protocoles IoT, analyse de données connectées</p>
            <div class="module-status">
                <span class="status-dot"></span>
                En cours
            </div>
        </a>

<a href="{{ site.baseurl }}/fssm/programmation-reseau" class="holo-card">
            <div class="module-icon">M2</div>
            <h3>Parallélisme & Programmation Réseaux</h3>
            <p>Programmation parallèle, sockets, protocoles réseau avancés</p>
            <div class="module-status">
                <span class="status-dot"></span>
                En cours
            </div>
        </a>
        
  <a href="{{ site.baseurl }}/fssm/droit" class="holo-card">
            <div class="module-icon">M3</div>
            <h3>Droit Digital</h3>
            <p>RGPD, propriété intellectuelle, aspects juridiques du numérique</p>
            <div class="module-status">
                <span class="status-dot"></span>
                En cours
            </div>
        </a>

 <a href="{{ site.baseurl }}/fssm/Gouvernance" class="holo-card">
            <div class="module-icon">M4</div>
            <h3>Gouvernance de la Sécurité</h3>
            <p>ISO 27001, gestion des risques, politiques de sécurité</p>
            <div class="module-status">
                <span class="status-dot"></span>
                En cours
            </div>
        </a>
        
 <a href="{{ site.baseurl }}/fssm/crypto" class="holo-card">
            <div class="module-icon">M5</div>
            <h3>Cryptographie & Cybersécurité</h3>
            <p>Chiffrement, PKI, signatures numériques, sécurité applicative</p>
            <div class="module-status">
                <span class="status-dot"></span>
                En cours
            </div>
        </a>
    </div>

    <!-- Semester Divider -->
   <div class="semester-divider">
        <h2>📚 Modules from Previous Semester</h2>
    </div>

    <!-- Modules Grid S5 -->
<div class="hologram-grid">
        <a href="{{ site.baseurl }}/fssm/s5" class="holo-card done">
            <div class="module-icon">S5</div>
            <h3>Pentesting Digital Forensics<br>& Services Réseau et Cloud</h3>
            <p>Pentest, analyse forensique, Cloud Computing, services réseau avancés</p>
            <div class="module-status">
                <span class="status-dot"></span>
                Complété
            </div>
        </a>
    </div>

    <!-- Footer -->
 <div class="cyber-footer">
        Année académique <span style="color: #60a5fa; font-weight: bold;">2025-2026</span><br>
        FSSM - Faculté des Sciences Semlalia, Marrakech<br>
        Spécialité: <span style="color: #3b82f6; font-weight: bold;">Cybersécurité & Réseau</span>
    </div>
</div>

<script>
// Create binary rain background
document.addEventListener('DOMContentLoaded', function() {
    const binaryContainer = document.querySelector('.binary-background');
    
    // Falling binary digits
    for (let i = 0; i < 100; i++) {
        const digit = document.createElement('div');
        digit.className = 'binary-digit';
        digit.textContent = Math.random() > 0.5 ? '1' : '0';
        digit.style.left = Math.random() * 100 + 'vw';
        digit.style.fontSize = (Math.random() * 18 + 12) + 'px';
        digit.style.animationDuration = (Math.random() * 10 + 5) + 's';
        digit.style.animationDelay = Math.random() * 5 + 's';
        digit.style.opacity = Math.random() * 0.2 + 0.05;
        const colors = ['rgba(59, 130, 246, 0.15)', 'rgba(96, 165, 250, 0.15)', 'rgba(37, 99, 235, 0.15)'];
        digit.style.color = colors[Math.floor(Math.random() * colors.length)];
        binaryContainer.appendChild(digit);
    }
    
    // Floating binary digits
    for (let i = 0; i < 30; i++) {
        const floatDigit = document.createElement('div');
        floatDigit.className = 'binary-digit float';
        floatDigit.textContent = Math.random() > 0.5 ? '1' : '0';
        floatDigit.style.left = Math.random() * 100 + 'vw';
        floatDigit.style.top = Math.random() * 100 + 'vh';
        floatDigit.style.fontSize = (Math.random() * 22 + 14) + 'px';
        floatDigit.style.animationDelay = Math.random() * 2 + 's';
        floatDigit.style.opacity = Math.random() * 0.3 + 0.1;
        const floatColors = ['rgba(59, 130, 246, 0.25)', 'rgba(96, 165, 250, 0.25)', 'rgba(37, 99, 235, 0.25)'];
        floatDigit.style.color = floatColors[Math.floor(Math.random() * floatColors.length)];
        binaryContainer.appendChild(floatDigit);
    }
});
</script>
