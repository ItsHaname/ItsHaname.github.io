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

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

body {
  background: #0a0e1a;
  min-height: 100vh;
  margin: 0;
  overflow-x: hidden;
}

.binary-background {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: -1;
}

.binary-digit {
  position: absolute;
  font-family: monospace;
  animation: matrixRain linear infinite;
}

.container {
  max-width: 1200px;
  margin: auto;
  padding: 40px 20px;
}

/* HEADER CYBERIA */
.cyberia-header {
  text-align: center;
  margin-bottom: 80px;
  padding: 50px 20px;
  background: rgba(0, 20, 40, 0.6);
  border-radius: 40px;
  border: 3px solid #1e4d7b;
  box-shadow: 0 0 50px rgba(30,77,123,.6);
}

/* AUTRES STYLES */
.neon-title {
  font-size: 3em;
  text-align: center;
  color: transparent;
  background: linear-gradient(90deg,#3b82f6,#60a5fa,#2563eb);
  -webkit-background-clip: text;
  animation: gradientBG 3s infinite;
  font-weight: 900;
}

.subtitle {
  text-align: center;
  color: #94a3b8;
  font-style: italic;
}

.hologram-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
  gap: 20px;
  margin: 60px 0;
}

.holo-card {
  background: rgba(15,23,42,.85);
  padding: 30px;
  border-radius: 15px;
  text-align: center;
  border: 1px solid rgba(59,130,246,.3);
  transition: .4s;
  color: inherit;
  text-decoration: none;
}

.holo-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(59,130,246,.4);
}

.holo-card h3 {
  color: #3b82f6;
}

.welcome-text {
  text-align: center;
  color: #94a3b8;
  margin: 50px 0;
}

.badge-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.floating-badge {
  padding: 12px 25px;
  border-radius: 30px;
  background: rgba(15,23,42,.8);
  border: 1px solid #1e40af;
  color: #60a5fa;
  text-decoration: none;
  animation: pulse 2s infinite;
}

.cyber-footer {
  margin-top: 80px;
  text-align: center;
  color: #64748b;
  font-size: .9em;
}
</style>

<script>
document.addEventListener("DOMContentLoaded",()=>{
  const bg=document.createElement("div");
  bg.className="binary-background";
  document.body.appendChild(bg);
  for(let i=0;i<120;i++){
    const d=document.createElement("div");
    d.className="binary-digit";
    d.textContent=Math.random()>.5?"1":"0";
    d.style.left=Math.random()*100+"vw";
    d.style.fontSize=12+Math.random()*18+"px";
    d.style.animationDuration=5+Math.random()*10+"s";
    d.style.opacity=Math.random()*.2;
    d.style.color="rgba(59,130,246,.2)";
    bg.appendChild(d);
  }
});
</script>

<div class="container">

  <!-- LOGO CYBERIA EXACT -->
  <div class="cyberia-header">
    <svg viewBox="0 0 900 420" width="100%" style="max-width:900px;margin:auto;display:block">

      <path d="M90 190
               C60 90,180 40,300 70
               C360 30,480 30,550 80
               C700 70,800 140,760 240
               C780 330,640 360,520 330
               C430 370,300 360,240 320
               C120 340,60 270,90 190 Z"
            fill="none"
            stroke="#e5f3ff"
            stroke-width="14"
            filter="url(#wg)" />

      <text x="450" y="220"
            text-anchor="middle"
            font-size="140"
            letter-spacing="10"
            fill="none"
            stroke="#ff6b4a"
            stroke-width="6"
            filter="url(#pg)"
            style="font-weight:900;font-style:italic">
        CYBERIA
      </text>

      <text x="450" y="330"
            text-anchor="middle"
            font-size="72"
            fill="#e5f3ff"
            filter="url(#wg)"
            style="font-style:italic">
        Cafe &amp; Club
      </text>

      <defs>
        <filter id="wg">
          <feGaussianBlur stdDeviation="6"/>
        </filter>
        <filter id="pg">
          <feGaussianBlur stdDeviation="5"/>
        </filter>
      </defs>

    </svg>
  </div>

  <div class="neon-title">WELCOME TO MY CYBERSPACE</div>
  <div class="subtitle">A digital notebook for everything I learn</div>

  <div class="hologram-grid">
    <a href="{{ site.baseurl }}/about" class="holo-card"><h3>À PROPOS</h3></a>
    <a href="{{ site.baseurl }}/fssm" class="holo-card"><h3>FSSM</h3></a>
    <a href="{{ site.baseurl }}/tryhackme" class="holo-card"><h3>TRYHACKME</h3></a>
    <a href="{{ site.baseurl }}/my-lab" class="holo-card"><h3>MON LAB</h3></a>
  </div>

  <div class="welcome-text">
    Salut — je suis <strong style="color:#3b82f6">Haname</strong>, étudiante en cybersécurité.
  </div>

  <div class="badge-container">
    <a class="floating-badge" href="{{ site.baseurl }}/tryhackme">TRYHACKME</a>
    <a class="floating-badge" href="https://github.com/ItsHaname">GITHUB</a>
    <a class="floating-badge" href="#">TWITTER</a>
    <a class="floating-badge" href="#">LINKEDIN</a>
  </div>

  <div class="cyber-footer">
    © 2025 CYBERIA — HANAME — FSSM
  </div>

</div>
