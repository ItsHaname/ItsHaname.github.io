---
layout: default
title: About
nav: about
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

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

@keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.05); }
}

@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: #0a0e1a;
    min-height: 100vh;
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    color: #e2e8f0;
    overflow-x: hidden;
}

.binary-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
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

.about-container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 60px 30px;
    position: relative;
    z-index: 1;
}

.about-header {
    text-align: center;
    margin-bottom: 80px;
    animation: fadeIn 1s ease-out;
}

.about-header h1 {
    font-size: 3.5em;
    background: linear-gradient(90deg, #60a5fa, #3b82f6, #2563eb);
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: gradientShift 3s ease infinite;
    margin-bottom: 15px;
    font-weight: 700;
    letter-spacing: 3px;
}

.about-tagline {
    font-size: 1.3em;
    color: #94a3b8;
    font-weight: 300;
}

.about-tagline::after {
    content: '_';
    animation: blink 1s infinite;
    color: #60a5fa;
}

.divider {
    width: 180px;
    height: 2px;
    background: linear-gradient(90deg, transparent, #3b82f6, #60a5fa, #3b82f6, transparent);
    margin: 30px auto;
}

.profile-section {
    display: flex;
    flex-direction: column;
    gap: 40px;
    margin-bottom: 60px;
    animation: fadeIn 1.2s ease-out;
}

.profile-image-container {
    display: flex;
    justify-content: center;
    width: 100%;
}

.profile-image {
    width: 320px;
    height: 320px;
    border-radius: 50%;
    overflow: hidden;
    background: #1e293b;
    transition: all 0.4s ease;
    box-shadow: 0 10px 40px rgba(59, 130, 246, 0.3);
}

.profile-image:hover {
    transform: scale(1.05);
    box-shadow: 0 15px 50px rgba(59, 130, 246, 0.5);
}

.profile-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.quick-info {
    background: rgba(15, 23, 42, 0.85);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 15px;
    padding: 35px;
    text-align: center;
    transition: all 0.3s ease;
    width: 100%;
}

.quick-info:hover {
    border-color: #3b82f6;
    box-shadow: 0 8px 30px rgba(59, 130, 246, 0.35);
}

.quick-info h3 {
    color: #3b82f6;
    font-size: 1.6em;
    margin-bottom: 25px;
    font-weight: 600;
    border-bottom: 2px solid #3b82f6;
    padding-bottom: 15px;
}

.info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    text-align: left;
}

.info-item {
    color: #cbd5e1;
    font-size: 1.05em;
    line-height: 1.8;
    padding: 15px;
    background: rgba(30, 41, 59, 0.5);
    border-radius: 8px;
    border-left: 3px solid #3b82f6;
}

.info-item strong {
    color: #60a5fa;
    display: block;
    margin-bottom: 5px;
}

.about-section {
    background: rgba(15, 23, 42, 0.85);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 20px;
    padding: 50px;
    margin-bottom: 50px;
    animation: fadeIn 1.4s ease-out;
}

.about-section h2 {
    color: #3b82f6;
    font-size: 2.4em;
    margin-bottom: 30px;
    font-weight: 700;
    position: relative;
    display: inline-block;
}

.about-section h2:after {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 0;
    width: 60%;
    height: 3px;
    background: linear-gradient(90deg, #3b82f6, #60a5fa);
}

.about-section p {
    color: #cbd5e1;
    line-height: 2;
    margin-bottom: 20px;
    font-size: 1.15em;
}

.highlight {
    color: #60a5fa;
    font-weight: 600;
}

.section-title {
    color: #3b82f6;
    font-size: 2.2em;
    margin: 70px 0 40px 0;
    font-weight: 700;
    text-align: center;
    letter-spacing: 1px;
}

.focus-areas {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 30px;
    margin-bottom: 60px;
}

.focus-card {
    background: rgba(15, 23, 42, 0.85);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 15px;
    padding: 35px;
    transition: all 0.3s ease;
    animation: fadeIn 1.4s ease-out;
}

.focus-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(59, 130, 246, 0.4);
    border-color: #3b82f6;
}

.focus-card h3 {
    color: #60a5fa;
    font-size: 1.4em;
    margin-bottom: 20px;
    font-weight: 600;
}

.focus-card ul {
    list-style: none;
    padding: 0;
}

.focus-card li {
    color: #cbd5e1;
    margin-bottom: 12px;
    padding-left: 25px;
    position: relative;
    line-height: 1.7;
    font-size: 1.05em;
}

.focus-card li:before {
    content: "→";
    position: absolute;
    left: 0;
    color: #3b82f6;
    font-weight: bold;
}

.newsletter-section {
    background: rgba(15, 23, 42, 0.85);
    border: 1px solid rgba(59, 130, 246, 0.3);
    border-radius: 20px;
    padding: 50px;
    margin: 60px 0;
    text-align: center;
    animation: fadeIn 1.6s ease-out;
}

.newsletter-section h3 {
    color: #3b82f6;
    font-size: 2em;
    margin-bottom: 20px;
    font-weight: 700;
}

.newsletter-section p {
    color: #cbd5e1;
    font-size: 1.2em;
    margin-bottom: 30px;
    line-height: 1.7;
}

.subscribe-form {
    display: flex;
    gap: 15px;
    max-width: 600px;
    margin: 0 auto;
    flex-wrap: wrap;
    justify-content: center;
}

.subscribe-form input {
    flex: 1;
    min-width: 300px;
    padding: 18px 25px;
    border: 1px solid rgba(59, 130, 246, 0.4);
    border-radius: 8px;
    font-size: 1.05em;
    background: rgba(10, 14, 26, 0.8);
    color: #e2e8f0;
    transition: all 0.3s ease;
}

.subscribe-form input:focus {
    outline: none;
    border-color: #3b82f6;
    box-shadow: 0 0 15px rgba(59, 130, 246, 0.3);
}

.subscribe-form button {
    padding: 18px 40px;
    background: linear-gradient(135deg, #3b82f6, #60a5fa);
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1.05em;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
}

.subscribe-form button:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(59, 130, 246, 0.5);
}

.subscribe-form button:disabled {
    opacity: 0.6;
    cursor: not-allowed;
}

.subscribe-message {
    margin-top: 20px;
    padding: 15px;
    border-radius: 8px;
    display: none;
    font-size: 1.05em;
}

.subscribe-message.success {
    background: rgba(76, 175, 80, 0.1);
    border: 1px solid rgba(76, 175, 80, 0.3);
    color: #4caf50;
}

.subscribe-message.error {
    background: rgba(244, 67, 54, 0.1);
    border: 1px solid rgba(244, 67, 54, 0.3);
    color: #f44336;
}

.social-links {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
    margin: 60px 0;
}

.social-btn {
    padding: 15px 35px;
    background: rgba(59, 130, 246, 0.15);
    border: 1px solid #3b82f6;
    color: #60a5fa;
    text-decoration: none;
    border-radius: 8px;
    font-weight: 600;
    font-size: 1.05em;
    transition: all 0.3s ease;
    display: inline-block;
}

.social-btn:hover {
    background: linear-gradient(135deg, #3b82f6, #60a5fa);
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(59, 130, 246, 0.5);
}

.about-footer {
    text-align: center;
    margin-top: 80px;
    padding-top: 30px;
    border-top: 1px solid rgba(59, 130, 246, 0.3);
    color: #94a3b8;
    font-size: 1em;
    line-height: 1.8;
}

.email-info-box {
    background: rgba(30, 41, 59, 0.7);
    border: 1px solid rgba(59, 130, 246, 0.4);
    border-radius: 10px;
    padding: 20px;
    margin-top: 20px;
    text-align: left;
}

.email-info-box h4 {
    color: #60a5fa;
    margin-bottom: 10px;
    font-size: 1.1em;
}

.email-info-box p {
    color: #cbd5e1;
    font-size: 0.95em;
    line-height: 1.6;
    margin-bottom: 8px;
}

.email-info-box code {
    background: rgba(59, 130, 246, 0.1);
    padding: 2px 6px;
    border-radius: 3px;
    color: #60a5fa;
    font-family: 'Courier New', monospace;
}

@media (max-width: 768px) {
    .about-header h1 {
        font-size: 2.2em;
    }

    .profile-image {
        width: 250px;
        height: 250px;
    }

    .focus-areas {
        grid-template-columns: 1fr;
    }

    .subscribe-form {
        flex-direction: column;
    }

    .subscribe-form input {
        min-width: 100%;
    }

    .about-section {
        padding: 30px;
    }

    .info-grid {
        grid-template-columns: 1fr;
    }
}
</style>

<div class="binary-background" id="binaryBg"></div>

<div class="about-container">
    <div class="about-header">
        <h1>HANANE AIT BAH</h1>
        <div class="divider"></div>
        <p class="about-tagline">Network Security Student | Cybersecurity Enthusiast | NSC @ FSSM</p>
    </div>

  <div class="profile-section">
        <div class="profile-image-container">
            <div class="profile-image">
                <img src="https://github.com/user-attachments/assets/6c553521-15b0-4d1a-aa6f-798d79f1c896" alt="Hanane AIT BAH">
            </div>
        </div>
        
  <div class="quick-info">
            <h3>Contact Information</h3>
            <div class="info-grid">
                <div class="info-item">
                    <strong>Location</strong>
                    Marrakech, Morocco
                </div>
                <div class="info-item">
                    <strong>Institution</strong>
                    FSSM, Cadi Ayyad University
                </div>
                <div class="info-item">
                    <strong>Program</strong>
                    Bachelor's in Networking & Cybersecurity
                </div>
                <div class="info-item">
                    <strong>Blog Launch</strong>
                    January 1, 2026
                </div>
            </div>
        </div>
    </div>

  <div class="about-section">
        <h2>Welcome to Cyberia</h2>
        <p>My name is <span class="highlight">Hanane (Haname)</span>, a cybersecurity student at the Faculty of Sciences Semlalia (FSSM), Cadi Ayyad University. I am currently pursuing a Bachelor's degree in Networking and Cybersecurity after completing foundational studies in Computer Science.</p>
            <p>On January 1st, 2026, I launched this blog to document my journey as an <span class="highlight">NSC (Network Security)</span> student. My goal is to share my notes, projects, and reflections related to cybersecurity, network defense, and my academic path.</p>
        
   <p>I am passionate about <span class="highlight">offensive security</span>, <span class="highlight">vulnerability analysis</span>, and <span class="highlight">reverse engineering</span>. This blog serves both as a personal learning journal and as a resource for others interested in the field.</p>
    </div>

   <h2 class="section-title">What You'll Find Here</h2>
    
 <div class="focus-areas">
        <div class="focus-card">
            <h3>My Academic Journey at FSSM</h3>
            <ul>
                <li>Course notes and study materials</li>
                <li>Academic projects and assignments</li>
                <li>Key concepts in network security</li>
                <li>University learning experiences</li>
            </ul>
        </div>

 <div class="focus-card">
            <h3>My TryHackMe Paths</h3>
            <ul>
                <li>Completed rooms and challenges</li>
                <li>Detailed write-ups and solutions</li>
                <li>Badges and achievements</li>
                <li>Skills development tracking</li>
            </ul>
        </div>

<div class="focus-card">
            <h3>My Personal Lab</h3>
            <ul>
                <li>Virtual machine configurations</li>
                <li>Network topologies and setups</li>
                <li>Practical experiments and tests</li>
                <li>Technical documentation</li>
            </ul>
        </div>

  <div class="focus-card">
            <h3>Resources & Learning Notes</h3>
            <ul>
                <li>Curated study materials</li>
                <li>Tools and software reviews</li>
                <li>Security best practices</li>
                <li>Community recommendations</li>
            </ul>
        </div>
    </div>

  <div class="about-footer">
        <p>&copy; 2026 Hanane AIT BAH - Network Security Student @ FSSM</p>
        <p>Cyberia: A Personal Cybersecurity Learning Journey</p>
    </div>
</div>

