<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anonymity & Privacy Lab</title>
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

   @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

   @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

   @keyframes glow {
            0%, 100% { text-shadow: 0 0 10px #9333ea, 0 0 20px #9333ea, 0 0 30px #9333ea; }
            50% { text-shadow: 0 0 20px #9333ea, 0 0 30px #9333ea, 0 0 40px #7c3aed, 0 0 50px #7c3aed; }
        }

  * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

 body {
            background: #0a0e1a;
            min-height: 100vh;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            color: #e2e8f0;
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
            color: rgba(147, 51, 234, 0.15);
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

  .page-header {
            text-align: center;
            margin-bottom: 60px;
            padding: 50px 20px;
            background: rgba(20, 0, 40, 0.6);
            border-radius: 30px;
            border: 3px solid #7c3aed;
            box-shadow: 0 0 40px rgba(124, 58, 237, 0.5), inset 0 0 30px rgba(124, 58, 237, 0.2);
            position: relative;
            overflow: hidden;
        }

  .onion-logo {
            width: 200px;
            height: 200px;
            margin: 0 auto 30px;
            animation: floatUpDown 4s ease-in-out infinite;
            filter: drop-shadow(0 0 25px rgba(147, 51, 234, 0.6));
        }

  .onion-logo img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

   .page-title {
            font-size: 3.5em;
            color: #a855f7;
            text-shadow: 
                0 0 10px #a855f7,
                0 0 20px #a855f7,
                0 0 30px #9333ea,
                0 0 40px #9333ea;
            margin: 0 0 20px 0;
            font-weight: 900;
            letter-spacing: 8px;
            text-transform: uppercase;
            font-style: italic;
            -webkit-text-stroke: 2px #7c3aed;
            animation: glow 3s ease-in-out infinite;
        }

   .page-subtitle {
            font-size: 1.5em;
            color: #c4b5fd;
            margin: 10px 0 0 0;
            text-shadow: 0 0 10px #c4b5fd, 0 0 20px #a855f7;
            letter-spacing: 3px;
            font-style: italic;
        }

   .page-subtitle::after {
            content: '_';
            animation: blink 1s infinite;
            color: #c4b5fd;
        }

   .hero-section {
            background: linear-gradient(135deg, rgba(30, 10, 50, 0.9), rgba(20, 0, 40, 0.8));
            border: 2px solid rgba(147, 51, 234, 0.3);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 50px;
            text-align: center;
        }

  .hero-section h2 {
            color: transparent;
            background: linear-gradient(90deg, #9333ea, #a855f7, #7c3aed);
            background-size: 200% auto;
            -webkit-background-clip: text;
            background-clip: text;
            animation: gradientBG 3s ease infinite;
            font-size: 2.5em;
            margin: 0 0 20px 0;
            font-weight: 900;
        }

   .hero-section p {
            color: #cbd5e1;
            font-size: 1.2em;
            line-height: 1.8;
            margin: 0;
        }

  .hero-section strong {
            color: #a855f7;
        }

   .warning-box {
            background: rgba(220, 38, 38, 0.1);
            border: 2px solid rgba(220, 38, 38, 0.5);
            border-left: 5px solid #dc2626;
            border-radius: 10px;
            padding: 20px;
            margin: 30px 0;
            text-align: left;
        }

   .warning-box h3 {
            color: #ef4444;
            font-size: 1.5em;
            margin: 0 0 15px 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }

   .warning-box p {
            color: #fca5a5;
            margin: 10px 0;
            line-height: 1.6;
        }

 .warning-box ul {
            list-style: none;
            padding: 0;
            margin: 15px 0 0 0;
        }

   .warning-box li {
            color: #fca5a5;
            padding: 5px 0;
            padding-left: 25px;
            position: relative;
        }

   .warning-box li::before {
            content: "•";
            position: absolute;
            left: 0;
            font-size: 1.5em;
        }

  .prereq-box {
            background: rgba(59, 130, 246, 0.1);
            border: 2px solid rgba(59, 130, 246, 0.3);
            border-left: 5px solid #3b82f6;
            border-radius: 10px;
            padding: 20px;
            margin: 30px 0;
        }

  .prereq-box h3 {
            color: #60a5fa;
            font-size: 1.5em;
            margin: 0 0 15px 0;
        }

  .prereq-box p {
            color: #bfdbfe;
            margin: 10px 0;
            line-height: 1.6;
        }

  .specs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 50px 0;
        }

  .spec-card {
            background: rgba(30, 10, 50, 0.85);
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s;
        }

   .spec-card:hover {
            transform: translateY(-5px);
            border-color: #a855f7;
            box-shadow: 0 10px 25px rgba(147, 51, 234, 0.3);
        }

  .spec-icon {
            font-size: 3em;
            margin-bottom: 15px;
            font-weight: 900;
        }

  .spec-card h3 {
            color: #9333ea;
            font-size: 1.3em;
            margin: 0 0 10px 0;
            font-weight: 600;
        }

   .spec-card p {
            color: #cbd5e1;
            margin: 0;
            line-height: 1.6;
        }

 .section-title {
            font-size: 2.5em;
            color: transparent;
            background: linear-gradient(90deg, #9333ea, #a855f7, #7c3aed);
            background-size: 200% auto;
            -webkit-background-clip: text;
            background-clip: text;
            animation: gradientBG 3s ease infinite;
            margin: 60px 0 30px 0;
            font-weight: 900;
            text-align: center;
        }

   .path-container {
            background: rgba(30, 10, 50, 0.5);
            border: 2px solid rgba(147, 51, 234, 0.3);
            border-radius: 20px;
            padding: 40px;
            margin: 40px 0;
        }

   .path-header {
            text-align: center;
            margin-bottom: 40px;
        }

   .path-header h3 {
            color: #a855f7;
            font-size: 2em;
            margin: 0 0 15px 0;
        }

  .path-header p {
            color: #cbd5e1;
            font-size: 1.1em;
            margin: 0;
        }

   .level-section {
            margin: 40px 0;
        }

 .level-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            padding: 15px;
            background: rgba(147, 51, 234, 0.1);
            border-left: 5px solid #9333ea;
            border-radius: 10px;
        }

  .level-badge {
            font-size: 2em;
            font-weight: 900;
            color: #a855f7;
        }

  .level-info h4 {
            color: #a855f7;
            font-size: 1.8em;
            margin: 0 0 5px 0;
            font-weight: 700;
        }

  .level-meta {
            color: #9ca3af;
            font-size: 0.95em;
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

   .level-meta span {
            display: flex;
            align-items: center;
            gap: 5px;
        }

   .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

   .project-card {
            background: rgba(30, 10, 50, 0.85);
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 15px;
            padding: 30px;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
        }

  .project-card:before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #9333ea, #a855f7, transparent);
            z-index: -1;
            opacity: 0;
            transition: opacity 0.4s;
        }

  .project-card:hover:before {
            opacity: 0.5;
        }

  .project-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: #a855f7;
            box-shadow: 0 15px 35px rgba(147, 51, 234, 0.3);
        }

   .project-number {
            display: inline-block;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #7c3aed, #6d28d9);
            color: white;
            font-size: 1.5em;
            font-weight: 900;
            border-radius: 50%;
            text-align: center;
            line-height: 50px;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(124, 58, 237, 0.4);
        }

 .project-card h3 {
            color: #9333ea;
            font-size: 1.6em;
            margin: 0 0 15px 0;
            font-weight: 600;
        }

  .project-card p {
            color: #cbd5e1;
            line-height: 1.6;
            margin: 0 0 15px 0;
        }

   .project-duration {
            display: inline-block;
            background: rgba(147, 51, 234, 0.15);
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.85em;
            color: #c4b5fd;
            margin-top: 10px;
        }

   .status-badge {
            display: inline-block;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 700;
            margin-top: 10px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

 .status-done {
            background: rgba(34, 197, 94, 0.2);
            color: #4ade80;
            border: 2px solid rgba(34, 197, 94, 0.5);
        }

 .status-done::before {
            content: "✓ ";
            font-size: 1.1em;
        }

   .status-upcoming {
            background: rgba(251, 191, 36, 0.2);
            color: #fbbf24;
            border: 2px solid rgba(251, 191, 36, 0.5);
        }

  .status-upcoming::before {
            content: "⏳ ";
            font-size: 1.1em;
        }

 .info-box {
            background: rgba(147, 51, 234, 0.1);
            border: 2px solid rgba(147, 51, 234, 0.3);
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
        }

  .info-box h3 {
            color: #a855f7;
            font-size: 1.8em;
            margin: 0 0 20px 0;
        }

  .info-box ul {
            list-style: none;
            margin: 0;
            padding: 0;
        }

   .info-box li {
            color: #cbd5e1;
            padding: 10px 0 10px 30px;
            position: relative;
            line-height: 1.6;
        }

  .info-box li:before {
            content: "▸";
            position: absolute;
            left: 0;
            color: #a855f7;
            font-size: 1.2em;
            font-weight: 900;
        }

.timeline {
            background: rgba(30, 10, 50, 0.5);
            border: 2px solid rgba(147, 51, 234, 0.3);
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
        }

  .timeline h3 {
            color: #a855f7;
            font-size: 1.8em;
            margin: 0 0 25px 0;
            text-align: center;
        }

   .timeline-item {
            display: flex;
            gap: 20px;
            margin: 20px 0;
            padding: 15px;
            background: rgba(147, 51, 234, 0.05);
            border-left: 4px solid #9333ea;
            border-radius: 8px;
        }

  .timeline-week {
            font-size: 1.2em;
            font-weight: 700;
            color: #a855f7;
            min-width: 120px;
        }

  .timeline-content {
            flex: 1;
        }

   .timeline-content p {
            color: #cbd5e1;
            margin: 0;
        }

  .footer-nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 60px;
            flex-wrap: wrap;
        }

 .nav-button {
            display: inline-block;
            padding: 15px 30px;
            background: rgba(147, 51, 234, 0.2);
            border: 1px solid #9333ea;
            border-radius: 10px;
            color: #a855f7;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }

   .nav-button:hover {
            background: #9333ea;
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(147, 51, 234, 0.4);
        }

  .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

   .resource-card {
            background: rgba(30, 10, 50, 0.5);
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 12px;
            padding: 20px;
            transition: all 0.3s;
        }

  .resource-card:hover {
            border-color: #a855f7;
            transform: translateY(-3px);
        }

   .resource-card h4 {
            color: #9333ea;
            font-size: 1.3em;
            margin: 0 0 15px 0;
        }

 .resource-card ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

.resource-card li {
            color: #cbd5e1;
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
        }

  .resource-card li::before {
            content: "→";
            position: absolute;
            left: 0;
            color: #a855f7;
        }

 .resource-card a {
            color: #a855f7;
            text-decoration: none;
            transition: color 0.3s;
        }

  .resource-card a:hover {
            color: #c4b5fd;
        }

  @media (max-width: 768px) {
            .page-title {
                font-size: 2.5em;
                letter-spacing: 4px;
            }
            
   .page-subtitle {
                font-size: 1.2em;
                letter-spacing: 2px;
            }
            
  .onion-logo {
                width: 140px;
                height: 140px;
            }
            
   .projects-grid {
                grid-template-columns: 1fr;
            }
            
   .specs-grid {
                grid-template-columns: 1fr;
            }

 .level-meta {
                flex-direction: column;
                gap: 10px;
            }

   .resources-grid {
                grid-template-columns: 1fr;
            }

   .timeline-item {
                flex-direction: column;
                gap: 10px;
            }

  .timeline-week {
                min-width: auto;
            }
        }
    </style>
</head>
<body>
    <div class="binary-background"></div>

   <div class="container">
        <div class="page-header">
            <div class="onion-logo">
                <img src="/assets/images/tor.png" alt="Tor Onion Logo">
            </div>
            <h1 class="page-title">ANONYMITY & PRIVACY</h1>
            <p class="page-subtitle">Master the Dark Web & Anonymous Technologies</p>
        </div>

  <div class="hero-section">
            <h2>What is This Lab About?</h2>
            <p>
                Learn to protect your <strong>privacy</strong> and achieve <strong>true anonymity</strong> online. 
                This comprehensive lab covers <strong>Tor</strong>, <strong>Tails OS</strong>, <strong>Dark Web navigation</strong>, 
                <strong>OPSEC</strong>, and advanced <strong>anti-surveillance techniques</strong>. Master the tools used by 
                journalists, activists, and security researchers worldwide.
            </p>
        </div>

   <div class="warning-box">
            <h3>Legal & Ethical Notice</h3>
            <p><strong>These labs are for EDUCATIONAL and RESEARCH purposes ONLY.</strong></p>
            <p>You are responsible for your actions. This lab teaches privacy technologies, not how to break the law.</p>
            <ul>
                <li>Do NOT access, buy, or sell illegal content</li>
                <li>Do NOT participate in criminal activities</li>
                <li>Do NOT use these tools for unauthorized hacking</li>
                <li>Respect local laws and regulations</li>
            </ul>
        </div>

  <div class="prereq-box">
            <h3>Prerequisites Before Starting</h3>
            <p>Before diving into anonymity labs, make sure you have solid foundations in:</p>
            <p><strong>Networking Fundamentals:</strong> TCP/IP, DNS, HTTP/HTTPS, routing, proxies<br>
            <strong>Linux Basics:</strong> Command line, package management, services, file permissions<br>
            <strong>Cryptography Basics:</strong> Symmetric vs asymmetric encryption, hashing, digital signatures<br>
            <strong>Web Technologies:</strong> How browsers work, cookies, JavaScript, web servers</p>
        </div>

   <div class="specs-grid">
            <div class="spec-card">
                <div class="spec-icon">TOR</div>
                <h3>Tor Network</h3>
                <p>Master onion routing and hidden services (.onion sites)</p>
            </div>
            
  <div class="spec-card">
                <div class="spec-icon">OS</div>
                <h3>Tails OS</h3>
                <p>Amnesic live operating system for maximum privacy</p>
            </div>
            
  <div class="spec-card">
                <div class="spec-icon">ENC</div>
                <h3>Encryption</h3>
                <p>PGP, end-to-end encryption, and secure communications</p>
            </div>
            
   <div class="spec-card">
                <div class="spec-icon">SEC</div>
                <h3>OPSEC</h3>
                <p>Operational security and identity compartmentalization</p>
            </div>
        </div>

   <h2 class="section-title">Learning Path</h2>

<div class="path-container">
            <div class="path-header">
                <h3>Complete Anonymity Mastery Path</h3>
                <p>From beginner to expert in 20 comprehensive labs - 20 to 24 weeks total</p>
            </div>

   <div class="level-section">
                <div class="level-header">
                    <div class="level-badge">L0</div>
                    <div class="level-info">
                        <h4>Level 0: Essential Foundations</h4>
                        <div class="level-meta">
                            <span>Duration: 2-3 weeks</span>
                            <span>3 Labs</span>
                            <span>Difficulty: Beginner</span>
                        </div>
                    </div>
                </div>

   <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-number">0</div>
                        <h3>Networking for Privacy</h3>
                        <p>Deep dive into TCP/IP, DNS, routing, proxies, and VPNs. Understand how internet traffic works and where metadata leaks occur.</p>
                        <div class="status-badge status-done">Done</div>
                        <div class="project-duration">6-8 hours</div>
                    </div>

   <div class="project-card">
                        <div class="project-number">0.1</div>
                        <h3>Cryptography Fundamentals</h3>
                        <p>Learn encryption basics: symmetric/asymmetric, hashing, digital signatures, certificates, TLS/SSL, and perfect forward secrecy.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">5-7 hours</div>
                    </div>

  <div class="project-card">
                        <div class="project-number">0.2</div>
                        <h3>Linux Command Line Mastery</h3>
                        <p>Master essential Linux commands, shell scripting, package management, process control, and system administration basics.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">8-10 hours</div>
                    </div>
                </div>
            </div>

   <div class="level-section">
                <div class="level-header">
                    <div class="level-badge">L1</div>
                    <div class="level-info">
                        <h4>Level 1: Privacy Foundations</h4>
                        <div class="level-meta">
                            <span>Duration: 3-4 weeks</span>
                            <span>4 Labs</span>
                            <span>Difficulty: Easy</span>
                        </div>
                    </div>
                </div>

  <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-number">1</div>
                        <h3>Online Anonymity Basics</h3>
                        <p>Learn the fundamentals: VPN vs Tor vs Proxy, threat modeling, metadata, browser fingerprinting, and tracking techniques.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">4-5 hours</div>
                    </div>

   <div class="project-card">
                        <div class="project-number">2</div>
                        <h3>Privacy-Hardened Browser</h3>
                        <p>Configure Firefox/Brave with privacy extensions, understand fingerprinting, cookies, WebRTC leaks, and browser isolation.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">3-4 hours</div>
                    </div>

   <div class="project-card">
                        <div class="project-number">3</div>
                        <h3>Tor Browser Mastery</h3>
                        <p>Configure Tor Browser, understand circuits and nodes, navigate .onion sites safely, master the three security levels.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">4-5 hours</div>
                    </div>

 <div class="project-card">
                        <div class="project-number">4</div>
                        <h3>Secure Communications</h3>
                        <p>Master Signal, Session, encrypted email (ProtonMail), metadata-resistant messaging, and secure file sharing.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">3-4 hours</div>
                    </div>
                </div>
            </div>

<div class="level-section">
                <div class="level-header">
                    <div class="level-badge">L2</div>
                    <div class="level-info">
                        <h4>Level 2: Intermediate Anonymity</h4>
                        <div class="level-meta">
                            <span>Duration: 4-5 weeks</span>
                            <span>5 Labs</span>
                            <span>Difficulty: Medium</span>
                        </div>
                    </div>
                </div>

   <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-number">5</div>
                        <h3>Tails OS - Live Anonymity</h3>
                        <p>Install Tails OS on USB, understand the amnesic system, explore tools, configure persistence, and daily usage workflows.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">5-6 hours</div>
                    </div>
  <div class="project-card">
                        <div class="project-number">6</div>
                        <h3>PGP/GPG Encryption</h3>
                        <p>Master PGP for email encryption, key generation, key signing, web of trust, encrypted file storage, and key management.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">4-5 hours</div>
                    </div>

  <div class="project-card">
                        <div class="project-number">7</div>
                        <h3>Tor Network Architecture</h3>
                        <p>Deep dive into how Tor works: guard nodes, exit nodes, directory authorities, circuits, and onion routing protocols.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">6-7 hours</div>
                    </div>

<div class="project-card">
                        <div class="project-number">8</div>
                        <h3>OPSEC - Operational Security</h3>
                        <p>Master compartmentalization, create multiple personas, avoid correlation, secure password management, and real OPSEC failures.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">5-6 hours</div>
                    </div>

   <div class="project-card">
                        <div class="project-number">9</div>
                        <h3>Dark Web Navigation</h3>
                        <p>Safely explore the Dark Web, use .onion search engines, identify scams, understand Deep Web vs Dark Web, find resources.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">4-5 hours</div>
                    </div>
                </div>
            </div>

 <div class="level-section">
                <div class="level-header">
                    <div class="level-badge">L3</div>
                    <div class="level-info">
                        <h4>Level 3: Advanced Techniques</h4>
                        <div class="level-meta">
                            <span>Duration: 5-6 weeks</span>
                            <span>5 Labs</span>
                            <span>Difficulty: Hard</span>
                        </div>
                    </div>
                </div>

 <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-number">10</div>
                        <h3>Create Your Own .onion Site</h3>
                        <p>Set up a hidden service, configure Nginx/Apache, understand rendezvous points, generate vanity addresses, and security hardening.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">8-10 hours</div>
                    </div>

 <div class="project-card">
                        <div class="project-number">11</div>
                        <h3>Whonix - Maximum Isolation</h3>
                        <p>Deploy Whonix Gateway + Workstation, understand VM isolation, stream isolation, compare with Tails, advanced configurations.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">7-9 hours</div>
                    </div>

   <div class="project-card">
                        <div class="project-number">12</div>
                        <h3>Attacks Against Tor</h3>
                        <p>Understand deanonymization: traffic correlation, website fingerprinting, bad exit nodes, timing attacks, and NSA capabilities.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">6-8 hours</div>
                    </div>

 <div class="project-card">
                        <div class="project-number">13</div>
                        <h3>Monero & Anonymous Crypto</h3>
                        <p>Why Bitcoin isn't anonymous, master Monero (XMR), use mixers/tumblers, atomic swaps, and anonymous transactions.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">6-7 hours</div>
                    </div>

  <div class="project-card">
                        <div class="project-number">14</div>
                        <h3>Metadata Analysis & Removal</h3>
                        <p>Analyze file metadata (EXIF, PDF), use MAT2 for removal, understand metadata in documents, images, and communications.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">4-5 hours</div>
                    </div>
                </div>
            </div>

 <div class="level-section">
                <div class="level-header">
                    <div class="level-badge">L4</div>
                    <div class="level-info">
                        <h4>Level 4: Expert Mastery</h4>
                        <div class="level-meta">
                            <span>Duration: 6-7 weeks</span>
                            <span>5 Labs</span>
                            <span>Difficulty: Expert</span>
                        </div>
                    </div>
                </div>

   <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-number">15</div>
                        <h3>OSINT on the Dark Web</h3>
                        <p>Dark Web intelligence gathering, use OnionScan, scrape .onion sites ethically, monitor changes, build relationship graphs.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">8-10 hours</div>
                    </div>

<div class="project-card">
                        <div class="project-number">16</div>
                        <h3>Run a Tor Relay</h3>
                        <p>Contribute to Tor network by running a relay. Middle relays vs exit nodes, legal considerations, monitoring, and optimization.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">10-12 hours</div>
                    </div>

 <div class="project-card">
                        <div class="project-number">17</div>
                        <h3>Forensics & Anti-Forensics</h3>
                        <p>Analyze Tails for traces, RAM forensics, cold boot attacks, disk encryption forensics, and advanced anti-forensics techniques.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">10-12 hours</div>
                    </div>

  <div class="project-card">
                        <div class="project-number">18</div>
                        <h3>Advanced Persistent Anonymity</h3>
                        <p>Build complete anonymous infrastructure: Whonix + Qubes OS + Tor + VPN chains + compartmentalized identities + OPSEC protocols.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">15-20 hours</div>
                    </div>

  <div class="project-card">
                        <div class="project-number">19</div>
                        <h3>Final Project: Journalist Infrastructure</h3>
                        <p>Complete anonymous system for investigative journalism: Tails + Whonix + Hidden Service + SecureDrop + Encrypted comms + Full OPSEC.</p>
                        <div class="status-badge status-upcoming">Upcoming</div>
                        <div class="project-duration">25-35 hours</div>
                    </div>
                </div>
            </div>
        </div>

  <div class="timeline">
            <h3>Suggested Timeline</h3>
            <div class="timeline-item">
                <div class="timeline-week">Week 1-3</div>
                <div class="timeline-content">
                    <p><strong>Level 0 - Foundations:</strong> Labs 0-0.2 - Build essential networking, crypto, and Linux skills</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-week">Week 4-7</div>
                <div class="timeline-content">
                    <p><strong>Level 1 - Privacy Basics:</strong> Labs 1-4 - Master Tor Browser and secure communications</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-week">Week 8-12</div>
                <div class="timeline-content">
                    <p><strong>Level 2 - Intermediate:</strong> Labs 5-9 - Deploy Tails, learn OPSEC, explore Dark Web safely</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-week">Week 13-18</div>
                <div class="timeline-content">
                    <p><strong>Level 3 - Advanced:</strong> Labs 10-14 - Build .onion sites, deploy Whonix, understand attacks</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-week">Week 19-24</div>
                <div class="timeline-content">
                    <p><strong>Level 4 - Expert:</strong> Labs 15-19 - Run Tor relay, master forensics, complete final project</p>
                </div>
            </div>
        </div>

 <div class="info-box">
            <h3>What You Will Master</h3>
            <ul>
                <li><strong>Networking & Protocols:</strong> Deep understanding of TCP/IP, DNS, VPNs, and proxy chains</li>
                <li><strong>Cryptography:</strong> Symmetric/asymmetric encryption, PGP/GPG, TLS/SSL, and secure protocols</li>
                <li><strong>Tor Network:</strong> Onion routing architecture, hidden services, and circuit analysis</li>
                <li><strong>Tails & Whonix:</strong> Expert-level configuration and operational deployment</li>
                <li><strong>OPSEC:</strong> Identity compartmentalization, threat modeling, and operational security</li>
                <li><strong>Dark Web:</strong> Safe navigation, .onion services, and OSINT techniques</li>
                <li><strong>Cryptocurrencies:</strong> Anonymous transactions with Monero and privacy coins</li>
                <li><strong>Anti-Forensics:</strong> Metadata removal, disk encryption, and covering digital tracks</li>
            </ul>
        </div>

  <h2 class="section-title">Resources & Tools</h2>

   <div class="resources-grid">
            <div class="resource-card">
                <h4>Essential Reading</h4>
                <ul>
                    <li>The Art of Invisibility - Kevin Mitnick</li>
                    <li>Extreme Privacy - Michael Bazzell</li>
                    <li>Permanent Record - Edward Snowden</li>
                    <li>Tor Project Documentation</li>
                    <li>NIST Cryptography Standards</li>
                </ul>
            </div>

   <div class="resource-card">
                <h4>Required Tools</h4>
                <ul>
                    <li>Tails OS (Live USB 8GB+)</li>
                    <li>Tor Browser Bundle</li>
                    <li>Whonix (Gateway + Workstation)</li>
                    <li>VirtualBox / VMware</li>
                    <li>KeePassXC (Password Manager)</li>
                    <li>VeraCrypt (Disk Encryption)</li>
                </ul>
            </div>

  <div class="resource-card">
                <h4>Official Sites</h4>
                <ul>
                    <li><a href="https://www.torproject.org" target="_blank">torproject.org</a></li>
                    <li><a href="https://tails.boum.org" target="_blank">tails.boum.org</a></li>
                    <li><a href="https://www.whonix.org" target="_blank">whonix.org</a></li>
                    <li><a href="https://www.privacyguides.org" target="_blank">privacyguides.org</a></li>
                    <li><a href="https://www.getmonero.org" target="_blank">getmonero.org</a></li>
                </ul>
            </div>

  <div class="resource-card">
                <h4>Learning Resources</h4>
                <ul>
                    <li><a href="https://www.eff.org/pages/tor-and-https" target="_blank">EFF - Tor & HTTPS</a></li>
                    <li><a href="https://github.com/Attacks-on-Tor/Attacks-on-Tor" target="_blank">Attacks on Tor (GitHub)</a></li>
                    <li><a href="https://www.youtube.com/@TheHatedOne" target="_blank">The Hated One (YouTube)</a></li>
                    <li>OWASP Privacy Project</li>
                    <li>Privacy Tools subreddit</li>
                </ul>
            </div>

   <div class="resource-card">
                <h4>Communities</h4>
                <ul>
                    <li>r/TOR (Reddit)</li>
                    <li>r/privacy (Reddit)</li>
                    <li>r/onions (Reddit - legal only)</li>
                    <li>Tor Project IRC</li>
                    <li>Privacy Guides Forum</li>
                </ul>
            </div>

   <div class="resource-card">
                <h4>Practice Environments</h4>
                <ul>
                    <li>TryHackMe - Privacy Rooms</li>
                    <li>HackTheBox - Anonymity Labs</li>
                    <li>Local VM Lab Setup</li>
                    <li>Tor Test Network</li>
                    <li>Whonix Testbed</li>
                </ul>
            </div>
        </div>

 <div class="info-box">
            <h3>Prerequisites & Requirements</h3>
            <ul>
                <li><strong>Basic Linux Knowledge:</strong> Command line, package management, file permissions, services</li>
                <li><strong>Networking Fundamentals:</strong> TCP/IP, DNS, HTTP/HTTPS, routing concepts</li>
                <li><strong>Security Mindset:</strong> Threat modeling, risk assessment, critical thinking</li>
                <li><strong>Hardware:</strong> USB drive (8GB+), computer with 8GB+ RAM for VMs, dedicated practice machine recommended</li>
                <li><strong>Time Commitment:</strong> 20-24 weeks at 8-12 hours per week (160-280 hours total)</li>
                <li><strong>Recommended Background:</strong> Completed basic cybersecurity or networking course</li>
            </ul>
        </div>
   <div class="footer-nav">
            <a href="/my-lab" class="nav-button">Back to Lab</a>
            <a href="https://www.torproject.org/" target="_blank" class="nav-button">Tor Project</a>
            <a href="https://tails.boum.org/" target="_blank" class="nav-button">Tails OS</a>
            <a href="https://www.whonix.org/" target="_blank" class="nav-button">Whonix</a>
        </div>
    </div>

<script>
        document.addEventListener('DOMContentLoaded', function() {
            const binaryContainer = document.querySelector('.binary-background');
            
            for (let i = 0; i < 100; i++) {
                const digit = document.createElement('div');
                digit.className = 'binary-digit';
                digit.textContent = Math.random() > 0.5 ? '1' : '0';
                digit.style.left = Math.random() * 100 + 'vw';
                digit.style.fontSize = (Math.random() * 18 + 12) + 'px';
                digit.style.animationDuration = (Math.random() * 10 + 5) + 's';
                digit.style.animationDelay = Math.random() * 5 + 's';
                digit.style.opacity = Math.random() * 0.2 + 0.05;
                const colors = ['rgba(147, 51, 234, 0.15)', 'rgba(168, 85, 247, 0.15)', 'rgba(124, 58, 237, 0.15)'];
                digit.style.color = colors[Math.floor(Math.random() * colors.length)];
                binaryContainer.appendChild(digit);
            }
            
            for (let i = 0; i < 30; i++) {
                const floatDigit = document.createElement('div');
                floatDigit.className = 'binary-digit float';
                floatDigit.textContent = Math.random() > 0.5 ? '1' : '0';
                floatDigit.style.left = Math.random() * 100 + 'vw';
                floatDigit.style.top = Math.random() * 100 + 'vh';
                floatDigit.style.fontSize = (Math.random() * 22 + 14) + 'px';
                floatDigit.style.animationDelay = Math.random() * 2 + 's';
                floatDigit.style.opacity = Math.random() * 0.3 + 0.1;
                const floatColors = ['rgba(147, 51, 234, 0.25)', 'rgba(168, 85, 247, 0.25)'];
                floatDigit.style.color = floatColors[Math.floor(Math.random() * floatColors.length)];
                binaryContainer.appendChild(floatDigit);
            }
        });
    </script>
</body>
</html>
