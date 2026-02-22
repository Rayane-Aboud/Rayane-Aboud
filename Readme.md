<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rayane Aboud — Systems Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #050a0f;
    --surface: #0a1520;
    --border: #0d2035;
    --accent: #00c8ff;
    --accent2: #00ff9d;
    --accent3: #ff6b35;
    --text: #c9d8e8;
    --muted: #4a6070;
    --white: #eaf4ff;
    --glow: 0 0 20px rgba(0,200,255,0.3);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    line-height: 1.7;
  }

  /* Grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,200,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,200,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  /* Glow orbs */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(100px);
    pointer-events: none;
    z-index: 0;
  }
  .orb1 { width: 500px; height: 500px; background: rgba(0,200,255,0.06); top: -100px; left: -100px; }
  .orb2 { width: 400px; height: 400px; background: rgba(0,255,157,0.04); bottom: 20%; right: -100px; }

  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    padding: 80px 0 60px;
    text-align: center;
    position: relative;
  }

  .bismillah {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    color: var(--accent);
    letter-spacing: 0.1em;
    margin-bottom: 32px;
    opacity: 0.8;
  }

  .flag {
    font-size: 2rem;
    display: inline-block;
    animation: wave 2s ease-in-out infinite;
    transform-origin: bottom right;
  }
  @keyframes wave {
    0%, 100% { transform: rotate(0deg); }
    25% { transform: rotate(8deg); }
    75% { transform: rotate(-4deg); }
  }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 800;
    color: var(--white);
    line-height: 1.1;
    margin: 12px 0 8px;
    letter-spacing: -0.02em;
  }

  .hero-name span {
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-title {
    font-size: 1rem;
    color: var(--muted);
    margin-bottom: 24px;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  /* Typing animation */
  .typing-line {
    display: inline-block;
    font-size: 0.9rem;
    color: var(--accent);
    border-right: 2px solid var(--accent);
    padding-right: 4px;
    overflow: hidden;
    white-space: nowrap;
    animation: typing 4s steps(40) infinite, blink 0.7s step-end infinite;
    max-width: 400px;
  }
  @keyframes typing {
    0%, 10% { width: 0; }
    40%, 60% { width: 100%; }
    90%, 100% { width: 0; }
  }
  @keyframes blink { 50% { border-color: transparent; } }

  /* Social links */
  .social-links {
    display: flex;
    gap: 12px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 32px;
  }

  .social-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 1px solid var(--border);
    border-radius: 4px;
    color: var(--text);
    text-decoration: none;
    font-size: 0.8rem;
    font-family: 'JetBrains Mono', monospace;
    transition: all 0.2s;
    background: var(--surface);
    letter-spacing: 0.05em;
  }
  .social-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: var(--glow);
    transform: translateY(-2px);
  }
  .social-btn svg { width: 16px; height: 16px; fill: currentColor; }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent), var(--accent2), transparent);
    margin: 40px 0;
    opacity: 0.4;
  }

  /* ── SECTION HEADERS ── */
  .section-header {
    font-family: 'Syne', sans-serif;
    font-size: 1.4rem;
    font-weight: 800;
    color: var(--white);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-header::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── CODE BLOCK ── */
  .code-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: 40px;
  }
  .code-bar {
    background: #071018;
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
    border-bottom: 1px solid var(--border);
  }
  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-r { background: #ff5f57; }
  .dot-y { background: #febc2e; }
  .dot-g { background: #28c840; }
  .code-lang {
    margin-left: auto;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }
  .code-content {
    padding: 24px;
    font-size: 0.82rem;
    line-height: 1.8;
    overflow-x: auto;
  }
  .kw { color: #ff79c6; }
  .ty { color: #8be9fd; }
  .st { color: #f1fa8c; }
  .cm { color: var(--muted); font-style: italic; }
  .fn-name { color: #50fa7b; }
  .prop { color: var(--accent); }
  .val { color: #ff6b35; }

  /* ── ACHIEVEMENT CARDS ── */
  .achievements {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
    margin-bottom: 40px;
  }
  .ach-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }
  .ach-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }
  .ach-card:hover { border-color: var(--accent); transform: translateY(-3px); box-shadow: var(--glow); }
  .ach-card:hover::before { transform: scaleX(1); }
  .ach-icon { font-size: 1.5rem; margin-bottom: 10px; }
  .ach-stat {
    font-family: 'Syne', sans-serif;
    font-size: 1.6rem;
    font-weight: 800;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 6px;
  }
  .ach-desc { font-size: 0.75rem; color: var(--muted); line-height: 1.5; }

  /* ── TECH STACK ── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 12px;
    margin-bottom: 40px;
  }
  .tech-chip {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 12px;
    text-align: center;
    font-size: 0.8rem;
    color: var(--text);
    transition: all 0.2s;
    cursor: default;
  }
  .tech-chip .tech-icon { font-size: 1.4rem; display: block; margin-bottom: 6px; }
  .tech-chip:hover { border-color: var(--accent2); color: var(--accent2); transform: scale(1.04); }

  /* ── STATS SECTION ── */
  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 40px;
  }
  .stat-box {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    font-size: 0.8rem;
    color: var(--muted);
  }
  .stat-box .label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
    margin-bottom: 8px;
  }
  .stat-row-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 6px 0;
    border-bottom: 1px solid var(--border);
    font-size: 0.78rem;
  }
  .stat-row-item:last-child { border-bottom: none; }
  .stat-row-item .name { color: var(--text); }
  .stat-row-item .val { color: var(--accent); }

  /* ── FOOTER ── */
  footer {
    text-align: center;
    padding: 40px 0 60px;
    color: var(--muted);
    font-size: 0.75rem;
    border-top: 1px solid var(--border);
  }
  footer .quote {
    color: var(--accent);
    font-style: italic;
    margin-top: 8px;
    font-size: 0.85rem;
  }
  .flag-colors { display: flex; justify-content: center; gap: 6px; margin-top: 12px; }
  .flag-dot { width: 10px; height: 10px; border-radius: 50%; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero { animation: fadeUp 0.8s ease forwards; }
  .code-block { animation: fadeUp 0.8s 0.2s ease both; }
  .achievements { animation: fadeUp 0.8s 0.4s ease both; }

  @media (max-width: 600px) {
    .stats-row { grid-template-columns: 1fr; }
    .hero-name { font-size: 2rem; }
  }
</style>
</head>
<body>

<div class="orb orb1"></div>
<div class="orb orb2"></div>

<div class="container">

  <!-- HERO -->
  <section class="hero">
    <div class="bismillah">بسم الله الرحمن الرحيم</div>
    <div>Hi 👋, I'm</div>
    <h1 class="hero-name"><span>Rayane Aboud</span> <span class="flag">🇩🇿</span></h1>
    <p class="hero-title">Software &amp; Systems Engineer · Algiers, Algeria</p>
    <div class="typing-line">Optimizing systems one microsecond at a time...</div>

    <div class="social-links">
      <a href="https://www.linkedin.com/in/rayane-aboud-611ab91a5/" class="social-btn" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="https://github.com/Rayane-Aboud" class="social-btn" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="mailto:rayane.aboud02@gmail.com" class="social-btn">
        <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
        Email
      </a>
      <a href="https://discord.com/users/rayane_aboud" class="social-btn" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057c.002.022.015.04.032.055a19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/></svg>
        Discord
      </a>
    </div>
  </section>

  <div class="divider"></div>

  <!-- ABOUT -->
  <section>
    <h2 class="section-header">🎯 About Me</h2>
    <div class="code-block">
      <div class="code-bar">
        <span class="dot dot-r"></span>
        <span class="dot dot-y"></span>
        <span class="dot dot-g"></span>
        <span class="code-lang">Rust</span>
      </div>
      <div class="code-content">
        <span class="kw">struct</span> <span class="ty">Engineer</span> {<br>
        &nbsp;&nbsp;<span class="prop">name</span>: <span class="st">"Rayane Aboud"</span>,<br>
        &nbsp;&nbsp;<span class="prop">role</span>: <span class="st">"Software &amp; Systems Engineer"</span>,<br>
        &nbsp;&nbsp;<span class="prop">company</span>: <span class="st">"Ouedkniss — Algeria's Leading Classifieds Platform"</span>,<br>
        &nbsp;&nbsp;<span class="prop">education</span>: <span class="st">"ESI Algiers · State Engineer &amp; Master 2 · GPA 3.7/4.0"</span>,<br>
        &nbsp;&nbsp;<span class="prop">location</span>: <span class="st">"Algiers, Algeria 🇩🇿"</span>,<br>
        }<br><br>

        <span class="kw">impl</span> <span class="ty">Engineer</span> {<br>
        &nbsp;&nbsp;<span class="kw">fn</span> <span class="fn-name">specializations</span>(&amp;<span class="kw">self</span>) -&gt; <span class="ty">Vec</span>&lt;&amp;<span class="kw">str</span>&gt; {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;vec![<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">"High-Performance Systems"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">"Edge AI &amp; MLOps"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">"Distributed Systems"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">"Performance Optimization"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="st">"Cloud-Native Technologies"</span>,<br>
        &nbsp;&nbsp;&nbsp;&nbsp;]<br>
        &nbsp;&nbsp;}<br>
        }
      </div>
    </div>
  </section>

  <!-- ACHIEVEMENTS -->
  <section>
    <h2 class="section-header">🏆 Key Achievements</h2>
    <div class="achievements">
      <div class="ach-card">
        <div class="ach-icon">⚡</div>
        <div class="ach-stat">Rust</div>
        <div class="ach-desc">Migrated core services — reduced latency &amp; improved throughput significantly</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">📦</div>
        <div class="ach-stat">40 → 8</div>
        <div class="ach-desc">Consolidated microservices to pods while maintaining 99.9% availability</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🧠</div>
        <div class="ach-stat">&lt;100ms</div>
        <div class="ach-desc">LSTM pipeline inference on edge devices</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">📄</div>
        <div class="ach-stat">2025</div>
        <div class="ach-desc">Published research at MedCCAI 2025</div>
      </div>
    </div>
  </section>

  <!-- TECH STACK -->
  <section>
    <h2 class="section-header">🛠️ Technology Arsenal</h2>
    <div class="tech-grid">
      <div class="tech-chip"><span class="tech-icon">🦀</span>Rust</div>
      <div class="tech-chip"><span class="tech-icon">⚙️</span>C / C++</div>
      <div class="tech-chip"><span class="tech-icon">🐍</span>Python</div>
      <div class="tech-chip"><span class="tech-icon">🐹</span>Go</div>
      <div class="tech-chip"><span class="tech-icon">🟨</span>JavaScript</div>
      <div class="tech-chip"><span class="tech-icon">🔷</span>TypeScript</div>
      <div class="tech-chip"><span class="tech-icon">☸️</span>Kubernetes</div>
      <div class="tech-chip"><span class="tech-icon">🐳</span>Docker</div>
      <div class="tech-chip"><span class="tech-icon">🔥</span>PyTorch</div>
      <div class="tech-chip"><span class="tech-icon">☁️</span>Cloud</div>
      <div class="tech-chip"><span class="tech-icon">📊</span>MLOps</div>
      <div class="tech-chip"><span class="tech-icon">🗄️</span>Postgres</div>
    </div>
  </section>

  <!-- STATS -->
  <section>
    <h2 class="section-header">📊 GitHub Analytics</h2>
    <div class="stats-row">
      <div class="stat-box">
        <div class="label">Top Languages</div>
        <div class="stat-row-item"><span class="name">Rust</span><span class="val">████████░░ 42%</span></div>
        <div class="stat-row-item"><span class="name">Python</span><span class="val">██████░░░░ 28%</span></div>
        <div class="stat-row-item"><span class="name">C++</span><span class="val">████░░░░░░ 18%</span></div>
        <div class="stat-row-item"><span class="name">Go</span><span class="val">██░░░░░░░░ 8%</span></div>
        <div class="stat-row-item"><span class="name">Other</span><span class="val">█░░░░░░░░░ 4%</span></div>
      </div>
      <div class="stat-box">
        <div class="label">Profile Overview</div>
        <div class="stat-row-item"><span class="name">Company</span><span class="val">Ouedkniss</span></div>
        <div class="stat-row-item"><span class="name">Location</span><span class="val">Algiers 🇩🇿</span></div>
        <div class="stat-row-item"><span class="name">Education</span><span class="val">ESI Algiers</span></div>
        <div class="stat-row-item"><span class="name">GPA</span><span class="val">3.7 / 4.0</span></div>
        <div class="stat-row-item"><span class="name">Research</span><span class="val">MedCCAI 2025</span></div>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- FOOTER -->
  <footer>
    <div>⭐ From <strong>Rayane-Aboud</strong> with 💚 ❤️ 🖤 🤍</div>
    <div class="quote">"Optimizing systems one microsecond at a time"</div>
    <div class="flag-colors">
      <div class="flag-dot" style="background:#006233"></div>
      <div class="flag-dot" style="background:#ffffff"></div>
      <div class="flag-dot" style="background:#d21034"></div>
    </div>
  </footer>

</div>

</body>
</html>
