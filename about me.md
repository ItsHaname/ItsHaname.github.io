---
layout: default
title: About Me - Hanane
permalink: /about/
---

<style>
  :root {
    --neon-cyan: #00d4ff;
    --neon-green: #00ff88;
    --neon-pink: #ff00ff;
    --dark-bg: #0a0e27;
    --card-bg: #1a1f3a;
  }
  
  body {
    background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0a0e27 100%);
    color: #fff;
    font-family: 'Segoe UI', system-ui, sans-serif;
  }
  
  .about-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
  }
  
  .profile-header {
    display: grid;
    grid-template-columns: 300px 1fr;
    gap: 3rem;
    margin-bottom: 4rem;
    align-items: start;
  }
  
  .profile-image-container {
    position: relative;
  }
  
  .profile-image {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    border: 4px solid var(--neon-cyan);
    box-shadow: 0 0 50px rgba(0, 212, 255, 0.6),
                0 0 100px rgba(0, 255, 136, 0.3);
    animation: float 3s ease-in-out infinite;
    object-fit: cover;
    background: var(--card-bg);
  }
  
  @keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
  }
  
  .profile-image-container::before {
    content: '';
    position: absolute;
    top: -10px;
    left: -10px;
    right: -10px;
    bottom: -10px;
    border-radius: 50%;
    background: linear-gradient(45deg, var(--neon-cyan), var(--neon-green), var(--neon-pink));
    z-index: -1;
    opacity: 0.3;
    animation: rotate 4s linear infinite;
  }
  
  @keyframes rotate {
    100% { transform: rotate(360deg); }
  }
  
  .profile-info {
    padding: 2rem;
  }
  
  .profile-name {
    font-size: 3.5rem;
    font-weight: bold;
    background: linear-gradient(135deg, var(--neon-cyan), var(--neon-pink));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 0.5rem;
  }
  
  .profile-role {
    font-size: 1.8rem;
    color: var(--neon-green);
    margin-bottom: 1rem;
    font-weight: 300;
  }
  
  .profile-tagline {
    font-size: 1.2rem;
    color: #bbb;
    line-height: 1.8;
    margin-bottom: 2rem;
    font-style: italic;
  }
  
  .quick-info {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
    margin-top: 2rem;
  }
  
  .info-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem;
    background: rgba(26, 31, 58, 0.6);
    border-radius: 10px;
    border-left: 3px solid var(--neon-cyan);
  }
  
  .info-icon {
    font-size: 1.5rem;
  }
  
  .info-label {
    color: #888;
    font-size: 0.9rem;
  }
  
  .info-value {
    color: var(--neon-cyan);
    font-weight: bold;
  }
  
  .section {
    background: rgba(26, 31, 58, 0.6);
    border: 2px solid var(--neon-green);
    border-radius: 20px;
    padding: 2.5rem;
    margin-bottom: 2rem;
    transition: all 0.3s;
  }
  
  .section:hover {
    box-shadow: 0 10px 50px rgba(0, 255, 136, 0.3);
    transform: translateY(-5px);
  }
  
  .section-title {
    font-size: 2rem;
    color: var(--neon-green);
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  
  .section-icon {
    font-size: 2.5rem;
  }
  
  .timeline {
    position: relative;
    padding-left: 2rem;
  }
  
  .timeline::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 2px;
    background: linear-gradient(180deg, var(--neon-cyan), var(--neon-green));
  }
  
  .timeline-item {
    position: relative;
    margin-bottom: 2rem;
    padding-left: 2rem;
  }
  
  .timeline-item::before {
    content: '';
    position: absolute;
    left: -2.4rem;
    top: 0.5rem;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background: var(--neon-cyan);
    box-shadow: 0 0 20px var(--neon-cyan);
  }
  
  .timeline-date {
    color: var(--neon-pink);
    font-weight: bold;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
  }
  
  .timeline-title {
    color: var(--neon-cyan);
    font-size: 1.3rem;
    font-weight: bold;
    margin-bottom: 0.3rem;
  }
  
  .timeline-org {
    color: var(--neon-green);
    font-size: 1.1rem;
    margin-bottom: 0.5rem;
  }
  
  .timeline-desc {
    color: #bbb;
    line-height: 1.6;
  }
  
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
  }
  
  .skill-category {
    background: rgba(0, 0, 0, 0.3);
    padding: 1.5rem;
    border-radius: 15px;
    border: 1px solid rgba(0, 212, 255, 0.3);
  }
  
  .skill-category-title {
    color: var(--neon-cyan);
    font-weight: bold;
    margin-bottom: 1rem;
    font-size: 1.2rem;
  }
  
  .skill-list {
    list-style: none;
    padding: 0;
  }
  
  .skill-list li {
    padding: 0.5rem 0;
    color: #bbb;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  
  .skill-list li::before {
    content: '▹';
    color: var(--neon-green);
    font-weight: bold;
    font-size: 1.2rem;
  }
  
  .achievement-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
  }
  
  .achievement-card {
    background: rgba(0, 0, 0, 0.3);
    padding: 1.5rem;
    border-radius: 15px;
    border: 2px solid var(--neon-pink);
    text-align: center;
    transition: all 0.3s;
  }
  
  .achievement-card:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 40px rgba(255, 0, 255, 0.4);
  }
  
  .achievement-icon {
    font-size: 3rem;
    margin-bottom: 1rem;
  }
  
  .achievement-title {
    color: var(--neon-pink);
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  .achievement-desc {
    color: #888;
    font-size: 0.9rem;
  }
  
  .interests-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }
  
  .interest-tag {
    background: linear-gradient(135deg, rgba(0, 212, 255, 0.2), rgba(0, 255, 136, 0.2));
    border: 2px solid var(--neon-cyan);
    padding: 0.8rem 1.5rem;
    border-radius: 25px;
    color: var(--neon-cyan);
    font-weight: bold;
    transition: all 0.3s;
  }
  
  .interest-tag:hover {
    background: var(--neon-cyan);
    color: var(--dark-bg);
    transform: scale(1.1);
    box-shadow: 0 0 30px var(--neon-cyan);
  }
  
  .cta-section {
    text-align: center;
    padding: 3rem;
    background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(0, 255, 136, 0.1));
    border-radius: 20px;
    border: 2px solid var(--neon-green);
    margin-top: 3rem;
  }
  
  .cta-title {
    font-size: 2.5rem;
    background: linear-gradient(135deg, var(--neon-cyan), var(--neon-green));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 1rem;
  }
  
  .cta-buttons {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    flex-wrap: wrap;
    margin-top: 2rem;
  }
  
  .cta-btn {
    padding: 1rem 2.5rem;
    border: 2px solid var(--neon-cyan);
    background: transparent;
    color: var(--neon-cyan);
    text-decoration: none;
    border-radius: 10px;
    font-weight: bold;
    font-size: 1.1rem;
    transition: all 0.3s;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }
  
  .cta-btn:hover {
    background: var(--neon-cyan);
    color: var(--dark-bg);
    transform: translateY(-5px);
    box-shadow: 0 10px 40px rgba(0, 212, 255, 0.5);
  }
  
  @media (max-width: 768px) {
    .profile-header {
      grid-template-columns: 1fr;
      text-align: center;
      gap: 2rem;
    }
    
    .profile-image-container {
      margin: 0 auto;
    }
    
    .profile-name {
      font-size: 2.5rem;
    }
    
    .quick-info {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="about-container">
  
  <div class="profile-header">
    <div class="profile-image-container">
      <img src="assets/images/profile.jpg" alt="Hanane" class="profile-image">
    </div>
    
    <div class="profile-info">
      <h1 class="profile-name">Hanane</h1>
      <h2 class="profile-role">Cybersecurity Student & Ethical Hacker</h2>
      <p class="profile-tagline">
        "Passionnée par la sécurité informatique, le pentesting et la protection des systèmes. 
        Toujours en quête d'apprendre et de relever de nouveaux défis en cybersécurité."
      </p>
      
      <div class="quick-info">
        <div class="info-item">
          <span class="info-icon">📍</span>
          <div>
            <div class="info-label">Localisation</div>
            <div class="info-value">Casablanca, Maroc</div>
          </div>
        </div>
        
        <div class="info-item">
          <span class="info-icon">🎓</span>
          <div>
            <div class="info-label">Niveau d'études</div>
            <div class="info-value">Master Cybersécurité</div>
          </div>
        </div>
        
        <div class="info-item">
          <span class="info-icon">💼</span>
          <div>
            <div class="info-label">Statut</div>
            <div class="info-value">Étudiante / Stagiaire</div>
          </div>
        </div>
        
        <div class="info-item">
          <span class="info-icon">🌐</span>
          <div>
            <div class="info-label">Langues</div>
            <div class="info-value">Français, Arabe, Anglais</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Section Formation -->
  <div class="section">
    <h2 class="section-title">
      <span class="section-icon">🎓</span>
      Formation Académique
    </h2>
    
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-date">2023 - 2025</div>
        <div class="timeline-title">Master en Cybersécurité</div>
        <div class="timeline-org">École Supérieure de Technologie</div>
        <div class="timeline-desc">
          Spécialisation en sécurité des systèmes d'information, pentesting, cryptographie avancée et forensics numérique.
        </div>
      </div>
      
      <div class="timeline-item">
        <div class="timeline-date">2020 - 2023</div>
        <div class="timeline-title">Licence en Informatique</div>
        <div class="timeline-org">Faculté des Sciences</div>
        <div class="timeline-desc">
          Formation en développement logiciel, réseaux, bases de données et introduction à la cybersécurité.
        </div>
      </div>
      
      <div class="timeline-item">
        <div class="timeline-date">2019 - 2020</div>
        <div class="timeline-title">Baccalauréat Sciences Mathématiques</div>
        <div class="timeline-org">Lycée Mohammed V</div>
        <div class="timeline-desc">
          Mention Très Bien - Option Informatique
        </div>
      </div>
    </div>
  </div>

  <!-- Section Expérience -->
  <div class="section">
    <h2 class="section-title">
      <span class="section-icon">💼</span>
      Expérience Professionnelle
    </h2>
    
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-date">Été 2024 (3 mois)</div>
        <div class="timeline-title">Stagiaire Pentester</div>
        <div class="timeline-org">SecureTech Solutions</div>
        <div class="timeline-desc">
          • Réalisation de tests d'intrusion sur applications web et infrastructures réseau<br>
          • Rédaction de rapports de vulnérabilités et recommandations de sécurité<br>
          • Participation à des audits de sécurité pour clients bancaires<br>
          • Utilisation de Burp Suite, Metasploit, Nmap, Wireshark
        </div>
      </div>
      
      <div class="timeline-item">
        <div class="timeline-date">Été 2023 (2 mois)</div>
        <div class="timeline-title">Stagiaire Développeuse Web</div>
        <div class="timeline-org">Digital Agency Morocco</div>
        <div class="timeline-desc">
          • Développement d'applications web sécurisées (React, Node.js)<br>
          • Implémentation de bonnes pratiques OWASP<br>
          • Tests de sécurité et correction de vulnérabilités
        </div>
      </div>
    </div>
  </div>

  <!-- Section Compétences -->
  <div class="section">
    <h2 class="section-title">
      <span class="section-icon">💻</span>
      Compétences Techniques
    </h2>
    
    <div class="skills-grid">
      <div class="skill-category">
        <div class="skill-category-title">🔐 Sécurité Offensive</div>
        <ul class="skill-list">
          <li>Pentesting Web & Network</li>
          <li>Exploitation de vulnérabilités</li>
          <li>Metasploit, Burp Suite</li>
          <li>Social Engineering</li>
        </ul>
      </div>
      
      <div class="skill-category">
        <div class="skill-category-title">🛡️ Sécurité Défensive</div>
        <ul class="skill-list">
          <li>IDS/IPS (Snort, Suricata)</li>
          <li>Firewalls & WAF</li>
          <li>SIEM & Log Analysis</li>
          <li>Incident Response</li>
        </ul>
      </div>
      
      <div class="skill-category">
        <div class="skill-category-title">💻 Programmation</div>
        <ul class="skill-list">
          <li>Python (Scripts sécu)</li>
          <li>Bash Scripting</li>
          <li>JavaScript/Node.js</li>
          <li>C/C++ (Exploits)</li>
        </ul>
      </div>
      
      <div class="skill-category">
        <div class="skill-category-title">🌐 Technologies Web</div>
        <ul class="skill-list">
          <li>OWASP Top 10</li>
          <li>SQL Injection</li>
          <li>XSS, CSRF, XXE</li>
          <li>API Security</li>
        </ul>
      </div>
      
      <div class="skill-category">
        <div class="skill-category-title">🐧 Systèmes</div>
        <ul class="skill-list">
          <li>Linux (Kali, Parrot)</li>
          <li>Windows Server</li>
          <li>Active Directory</li>
          <li>Virtualisation</li>
        </ul>
      </div>
      
      <div class="skill-category">
        <div class="skill-category-title">🔍 Forensics & Reverse</div>
        <ul class="skill-list">
          <li>Wireshark, tcpdump</li>
          <li>Ghidra, IDA Pro</li>
          <li>Malware Analysis</li>
          <li>Memory Forensics</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- Section Certifications -->
  <div class="section">
    <h2 class="section-title">
      <span class="section-icon">🏆</span>
      Certifications & Achievements
    </h2>
    
    <div class="achievement-grid">
      <div class="achievement-card">
        <div class="achievement-icon">✅</div>
        <div class="achievement-title">eJPT</div>
        <div class="achievement-desc">Junior Penetration Tester</div>
      </div>
      
      <div class="achievement-card">
        <div class="achievement-icon">📖</div>
        <div class="achievement-title">CEH</div>
        <div class="achievement-desc">En cours de préparation</div>
      </div>
      
      <div class="achievement-card">
        <div class="achievement-icon">🎯</div>
        <div class="achievement-title">OWASP</div>
        <div class="achievement-desc">Top 10 Expert</div>
      </div>
      
      <div class="achievement-card">
        <div class="achievement-icon">🚩</div>
        <div class="achievement-title">50+ CTFs</div>
        <div class="achievement-desc">HackTheBox, THM</div>
      </div>
      
      <div class="achievement-card">
        <div class="achievement-icon">⭐</div>
        <div class="achievement-title">Top 10%</div>
        <div class="achievement-desc">TryHackMe Ranking</div>
      </div>
      
      <div class="achievement-card">
        <div class="achievement-icon">💻</div>
        <div class="achievement-title">15+ Projects</div>
        <div class="achievement-desc">GitHub Open Source</div>
      </div>
    </div>
  </div>

  <!-- Section Intérêts -->
  <div class="section">
    <h2 class="section-title">
      <span class="section-icon">💡</span>
      Centres d'Intérêt
    </h2>
    
    <div class="interests-container">
      <div class="interest-tag">🔓 Bug Bounty Hunting</div>
      <div class="interest-tag">🚩 CTF Competitions</div>
      <div class="interest-tag">🤖 Intelligence Artificielle & Sécu</div>
      <div class="interest-tag">📚 Veille Technologique</div>
      <div class="interest-tag">🎮 Gaming & E-sports</div>
      <div class="interest-tag">✍️ Technical Writing</div>
      <div class="interest-tag">🎨 Design & UI/UX</div>
      <div class="interest-tag">🌍 Open Source Contribution</div>
    </div>
  </div>

  <!-- Call to Action -->
  <div class="cta-section">
    <h2 class="cta-title">Travaillons Ensemble !</h2>
    <p style="color: #bbb; font-size: 1.2rem; max-width: 800px; margin: 0 auto;">
      Je suis actuellement à la recherche de stages et opportunités en cybersécurité. 
      N'hésitez pas à me contacter pour discuter de projets, collaborations ou simplement échanger sur la sécu !
    </p>
    
    <div class="cta-buttons">
      <a href="mailto:your.email@example.com" class="cta-btn">
        📧 Me Contacter
      </a>
      <a href="assets/cv.pdf" class="cta-btn" download>
        📄 Télécharger CV
      </a>
      <a href="https://github.com/ItsHanane" class="cta-btn">
        ⚡ Voir GitHub
      </a>
      <a href="https://linkedin.com/in/yourprofile" class="cta-btn">
        💼 LinkedIn
      </a>
    </div>
  </div>

</div>
