<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Husin Bin Hamdan — Automation & Robotics Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0e14;
    --surface: #111620;
    --surface2: #181f2e;
    --accent: #00e5a0;
    --accent2: #0099ff;
    --amber: #f5a623;
    --text: #e8edf5;
    --muted: #7a8499;
    --border: rgba(255,255,255,0.07);
    --card-border: rgba(0,229,160,0.12);
    --font-display: 'DM Serif Display', serif;
    --font-ui: 'Syne', sans-serif;
    --font-mono: 'DM Mono', monospace;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-ui);
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    background: rgba(10,14,20,0.85);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid var(--border);
    padding: 0 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 58px;
  }
  .nav-logo {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 0.08em;
    text-decoration: none;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 13px;
    font-weight: 600;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 100px 2rem 60px;
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
  }
  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
    width: 100%;
  }
  .hero-tag {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .hero-tag::before {
    content: '';
    display: inline-block;
    width: 24px; height: 1px;
    background: var(--accent);
  }
  h1 {
    font-family: var(--font-display);
    font-size: clamp(2.8rem, 5vw, 4.5rem);
    line-height: 1.05;
    color: var(--text);
    margin-bottom: 1.5rem;
  }
  h1 em {
    font-style: italic;
    color: var(--accent);
  }
  .hero-desc {
    font-size: 1.05rem;
    color: var(--muted);
    line-height: 1.75;
    margin-bottom: 2.5rem;
    max-width: 480px;
  }
  .hero-cta {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }
  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 28px;
    background: var(--accent);
    color: #0a0e14;
    font-family: var(--font-ui);
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border: none;
    cursor: pointer;
    text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 12px) 0, 100% 12px, 100% 100%, 12px 100%, 0 calc(100% - 12px));
    transition: opacity 0.2s, transform 0.2s;
  }
  .btn-primary:hover { opacity: 0.85; transform: translateY(-2px); }
  .btn-outline {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 28px;
    background: transparent;
    color: var(--text);
    font-family: var(--font-ui);
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border: 1px solid var(--border);
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

  /* Hero visual */
  .hero-visual {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .hero-card {
    background: var(--surface);
    border: 1px solid var(--card-border);
    padding: 2.5rem;
    width: 100%;
    max-width: 400px;
    position: relative;
    clip-path: polygon(0 0, calc(100% - 20px) 0, 100% 20px, 100% 100%, 20px 100%, 0 calc(100% - 20px));
  }
  .hero-card::before {
    content: '';
    position: absolute;
    top: -1px; right: 20px;
    width: 100px; height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent));
  }
  .stat-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }
  .stat-box {
    padding: 1rem;
    background: var(--surface2);
    border: 1px solid var(--border);
  }
  .stat-num {
    font-family: var(--font-mono);
    font-size: 1.8rem;
    font-weight: 500;
    color: var(--accent);
    display: block;
  }
  .stat-label {
    font-size: 11px;
    font-weight: 600;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }
  .skill-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 1rem;
  }
  .badge {
    font-family: var(--font-mono);
    font-size: 11px;
    padding: 4px 10px;
    border: 1px solid var(--border);
    color: var(--muted);
    letter-spacing: 0.06em;
  }
  .badge.accent { border-color: var(--accent); color: var(--accent); }
  .badge.blue { border-color: var(--accent2); color: var(--accent2); }

  /* SECTION COMMON */
  section { padding: 100px 2rem; max-width: 1200px; margin: 0 auto; }
  .section-label {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.14em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    max-width: 80px;
  }
  h2 {
    font-family: var(--font-display);
    font-size: clamp(2rem, 3.5vw, 3rem);
    margin-bottom: 3rem;
    color: var(--text);
  }
  h2 span { color: var(--accent); font-style: italic; }

  /* SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem;
  }
  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 1.75rem;
    position: relative;
    transition: border-color 0.3s, transform 0.3s;
    overflow: hidden;
  }
  .skill-card:hover { border-color: var(--accent); transform: translateY(-4px); }
  .skill-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    height: 2px; width: 0;
    background: var(--accent);
    transition: width 0.4s;
  }
  .skill-card:hover::after { width: 100%; }
  .skill-icon {
    width: 44px; height: 44px;
    background: var(--surface2);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1.25rem;
    font-size: 20px;
  }
  .skill-card h3 {
    font-family: var(--font-ui);
    font-size: 15px;
    font-weight: 700;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    margin-bottom: 1rem;
    color: var(--text);
  }
  .skill-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .skill-list li {
    font-size: 13px;
    color: var(--muted);
    display: flex;
    align-items: flex-start;
    gap: 8px;
  }
  .skill-list li::before {
    content: '›';
    color: var(--accent);
    font-size: 16px;
    line-height: 1.2;
    flex-shrink: 0;
  }

  /* EXPERIENCE */
  .timeline { position: relative; }
  .timeline::before {
    content: '';
    position: absolute;
    left: 10px; top: 0; bottom: 0;
    width: 1px;
    background: var(--border);
  }
  .timeline-item {
    padding-left: 3rem;
    position: relative;
    margin-bottom: 3rem;
  }
  .timeline-dot {
    position: absolute;
    left: 0; top: 6px;
    width: 20px; height: 20px;
    border: 1px solid var(--accent);
    background: var(--bg);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .timeline-dot::after {
    content: '';
    width: 6px; height: 6px;
    background: var(--accent);
  }
  .exp-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 1.75rem 2rem;
    transition: border-color 0.3s;
  }
  .exp-card:hover { border-color: rgba(0,229,160,0.3); }
  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 1rem;
    margin-bottom: 0.25rem;
    flex-wrap: wrap;
  }
  .exp-role {
    font-size: 17px;
    font-weight: 700;
    color: var(--text);
    letter-spacing: 0.02em;
  }
  .exp-period {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    padding: 3px 10px;
    border: 1px solid var(--card-border);
    white-space: nowrap;
  }
  .exp-company {
    font-size: 13px;
    color: var(--accent2);
    font-weight: 600;
    letter-spacing: 0.04em;
    margin-bottom: 1rem;
  }
  .exp-points { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .exp-points li {
    font-size: 14px;
    color: var(--muted);
    display: flex;
    align-items: flex-start;
    gap: 10px;
    line-height: 1.55;
  }
  .exp-points li::before {
    content: '—';
    color: var(--accent);
    flex-shrink: 0;
    font-family: var(--font-mono);
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 2rem;
    position: relative;
    transition: transform 0.3s, border-color 0.3s;
    overflow: hidden;
  }
  .project-card:hover { transform: translateY(-4px); border-color: rgba(0,153,255,0.3); }
  .project-card--featured { border-color: rgba(0,229,160,0.2); }
  .project-card--featured:hover { border-color: rgba(0,229,160,0.5); }
  .project-featured-badge {
    display: inline-block;
    font-family: var(--font-mono);
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #0a0e14;
    background: #00e5a0;
    padding: 3px 10px;
    margin-bottom: 0.85rem;
  }
  .accent-tag { border-color: rgba(0,229,160,0.4) !important; color: #00e5a0 !important; }
  .project-num {
    font-family: var(--font-mono);
    font-size: 48px;
    font-weight: 500;
    color: rgba(0,229,160,0.07);
    position: absolute;
    top: 1rem; right: 1.5rem;
    line-height: 1;
    pointer-events: none;
  }
  .project-card h3 {
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 0.75rem;
    line-height: 1.3;
    padding-right: 3rem;
  }
  .project-desc {
    font-size: 13.5px;
    color: var(--muted);
    line-height: 1.65;
    margin-bottom: 1.25rem;
  }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag {
    font-family: var(--font-mono);
    font-size: 11px;
    padding: 3px 8px;
    background: var(--surface2);
    color: var(--muted);
    border: 1px solid var(--border);
    letter-spacing: 0.05em;
  }

  /* EDUCATION */
  .edu-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }
  .edu-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 2rem;
    position: relative;
    overflow: hidden;
  }
  .edu-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: var(--accent);
  }
  .edu-degree {
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 0.4rem;
    line-height: 1.35;
  }
  .edu-school {
    font-size: 13px;
    color: var(--accent2);
    font-weight: 600;
    margin-bottom: 0.4rem;
  }
  .edu-period {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--muted);
  }
  .edu-note {
    margin-top: 0.75rem;
    font-size: 13px;
    color: var(--muted);
    font-style: italic;
  }

  /* CONTACT */
  .contact-inner {
    background: var(--surface);
    border: 1px solid var(--card-border);
    padding: 3rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: center;
    position: relative;
    overflow: hidden;
  }
  .contact-inner::before {
    content: '';
    position: absolute;
    top: -1px; left: 0;
    height: 2px; width: 60%;
    background: linear-gradient(90deg, var(--accent), transparent);
  }
  .contact-title {
    font-family: var(--font-display);
    font-size: 2.2rem;
    line-height: 1.2;
    margin-bottom: 1rem;
    color: var(--text);
  }
  .contact-title em { color: var(--accent); font-style: italic; }
  .contact-sub { font-size: 14px; color: var(--muted); line-height: 1.7; }
  .contact-list { list-style: none; display: flex; flex-direction: column; gap: 1rem; }
  .contact-list li {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 14px;
    color: var(--muted);
  }
  .contact-icon {
    width: 36px; height: 36px;
    background: var(--surface2);
    border: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }
  .contact-list a { color: var(--text); text-decoration: none; }
  .contact-list a:hover { color: var(--accent); }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--border);
    padding: 2rem;
    text-align: center;
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 0.06em;
  }
  footer span { color: var(--accent); }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero-text > * { animation: fadeUp 0.7s ease both; }
  .hero-text > *:nth-child(1) { animation-delay: 0.1s; }
  .hero-text > *:nth-child(2) { animation-delay: 0.2s; }
  .hero-text > *:nth-child(3) { animation-delay: 0.3s; }
  .hero-text > *:nth-child(4) { animation-delay: 0.4s; }
  .hero-visual { animation: fadeUp 0.8s 0.5s ease both; }

  /* DIVIDER */
  .full-divider {
    width: 100%; height: 1px;
    background: var(--border);
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    .hero-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .hero-visual { order: -1; }
    .hero-card { max-width: 100%; }
    .contact-inner { grid-template-columns: 1fr; }
    nav .nav-links { display: none; }
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--accent); opacity: 0.5; }

  /* GLOW DOT BACKGROUND */
  body::before {
    content: '';
    position: fixed;
    top: -200px; right: -200px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(0,229,160,0.04) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  /* PROJECT GALLERY */
  .gallery-section {
    margin-top: 1.25rem;
    border-top: 1px solid var(--border);
    padding-top: 1rem;
  }
  .gallery-label {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .gallery-label::before { content: "//"; color: var(--accent); }
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
    gap: 8px;
  }
  .gallery-thumb {
    aspect-ratio: 1;
    overflow: hidden;
    border: 1px solid var(--border);
    cursor: pointer;
    transition: border-color 0.2s, transform 0.2s;
    background: var(--surface2);
  }
  .gallery-thumb:hover { border-color: var(--accent); transform: scale(1.03); }
  .gallery-thumb img { width:100%; height:100%; object-fit:cover; display:block; }
  .gallery-empty {
    font-family: var(--font-mono);
    font-size: 11px;
    color: rgba(122,132,153,0.4);
    letter-spacing: 0.06em;
    font-style: italic;
  }

  /* GALLERY & LIGHTBOX */
  .gallery-thumb { position: relative; }
  .lightbox { display:none; position:fixed; inset:0; z-index:9999; background:rgba(5,8,12,0.96); align-items:center; justify-content:center; flex-direction:column; padding:2rem; }
  .lightbox.open { display:flex; }
  .lightbox-img { max-width:90vw; max-height:82vh; object-fit:contain; border:1px solid var(--border); }
  .lightbox-close { position:fixed; top:1.5rem; right:1.5rem; background:var(--surface); border:1px solid var(--border); color:var(--text); font-size:16px; width:40px; height:40px; cursor:pointer; display:flex; align-items:center; justify-content:center; font-family:var(--font-mono); transition:border-color 0.2s; }
  .lightbox-close:hover { border-color:var(--accent); color:var(--accent); }
  .lightbox-nav { display:flex; gap:1rem; margin-top:1rem; }
  .lightbox-nav button { background:var(--surface); border:1px solid var(--border); color:var(--muted); font-family:var(--font-mono); font-size:13px; padding:6px 16px; cursor:pointer; transition:all 0.2s; }
  .lightbox-nav button:hover { border-color:var(--accent); color:var(--accent); }
  .lightbox-caption { font-family:var(--font-mono); font-size:11px; color:var(--muted); margin-top:0.75rem; letter-spacing:0.06em; }
</style>
</head>
<body>

<nav>
  <a class="nav-logo" href="#">HBH.ENG</a>
  <ul class="nav-links">
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div style="max-width:1200px; margin:0 auto;">
<section class="hero" style="padding-top:100px; max-width:100%;">
  <div class="hero-grid">
    <div class="hero-text">
      <div class="hero-tag">Available for Opportunities</div>
      <h1>Husin Bin<br><em>Hamdan</em></h1>
      <p class="hero-desc">
        Automation &amp; Robotics Engineering student with hands-on experience in robotic systems commissioning, embedded control, IoT integration, and mechanical design for competitive robotics.
      </p>
      <div class="hero-cta">
        <a href="#contact" class="btn-primary">Get In Touch ↗</a>
        <a href="#experience" class="btn-outline">View Work</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-card">
        <div class="section-label" style="margin-bottom:1.25rem; font-size:11px;">Current Focus</div>
        <div class="stat-row">
          <div class="stat-box">
            <span class="stat-num">3+</span>
            <span class="stat-label">Years Hands-On</span>
          </div>
          <div class="stat-box">
            <span class="stat-num">5+</span>
            <span class="stat-label">Tech Projects</span>
          </div>
          <div class="stat-box">
            <span class="stat-num">15%</span>
            <span class="stat-label">Setup Time Saved</span>
          </div>
          <div class="stat-box">
            <span class="stat-num">2025</span>
            <span class="stat-label">Robocon Trials</span>
          </div>
        </div>
        <div class="section-label" style="margin-bottom:0.75rem; font-size:11px;">Core Technologies</div>
        <div class="skill-badges">
          <span class="badge accent">Robotics</span>
          <span class="badge accent">3D CAD</span>
          <span class="badge blue">Python</span>
          <span class="badge blue">C/C++</span>
          <span class="badge">Node-RED</span>
          <span class="badge">SolidWorks</span>
          <span class="badge">PLC</span>
          <span class="badge">IoT</span>
        </div>
      </div>
    </div>
  </div>
</section>
</div>

<!-- SKILLS -->
<div style="max-width:1200px; margin:0 auto; padding:0 2rem;">
  <div class="full-divider" style="padding:0;"></div>
</div>
<section id="skills">
  <div class="section-label">Technical Skills</div>
  <h2>What I <span>Bring</span></h2>
  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-icon">⚙️</div>
      <h3>Mechanical &amp; Design</h3>
      <ul class="skill-list">
        <li>SolidWorks / CATIA / Inventor</li>
        <li>CAD modelling &amp; rapid prototyping</li>
        <li>Structural simulation &amp; impact analysis</li>
        <li>Fabrication, assembly &amp; dimensional QC</li>
        <li>Robot mechanism design &amp; tuning</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">⚡</div>
      <h3>Electrical &amp; Control</h3>
      <ul class="skill-list">
        <li>Circuit wiring &amp; troubleshooting</li>
        <li>Control panel integration</li>
        <li>Sensor &amp; actuator maintenance</li>
        <li>PLC programming (basic)</li>
        <li>Pneumatic application</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🤖</div>
      <h3>Embedded &amp; Software</h3>
      <ul class="skill-list">
        <li>Python &amp; C/C++ programming</li>
        <li>Microcontroller-based system design</li>
        <li>Real-time data acquisition</li>
        <li>IMU sensor integration &amp; feedback control</li>
        <li>Embedded control algorithms</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🌐</div>
      <h3>Automation &amp; IoT</h3>
      <ul class="skill-list">
        <li>Robotic system integration &amp; commissioning</li>
        <li>Node-RED IoT integration</li>
        <li>System diagnostics &amp; troubleshooting</li>
        <li>SMART Agriculture monitoring systems</li>
        <li>Real-time process monitoring</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">📊</div>
      <h3>Data &amp; Analytics</h3>
      <ul class="skill-list">
        <li>Microsoft Excel (Pivot Table, Dashboard)</li>
        <li>Power BI basic visualization</li>
        <li>Financial records &amp; budget reporting</li>
        <li>IoT monitoring database management</li>
      </ul>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🏆</div>
      <h3>Leadership &amp; Team</h3>
      <ul class="skill-list">
        <li>Head of mechanical team — Robocon 2025</li>
        <li>Treasurer &amp; financial management</li>
        <li>R&amp;D collaboration &amp; design iteration</li>
        <li>Technical procurement &amp; sourcing</li>
        <li>Cross-functional team coordination</li>
      </ul>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<div style="max-width:1200px; margin:0 auto; padding:0 2rem;">
  <div class="full-divider" style="padding:0;"></div>
</div>
<section id="experience">
  <div class="section-label">Work History</div>
  <h2>Where I've <span>Worked</span></h2>
  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="exp-card">
        <div class="exp-header">
          <span class="exp-role">Mechanical Design &amp; Procurement Assistant</span>
          <span class="exp-period">Sep 2025 – Apr 2026</span>
        </div>
        <div class="exp-company">FICES Technology — Part-Time</div>
        <ul class="exp-points">
          <li>Designed and developed prototypes for TerraSens — a SMART Agriculture &amp; IoT Monitoring Database system.</li>
          <li>Managed technical component selection and procurement, ensuring compatibility with design specifications.</li>
          <li>Implemented product improvements to enhance functionality, manufacturability, and performance.</li>
          <li>Collaborated with the team to iterate designs and optimize production workflows.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="exp-card">
        <div class="exp-header">
          <span class="exp-role">Head of Mechanical Team — Robotics Competition</span>
          <span class="exp-period">Mar 2024 – Apr 2026</span>
        </div>
        <div class="exp-company">UniKL Malaysia France Institute — Robotique Society</div>
        <ul class="exp-points">
          <li>Led mechanical design and fabrication of competition robot for ABU Robocon Malaysia 2025 trials, achieving improved movement stability and successful task execution.</li>
          <li>Managed the full design lifecycle: prototyping, testing, and mechanism tuning.</li>
          <li>Directed R&amp;D efforts and collaborated across teams to optimize mechanical performance under competition conditions.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="exp-card">
        <div class="exp-header">
          <span class="exp-role">Treasurer — Robotique Society Club</span>
          <span class="exp-period">Mar 2024 – Apr 2026</span>
        </div>
        <div class="exp-company">UniKL Malaysia France Institute</div>
        <ul class="exp-points">
          <li>Managed and monitored all club financial records, tracking expenses for activities and events.</li>
          <li>Maintained organized documentation to ensure full transparency and accountability.</li>
          <li>Prepared financial reports and budget claims to support funding requests.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="exp-card">
        <div class="exp-header">
          <span class="exp-role">Automation Robotic Internship Trainee</span>
          <span class="exp-period">Jun 2023</span>
        </div>
        <div class="exp-company">TXMR SDN BHD</div>
        <ul class="exp-points">
          <li>Contributed to the installation and commissioning of a robotic arm welding system, reducing setup time by 15% through calibration, wiring, and on-site testing.</li>
          <li>Improved system reliability by troubleshooting and maintaining sensors and actuators, reducing unexpected downtime during testing phases.</li>
          <li>Executed end-to-end electrical wiring between control panel and robotic arm, ensuring 100% signal integrity during commissioning tests.</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- PROJECTS -->
<div style="max-width:1200px; margin:0 auto; padding:0 2rem;">
  <div class="full-divider" style="padding:0;"></div>
</div>
<section id="projects">
  <div class="section-label">Featured Projects</div>
  <h2>What I've <span>Built</span></h2>
  <div class="projects-grid">

    <div class="project-card">
      <div class="project-num">01</div>
      <h3>Mecanum Wheel Mobile Robot — Slope Navigation</h3>
      <p class="project-desc">Designed and developed a mobile robot capable of navigating 5–12° inclined surfaces. Integrated IMU sensor for real-time slope detection and implemented IMU-based feedback control with motor load monitoring to eliminate wheel slippage on inclines.</p>
      <div class="project-tags">
        <span class="tag">Mecanum Drive</span>
        <span class="tag">IMU Sensor</span>
        <span class="tag">Feedback Control</span>
        <span class="tag">Embedded C</span>
      </div>
      <div class="gallery-section" id="section-p1">
        <div class="gallery-label">Project Proof — Mecanum Robot</div>
        <div class="gallery-grid" id="grid-p1">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/mr.1.png','Mecanum Robot — 1','grid-p1',0)"><img src="images/p1/mr.1.png" alt="Mecanum Robot 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/mr2.jpg','Mecanum Robot — 2','grid-p1',1)"><img src="images/p1/mr2.jpg" alt="Mecanum Robot 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/mr4.png','Mecanum Robot — 3','grid-p1',2)"><img src="images/p1/mr4.png" alt="Mecanum Robot 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/mr5.jpg','Mecanum Robot — 4','grid-p1',3)"><img src="images/p1/mr5.jpg" alt="Mecanum Robot 4" loading="lazy"></div>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-num">02</div>
      <h3>Combat Robot — 8Kg Class (Robattle Competition, UniKL MFI)</h3>
      <p class="project-desc">Performed structural simulation and impact analysis to evaluate stress distribution and improve frame durability. Executed full fabrication and assembly of components, ensuring dimensional accuracy and structural reliability under competition combat loads.</p>
      <div class="project-tags">
        <span class="tag">FEA Simulation</span>
        <span class="tag">Structural Design</span>
        <span class="tag">Fabrication</span>
        <span class="tag">SolidWorks</span>
      </div>
      <div class="gallery-section" id="section-p2">
        <div class="gallery-label">Project Proof — Combat Robot</div>
        <div class="gallery-grid" id="grid-p2">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr1.jpg','Combat Robot — 1','grid-p2',0)"><img src="images/p1/cr1.jpg" alt="Combat Robot 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr2.jpg','Combat Robot — 2','grid-p2',1)"><img src="images/p1/cr2.jpg" alt="Combat Robot 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr3.jpg','Combat Robot — 3','grid-p2',2)"><img src="images/p1/cr3.jpg" alt="Combat Robot 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr4.jpg','Combat Robot — 4','grid-p2',3)"><img src="images/p1/cr4.jpg" alt="Combat Robot 4" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr5.jpg','Combat Robot — 5','grid-p2',4)"><img src="images/p1/cr5.jpg" alt="Combat Robot 5" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr6.jpg','Combat Robot — 6','grid-p2',5)"><img src="images/p1/cr6.jpg" alt="Combat Robot 6" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr7.jpg','Combat Robot — 7','grid-p2',6)"><img src="images/p1/cr7.jpg" alt="Combat Robot 7" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr8.jpg','Combat Robot — 8','grid-p2',7)"><img src="images/p1/cr8.jpg" alt="Combat Robot 8" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr9.jpg','Combat Robot — 9','grid-p2',8)"><img src="images/p1/cr9.jpg" alt="Combat Robot 9" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/cr10.jpg','Combat Robot — 10','grid-p2',9)"><img src="images/p1/cr10.jpg" alt="Combat Robot 10" loading="lazy"></div>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-num">03</div>
      <h3>TerraSens — SMART Agriculture IoT Monitoring System</h3>
      <p class="project-desc">Designed and prototyped an IoT-based monitoring database system for smart agriculture applications at FICES Technology. Responsible for hardware prototype design, component procurement, and iterative improvement for production-readiness.</p>
      <div class="project-tags">
        <span class="tag">IoT</span>
        <span class="tag">Node-RED</span>
        <span class="tag">Sensor Integration</span>
        <span class="tag">Database</span>
      </div>
      <div class="gallery-section" id="section-p3">
        <div class="gallery-label">Project Proof — TerraSens IoT</div>
        <div class="gallery-grid" id="grid-p3">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr.jpg','TerraSens — 1','grid-p3',0)"><img src="images/p1/tr.jpg" alt="TerraSens 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr1.jpg','TerraSens — 2','grid-p3',1)"><img src="images/p1/tr1.jpg" alt="TerraSens 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr2.jpg','TerraSens — 3','grid-p3',2)"><img src="images/p1/tr2.jpg" alt="TerraSens 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr3.jpg','TerraSens — 4','grid-p3',3)"><img src="images/p1/tr3.jpg" alt="TerraSens 4" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr4.jpg','TerraSens — 5','grid-p3',4)"><img src="images/p1/tr4.jpg" alt="TerraSens 5" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr5.jpg','TerraSens — 6','grid-p3',5)"><img src="images/p1/tr5.jpg" alt="TerraSens 6" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr6.jpg','TerraSens — 7','grid-p3',6)"><img src="images/p1/tr6.jpg" alt="TerraSens 7" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr7.jpg','TerraSens — 8','grid-p3',7)"><img src="images/p1/tr7.jpg" alt="TerraSens 8" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr8.jpg','TerraSens — 9','grid-p3',8)"><img src="images/p1/tr8.jpg" alt="TerraSens 9" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr9.jpg','TerraSens — 10','grid-p3',9)"><img src="images/p1/tr9.jpg" alt="TerraSens 10" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr10.jpg','TerraSens — 11','grid-p3',10)"><img src="images/p1/tr10.jpg" alt="TerraSens 11" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr11.jpg','TerraSens — 12','grid-p3',11)"><img src="images/p1/tr11.jpg" alt="TerraSens 12" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr12.jpg','TerraSens — 13','grid-p3',12)"><img src="images/p1/tr12.jpg" alt="TerraSens 13" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr13.jpg','TerraSens — 14','grid-p3',13)"><img src="images/p1/tr13.jpg" alt="TerraSens 14" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr14.jpg','TerraSens — 15','grid-p3',14)"><img src="images/p1/tr14.jpg" alt="TerraSens 15" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr16.jpg','TerraSens — 16','grid-p3',15)"><img src="images/p1/tr16.jpg" alt="TerraSens 16" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tr17.jpg','TerraSens — 17','grid-p3',16)"><img src="images/p1/tr17.jpg" alt="TerraSens 17" loading="lazy"></div>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-num">04</div>
      <h3>ABU Robocon Malaysia 2025 — Competition Robot</h3>
      <p class="project-desc">Led the mechanical team in the design, fabrication, and fine-tuning of the Robocon competition robot. Managed full design lifecycle from concept to competition-ready prototype, focusing on movement stability and task execution under contest conditions.</p>
      <div class="project-tags">
        <span class="tag">Team Lead</span>
        <span class="tag">CAD Design</span>
        <span class="tag">Prototyping</span>
        <span class="tag">Competition</span>
      </div>
      <div class="gallery-section" id="section-p4">
        <div class="gallery-label">Project Proof — Robocon 2025</div>
        <div class="gallery-grid" id="grid-p4">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb1.jpg','Robocon 2025 — 1','grid-p4',0)"><img src="images/p1/rb1.jpg" alt="Robocon 2025 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb2.jpg','Robocon 2025 — 2','grid-p4',1)"><img src="images/p1/rb2.jpg" alt="Robocon 2025 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb3.jpg','Robocon 2025 — 3','grid-p4',2)"><img src="images/p1/rb3.jpg" alt="Robocon 2025 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb4.jpg','Robocon 2025 — 4','grid-p4',3)"><img src="images/p1/rb4.jpg" alt="Robocon 2025 4" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb5.jpg','Robocon 2025 — 5','grid-p4',4)"><img src="images/p1/rb5.jpg" alt="Robocon 2025 5" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb6.jpg','Robocon 2025 — 6','grid-p4',5)"><img src="images/p1/rb6.jpg" alt="Robocon 2025 6" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/rb7.jpg','Robocon 2025 — 7','grid-p4',6)"><img src="images/p1/rb7.jpg" alt="Robocon 2025 7" loading="lazy"></div>
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="project-num">05</div>
      <h3>Robotic Arm Welding System Commissioning</h3>
      <p class="project-desc">During internship at TXMR SDN BHD, contributed to full end-to-end commissioning of an industrial robotic arm welding system — including system calibration, complete electrical wiring, and on-site testing — achieving a 15% reduction in setup time.</p>
      <div class="project-tags">
        <span class="tag">Industrial Robotics</span>
        <span class="tag">Commissioning</span>
        <span class="tag">Electrical Wiring</span>
        <span class="tag">Calibration</span>
      </div>
      <div class="gallery-section" id="section-p5">
        <div class="gallery-label">Project Proof — Robotic Arm Commissioning</div>
        <div class="gallery-grid" id="grid-p5">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.jpg','TXMR Internship — 1','grid-p5',0)"><img src="images/p1/tx.jpg" alt="TXMR Internship 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.1.jpg','TXMR Internship — 2','grid-p5',1)"><img src="images/p1/tx.1.jpg" alt="TXMR Internship 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.2.jpg','TXMR Internship — 3','grid-p5',2)"><img src="images/p1/tx.2.jpg" alt="TXMR Internship 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.3.jpg','TXMR Internship — 4','grid-p5',3)"><img src="images/p1/tx.3.jpg" alt="TXMR Internship 4" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.4.jpg','TXMR Internship — 5','grid-p5',4)"><img src="images/p1/tx.4.jpg" alt="TXMR Internship 5" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.5.jpg','TXMR Internship — 6','grid-p5',5)"><img src="images/p1/tx.5.jpg" alt="TXMR Internship 6" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.6.jpg','TXMR Internship — 7','grid-p5',6)"><img src="images/p1/tx.6.jpg" alt="TXMR Internship 7" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.7.jpg','TXMR Internship — 8','grid-p5',7)"><img src="images/p1/tx.7.jpg" alt="TXMR Internship 8" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.8.jpg','TXMR Internship — 9','grid-p5',8)"><img src="images/p1/tx.8.jpg" alt="TXMR Internship 9" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.9.jpg','TXMR Internship — 10','grid-p5',9)"><img src="images/p1/tx.9.jpg" alt="TXMR Internship 10" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx.10.jpg','TXMR Internship — 11','grid-p5',10)"><img src="images/p1/tx.10.jpg" alt="TXMR Internship 11" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx11.jpg','TXMR Internship — 12','grid-p5',11)"><img src="images/p1/tx11.jpg" alt="TXMR Internship 12" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx13.jpg','TXMR Internship — 13','grid-p5',12)"><img src="images/p1/tx13.jpg" alt="TXMR Internship 13" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx14.jpg','TXMR Internship — 14','grid-p5',13)"><img src="images/p1/tx14.jpg" alt="TXMR Internship 14" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx16.jpg','TXMR Internship — 15','grid-p5',14)"><img src="images/p1/tx16.jpg" alt="TXMR Internship 15" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx17.jpg','TXMR Internship — 16','grid-p5',15)"><img src="images/p1/tx17.jpg" alt="TXMR Internship 16" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx18.jpg','TXMR Internship — 17','grid-p5',16)"><img src="images/p1/tx18.jpg" alt="TXMR Internship 17" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx19.jpg','TXMR Internship — 18','grid-p5',17)"><img src="images/p1/tx19.jpg" alt="TXMR Internship 18" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/tx20.jpg','TXMR Internship — 19','grid-p5',18)"><img src="images/p1/tx20.jpg" alt="TXMR Internship 19" loading="lazy"></div>
        </div>
      </div>
    </div>

    <div class="project-card project-card--featured">
      <div class="project-num">06</div>
      <div class="project-featured-badge">Achievement</div>
      <h3>Technical Consultant &amp; Fabrication Lead — International Robot Olympiad (IRO) Workshop 2025</h3>
      <p class="project-desc">Served as technical consultant and lead fabricator, providing expert mentorship on an AI-integrated automated sorting dustbin by optimising its conveyor mechanics and implementing complex sensor-wiring architectures for real-time waste classification. Simultaneously spearheaded the mechanical design and component integration for an autonomous lunar exploration robot, ensuring structural integrity and precise hardware arrangement for high-performance mobility.</p>
      <div class="project-tags">
        <span class="tag accent-tag">IRO 2025</span>
        <span class="tag">AI Integration</span>
        <span class="tag">Sensor Wiring</span>
        <span class="tag">Conveyor Design</span>
        <span class="tag">Lunar Robot</span>
        <span class="tag">Mentorship</span>
      </div>
      <div class="gallery-section" id="section-p6">
        <div class="gallery-label">Project Proof — IRO Workshop 2025</div>
        <div class="gallery-grid" id="grid-p6">
          <div class="gallery-thumb" onclick="openLightbox('images/p1/iro1.jpg','IRO Workshop — 1','grid-p6',0)"><img src="images/p1/iro1.jpg" alt="IRO Workshop 1" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/iro2.jpg','IRO Workshop — 2','grid-p6',1)"><img src="images/p1/iro2.jpg" alt="IRO Workshop 2" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/iro3.jpg','IRO Workshop — 3','grid-p6',2)"><img src="images/p1/iro3.jpg" alt="IRO Workshop 3" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/iro4.jpg','IRO Workshop — 4','grid-p6',3)"><img src="images/p1/iro4.jpg" alt="IRO Workshop 4" loading="lazy"></div>
          <div class="gallery-thumb" onclick="openLightbox('images/p1/iro5.jpg','IRO Workshop — 5','grid-p6',4)"><img src="images/p1/iro5.jpg" alt="IRO Workshop 5" loading="lazy"></div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- EDUCATION -->
<div style="max-width:1200px; margin:0 auto; padding:0 2rem;">
  <div class="full-divider" style="padding:0;"></div>
</div>
<section id="education">
  <div class="section-label">Academic Background</div>
  <h2>My <span>Education</span></h2>
  <div class="edu-grid">
    <div class="edu-card">
      <div class="edu-degree">Bachelor of Engineering Technology (Automation and Robotics) with Honours</div>
      <div class="edu-school">UniKL Malaysia France Institute</div>
      <div class="edu-period">Mar 2024 – Mar 2027 · Ongoing</div>
      <div class="edu-note">Active member &amp; Head of Mechanical Team, Robotique Society — ABU Robocon Malaysia 2025.</div>
    </div>
    <div class="edu-card">
      <div class="edu-degree">Diploma of Manufacturing Engineering (Automation and Robotics)</div>
      <div class="edu-school">Kolej Kemahiran Tinggi MARA Kuantan</div>
      <div class="edu-period">Sep 2020 – Sep 2023 · Completed</div>
      <div class="edu-note">Foundation of passion in automation, robotics, and manufacturing systems — launched hands-on technical journey.</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<div style="max-width:1200px; margin:0 auto; padding:0 2rem;">
  <div class="full-divider" style="padding:0;"></div>
</div>
<section id="contact">
  <div class="section-label">Contact</div>
  <h2>Let's <span>Connect</span></h2>
  <div class="contact-inner">
    <div>
      <p class="contact-title">Open to <em>Engineer</em><br>roles &amp; internships.</p>
      <p class="contact-sub">Looking for opportunities in automation engineering, robotics, embedded systems, or IoT — anywhere in Malaysia or beyond.</p>
    </div>
    <div>
      <ul class="contact-list">
        <li>
          <div class="contact-icon">📧</div>
          <a href="mailto:020husin.hamdan@gmail.com">020husin.hamdan@gmail.com</a>
        </li>
        <li>
          <div class="contact-icon">📱</div>
          <a href="tel:+60193778534">+60 19-377 8534</a>
        </li>
        <li>
          <div class="contact-icon">📍</div>
          <span>Banting, Selangor, Malaysia</span>
        </li>
      </ul>
    </div>
  </div>
</section>

<footer>
  Designed &amp; built for <span>Husin Bin Hamdan</span> · Automation &amp; Robotics Engineer · <span>2026</span>
</footer>

<script>
// ── Gallery Lightbox (GitHub-hosted images, no localStorage) ────────────────
var _lbImages = [];
var _lbIndex  = 0;

function openLightbox(src, caption, gridId, index) {
  var grid = document.getElementById(gridId);
  if (grid) {
    _lbImages = Array.from(grid.querySelectorAll('.gallery-thumb')).map(function(t) {
      return { src: t.querySelector('img').src, caption: t.querySelector('img').alt };
    });
  } else {
    _lbImages = [{ src: src, caption: caption }];
  }
  _lbIndex = index;
  showLightboxSlide();
  document.getElementById('lightbox').classList.add('open');
  document.body.style.overflow = 'hidden';
}

function showLightboxSlide() {
  var frame = _lbImages[_lbIndex];
  document.getElementById('lb-img').src = frame.src;
  document.getElementById('lb-caption').textContent =
    (_lbIndex + 1) + ' / ' + _lbImages.length + '  —  ' + frame.caption;
}

function lbNext() {
  if (_lbImages.length > 1) { _lbIndex = (_lbIndex + 1) % _lbImages.length; showLightboxSlide(); }
}
function lbPrev() {
  if (_lbImages.length > 1) { _lbIndex = (_lbIndex - 1 + _lbImages.length) % _lbImages.length; showLightboxSlide(); }
}

function closeLightbox(e) {
  var lb = document.getElementById('lightbox');
  if (!e || e.target === lb || (e.currentTarget && e.currentTarget.classList.contains('lightbox-close'))) {
    lb.classList.remove('open');
    document.getElementById('lb-img').src = '';
    document.body.style.overflow = '';
  }
}

document.addEventListener('DOMContentLoaded', function() {
  var lb = document.getElementById('lightbox');
  if (lb) lb.addEventListener('click', function(e) { if (e.target === this) closeLightbox(e); });
});

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape')      closeLightbox();
  if (e.key === 'ArrowRight')  lbNext();
  if (e.key === 'ArrowLeft')   lbPrev();
});
</script>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <button class="lightbox-close" onclick="closeLightbox(event)">&#10005;</button>
  <img id="lb-img" class="lightbox-img" src="" alt="">
  <div class="lightbox-nav">
    <button onclick="lbPrev()">&#8592; Prev</button>
    <button onclick="lbNext()">Next &#8594;</button>
  </div>
  <div class="lightbox-caption" id="lb-caption"></div>
</div>


</body>
</html>
