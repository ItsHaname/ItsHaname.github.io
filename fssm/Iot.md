---
layout: default
title: Chapitre 1 - Fondamentaux IoT
---

<style>
.course-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 20px;
}

.course-header {
  text-align: center;
  margin-bottom: 50px;
  padding: 40px 20px;
  background: rgba(0, 20, 40, 0.6);
  border-radius: 20px;
  border: 2px solid #1e4d7b;
  box-shadow: 0 0 30px rgba(30, 77, 123, 0.3);
}

.course-title {
  font-size: 2.5em;
  color: transparent;
  background: linear-gradient(90deg, #3b82f6, #60a5fa, #2563eb);
  background-size: 200% auto;
  -webkit-background-clip: text;
  background-clip: text;
  animation: gradientBG 3s ease infinite;
  margin-bottom: 10px;
  font-weight: 900;
}

.course-subtitle {
  color: #94a3b8;
  font-size: 1.1em;
  font-style: italic;
}

.section-card {
  background: rgba(15, 23, 42, 0.85);
  border: 1px solid rgba(59, 130, 246, 0.3);
  border-radius: 15px;
  padding: 30px;
  margin-bottom: 30px;
}

.section-card h2 {
  color: #3b82f6;
  font-size: 1.8em;
  margin-bottom: 20px;
  border-bottom: 2px solid rgba(59, 130, 246, 0.3);
  padding-bottom: 10px;
}

.section-card h3 {
  color: #60a5fa;
  font-size: 1.4em;
  margin: 20px 0 15px 0;
}

.section-card h4 {
  color: #93c5fd;
  font-size: 1.2em;
  margin: 15px 0 10px 0;
}

.section-card p {
  color: #cbd5e1;
  line-height: 1.8;
  margin-bottom: 15px;
}

.section-card ul, .section-card ol {
  color: #cbd5e1;
  margin-left: 30px;
  margin-bottom: 15px;
}

.section-card li {
  margin-bottom: 8px;
  line-height: 1.6;
}

.highlight-box {
  background: rgba(59, 130, 246, 0.1);
  border-left: 4px solid #3b82f6;
  padding: 20px;
  margin: 20px 0;
  border-radius: 8px;
}

.highlight-box strong {
  color: #60a5fa;
}

.example-box {
  background: rgba(30, 77, 123, 0.2);
  border: 1px solid #1e4d7b;
  padding: 20px;
  margin: 20px 0;
  border-radius: 10px;
}

.example-box h4 {
  color: #60a5fa;
  margin-bottom: 10px;
}

.comparison-table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
  background: rgba(15, 23, 42, 0.5);
}

.comparison-table th {
  background: rgba(59, 130, 246, 0.2);
  color: #60a5fa;
  padding: 15px;
  text-align: left;
  font-weight: 600;
}

.comparison-table td {
  padding: 15px;
  border-bottom: 1px solid rgba(59, 130, 246, 0.2);
  color: #cbd5e1;
}

.code-diagram {
  background: #0f172a;
  border: 1px solid #1e40af;
  border-radius: 8px;
  padding: 20px;
  margin: 20px 0;
  font-family: 'Courier New', monospace;
  color: #60a5fa;
  overflow-x: auto;
}

.key-points {
  background: rgba(59, 130, 246, 0.1);
  border-radius: 10px;
  padding: 25px;
  margin: 30px 0;
}

.key-points h3 {
  color: #3b82f6;
  margin-bottom: 15px;
}

.key-points ul {
  list-style: none;
  margin-left: 0;
}

.key-points li:before {
  content: "✓ ";
  color: #3b82f6;
  font-weight: bold;
  margin-right: 10px;
}

.nav-buttons {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
  gap: 20px;
  flex-wrap: wrap;
}

.nav-button {
  display: inline-block;
  padding: 15px 30px;
  background: rgba(59, 130, 246, 0.2);
  border: 1px solid #3b82f6;
  border-radius: 10px;
  color: #60a5fa;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s;
}

.nav-button:hover {
  background: #3b82f6;
  color: white;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(59, 130, 246, 0.4);
}

@media (max-width: 768px) {
  .course-title {
    font-size: 1.8em;
  }
  
  .section-card {
    padding: 20px;
  }
}
</style>

<div class="course-container">

<div class="course-header">
  <h1 class="course-title">Chapitre 1 : Fondamentaux de l'IoT</h1>
  <p class="course-subtitle">Module : IoT Analyse et Connexion | Durée : 2-3 heures</p>
</div>

<div class="section-card">
  <h2>Qu'est-ce que l'IoT ?</h2>
  
  <div class="highlight-box">
    <p><strong>L'Internet des Objets (IoT)</strong> est un réseau d'objets physiques connectés à Internet qui peuvent collecter et échanger des données automatiquement.</p>
  </div>
  
  <p><strong>Exemple simple :</strong> Ta montre connectée qui envoie tes données de santé à ton téléphone, ou ton thermostat intelligent qui ajuste la température tout seul.</p>
</div>

<div class="section-card">
  <h2>Architecture IoT : Les 4 Couches</h2>
  
  <h3>1. Couche Perception (Les Capteurs)</h3>
  
  <div class="example-box">
    <h4>📡 Les Capteurs collectent les données :</h4>
    <ul>
      <li>Température (DHT11, DHT22)</li>
      <li>Mouvement (PIR)</li>
      <li>Humidité</li>
      <li>Lumière</li>
      <li>GPS</li>
    </ul>
    
    <h4>⚙️ Les Actuateurs agissent sur l'environnement :</h4>
    <ul>
      <li>Moteurs</li>
      <li>Relais (allumer/éteindre)</li>
      <li>Valves</li>
      <li>LEDs</li>
    </ul>
  </div>

  <h3>2. Couche Réseau (La Passerelle)</h3>
  <p><strong>La Passerelle (Gateway)</strong> connecte les capteurs à Internet :</p>
  <ul>
    <li>Traduit les protocoles</li>
    <li>Filtre les données</li>
    <li>Sécurise la communication</li>
  </ul>
  <p><strong>Exemple :</strong> Un hub qui connecte tes ampoules Zigbee à ton WiFi.</p>

  <h3>3. Couche Traitement</h3>
  <p><strong>Edge Computing :</strong> Traitement rapide près des capteurs</p>
  <p><strong>Cloud Computing :</strong> Stockage massif et analyse (AWS, Azure, Google Cloud)</p>

  <h3>4. Couche Application</h3>
  <p><strong>Interface utilisateur :</strong></p>
  <ul>
    <li>Applications mobiles</li>
    <li>Dashboards web</li>
    <li>Systèmes de contrôle</li>
  </ul>
</div>

<div class="section-card">
  <h2>IoT vs IIoT vs IoE</h2>
  
  <table class="comparison-table">
    <tr>
      <th>Type</th>
      <th>Usage</th>
      <th>Exemple</th>
      <th>Priorité</th>
    </tr>
    <tr>
      <td><strong>IoT</strong></td>
      <td>Grand public</td>
      <td>Montre connectée, Smart home</td>
      <td>Confort</td>
    </tr>
    <tr>
      <td><strong>IIoT</strong></td>
      <td>Industrie</td>
      <td>Machines d'usine, Maintenance prédictive</td>
      <td>Fiabilité</td>
    </tr>
    <tr>
      <td><strong>IoE</strong></td>
      <td>Tout connecté</td>
      <td>Smart city complète</td>
      <td>Écosystème global</td>
    </tr>
  </table>
  
  <div class="highlight-box">
    <p><strong>Résumé :</strong></p>
    <ul>
      <li><strong>IoT</strong> = Objets du quotidien connectés</li>
      <li><strong>IIoT</strong> = IoT industriel (plus robuste)</li>
      <li><strong>IoE</strong> = Objets + Humains + Processus</li>
    </ul>
  </div>
</div>

<div class="section-card">
  <h2>Cas d'Usage</h2>
  
  <div class="example-box">
    <h3>🏡 Smart Home</h3>
    <ul>
      <li>Serrure connectée</li>
      <li>Thermostat intelligent (Nest)</li>
      <li>Lumières automatiques (Philips Hue)</li>
      <li>Assistants vocaux (Alexa, Google Home)</li>
    </ul>
  </div>

  <div class="example-box">
    <h3>🏙️ Smart City</h3>
    <ul>
      <li>Éclairage public intelligent</li>
      <li>Gestion du trafic en temps réel</li>
      <li>Poubelles connectées</li>
      <li>Parking intelligent</li>
      <li>Capteurs de qualité d'air</li>
    </ul>
  </div>

  <div class="example-box">
    <h3>🏭 Industrie 4.0</h3>
    <ul>
      <li>Maintenance prédictive</li>
      <li>Optimisation de production</li>
      <li>Suivi en temps réel</li>
      <li>Économie d'énergie</li>
    </ul>
  </div>

  <div class="example-box">
    <h3>🏥 Santé Connectée</h3>
    <ul>
      <li>Pacemakers connectés</li>
      <li>Glucomètres pour diabétiques</li>
      <li>Montres détectant arythmies</li>
      <li>Télémédecine</li>
    </ul>
  </div>
</div>

<div class="section-card">
  <h2>Écosystème IoT</h2>
  
  <h3>Hardware</h3>
  <ul>
    <li><strong>Arduino</strong> - Plateforme éducative</li>
    <li><strong>Raspberry Pi</strong> - Mini-ordinateur</li>
    <li><strong>ESP32/ESP8266</strong> - WiFi intégré</li>
  </ul>

  <h3>Plateformes Cloud</h3>
  <ul>
    <li><strong>AWS IoT Core</strong> - Amazon</li>
    <li><strong>Azure IoT Hub</strong> - Microsoft</li>
    <li><strong>Google Cloud IoT</strong> - Google</li>
  </ul>

  <h3>Protocoles</h3>
  <ul>
    <li><strong>MQTT</strong> - Messagerie légère</li>
    <li><strong>CoAP</strong> - HTTP pour IoT</li>
    <li><strong>LoRaWAN</strong> - Longue portée</li>
  </ul>

  <h3>Entreprises</h3>
  <ul>
    <li>Google (Nest)</li>
    <li>Amazon (Alexa)</li>
    <li>Apple (HomeKit)</li>
    <li>Samsung (SmartThings)</li>
  </ul>
</div>

<div class="section-card">
  <h2>Schéma Simple</h2>
  <div class="code-diagram">
Capteur → Passerelle → Internet → Cloud → Application → Actuateur
  ↓         ↓           ↓         ↓          ↓           ↓
Collecte  Traduit   Transmet  Analyse  Visualise    Agit
  </div>
</div>

<div class="key-points">
  <h3>Points Clés à Retenir</h3>
  <ul>
    <li><strong>IoT = Capteurs + Connectivité + Intelligence</strong></li>
    <li><strong>4 couches :</strong> Perception → Réseau → Traitement → Application</li>
    <li><strong>Capteurs</strong> perçoivent, <strong>Actuateurs</strong> agissent</li>
    <li><strong>Passerelles</strong> font le pont entre objets et Internet</li>
    <li><strong>IIoT</strong> est l'IoT pour l'industrie (plus sécurisé)</li>
  </ul>
</div>

<div class="section-card">
  <h2>💡 Exercice Pratique</h2>
  <p><strong>Identifie dans ta maison :</strong></p>
  <ol>
    <li>3 objets IoT que tu utilises</li>
    <li>Quels capteurs ils utilisent</li>
    <li>Comment ils sont connectés (WiFi, Bluetooth, etc.)</li>
  </ol>
</div>

<div class="nav-buttons">
  <a href="{{ site.baseurl }}/fssm" class="nav-button">← Retour FSSM</a>
  <a href="{{ site.baseurl }}/fssm/iot-chapitre2" class="nav-button">Chapitre 2 : Protocoles →</a>
</div>

</div>
