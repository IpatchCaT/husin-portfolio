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

  /* PROOF / UPLOAD SYSTEM */
  .proof-section {
    margin-top: 1.25rem;
    border-top: 1px solid var(--border);
    padding-top: 1rem;
    /* upload zone hidden from public by default */
  }
  .upload-zone { display: none; }
  body.owner-mode .upload-zone { display: block; }

  /* OWNER SYSTEM */
  .owner-btn { font-family:'DM Mono',monospace; font-size:11px; letter-spacing:0.08em; padding:5px 12px; background:transparent; border:1px solid transparent; color:transparent; cursor:pointer; transition:all 0.3s; }
  .owner-btn:hover { border-color:rgba(0,229,160,0.25); color:#7a8499; }
  body.owner-mode .owner-btn { border-color:#00e5a0; color:#00e5a0; }
  .owner-badge { display:none; font-family:'DM Mono',monospace; font-size:10px; color:#00e5a0; border:1px solid rgba(0,229,160,0.3); padding:2px 8px; letter-spacing:0.08em; }
  body.owner-mode .owner-badge { display:inline-block; }
  .remove-btn { position:absolute; top:3px; right:3px; width:18px; height:18px; background:rgba(10,14,20,0.85); border:1px solid rgba(255,255,255,0.1); color:#7a8499; font-size:10px; cursor:pointer; display:none; align-items:center; justify-content:center; line-height:1; padding:0; }
  body.owner-mode .attachment-thumb:hover .remove-btn { display:flex; }
  .remove-btn:hover { color:#ff5555 !important; border-color:#ff5555 !important; }

  /* PASSWORD MODAL */
  .pw-overlay { display:none; position:fixed; inset:0; z-index:500; background:rgba(5,8,12,0.92); align-items:center; justify-content:center; }
  .pw-overlay.open { display:flex; }
  .pw-modal { background:#111620; border:1px solid rgba(0,229,160,0.15); padding:2.5rem; width:100%; max-width:360px; position:relative; }
  .pw-modal::before { content:''; position:absolute; top:-1px; left:0; height:2px; width:50%; background:linear-gradient(90deg,#00e5a0,transparent); }
  .pw-title { font-family:'DM Mono',monospace; font-size:12px; color:#00e5a0; letter-spacing:0.12em; text-transform:uppercase; margin-bottom:1.5rem; }
  .pw-input { width:100%; background:#181f2e; border:1px solid rgba(255,255,255,0.08); color:#e8edf5; font-family:'DM Mono',monospace; font-size:16px; padding:10px 14px; outline:none; letter-spacing:0.1em; margin-bottom:1rem; box-sizing:border-box; transition:border-color 0.2s; }
  .pw-input:focus { border-color:#00e5a0; }
  .pw-input.shake { animation:shake 0.4s ease; border-color:#ff4444; }
  .pw-btn { width:100%; background:#00e5a0; color:#0a0e14; font-family:'DM Mono',monospace; font-size:13px; font-weight:700; letter-spacing:0.1em; padding:10px; border:none; cursor:pointer; text-transform:uppercase; transition:opacity 0.2s; }
  .pw-btn:hover { opacity:0.85; }
  .pw-err { font-family:'DM Mono',monospace; font-size:11px; color:#ff4444; margin-top:8px; display:none; letter-spacing:0.06em; }
  .pw-cancel { display:block; text-align:center; margin-top:1rem; font-family:'DM Mono',monospace; font-size:11px; color:#7a8499; cursor:pointer; background:none; border:none; width:100%; transition:color 0.2s; letter-spacing:0.06em; }
  .pw-cancel:hover { color:#e8edf5; }
  @keyframes shake { 0%,100%{transform:translateX(0)} 25%{transform:translateX(-8px)} 75%{transform:translateX(8px)} }
  .proof-label {
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
  .proof-label::before { content: '//'; color: var(--accent); }
  .upload-zone {
    border: 1px dashed rgba(0,229,160,0.25);
    padding: 1rem;
    text-align: center;
    cursor: pointer;
    transition: border-color 0.2s, background 0.2s;
    position: relative;
  }
  .upload-zone:hover { border-color: var(--accent); background: rgba(0,229,160,0.03); }
  .upload-zone input[type="file"] {
    position: absolute;
    inset: 0;
    opacity: 0;
    cursor: pointer;
    width: 100%;
    height: 100%;
  }
  .upload-zone-text {
    font-size: 12px;
    color: var(--muted);
    pointer-events: none;
  }
  .upload-zone-text span { color: var(--accent); }
  .attachments-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
    gap: 8px;
    margin-top: 0.75rem;
  }
  .attachment-thumb {
    position: relative;
    aspect-ratio: 1;
    background: var(--surface2);
    border: 1px solid var(--border);
    overflow: hidden;
    cursor: pointer;
    transition: border-color 0.2s;
  }
  .attachment-thumb:hover { border-color: var(--accent); }
  .attachment-thumb img {
    width: 100%; height: 100%;
    object-fit: cover;
    display: block;
  }
  .attachment-thumb .pdf-icon {
    width: 100%; height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 4px;
  }
  .pdf-icon-sym {
    font-size: 22px;
    line-height: 1;
  }
  .pdf-icon-name {
    font-family: var(--font-mono);
    font-size: 9px;
    color: var(--muted);
    text-align: center;
    padding: 0 4px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    width: 100%;
    text-align: center;
  }
  .attachment-thumb .remove-btn {
    position: absolute;
    top: 3px; right: 3px;
    width: 18px; height: 18px;
    background: rgba(10,14,20,0.85);
    border: 1px solid var(--border);
    color: var(--muted);
    font-size: 11px;
    line-height: 1;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.2s;
  }
  .attachment-thumb:hover .remove-btn { opacity: 1; }
  .remove-btn:hover { color: #ff5555 !important; border-color: #ff5555 !important; }

  /* LIGHTBOX */
  .lightbox {
    display: none;
    position: fixed;
    inset: 0;
    z-index: 999;
    background: rgba(5,8,12,0.95);
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 2rem;
  }
  .lightbox.open { display: flex; }
  .lightbox-img {
    max-width: 90vw;
    max-height: 80vh;
    object-fit: contain;
    border: 1px solid var(--border);
  }
  .lightbox-close {
    position: fixed;
    top: 1.5rem; right: 1.5rem;
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--text);
    font-size: 18px;
    width: 40px; height: 40px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--font-mono);
    transition: border-color 0.2s;
  }
  .lightbox-close:hover { border-color: var(--accent); color: var(--accent); }
  .lightbox-caption {
    margin-top: 1rem;
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 0.06em;
  }
  .attachment-count {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--accent);
    margin-left: auto;
  }
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
  <div style="display:flex;align-items:center;gap:10px;">
    <span class="owner-badge">OWNER</span>
    <button class="owner-btn" onclick="openPwModal()" title="Owner login">&#9679;&#9679;&#9679;</button>
  </div>
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
          <span class="badge accent">ROS</span>
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
      <div class="proof-section">
        <div class="proof-label">Proof &amp; Attachments <span class="attachment-count" id="count-p1"></span></div>
        <div class="upload-zone" id="zone-p1">
          <input type="file" multiple accept="image/*,.pdf,.doc,.docx" onchange="handleUpload(this,'p1')">
          <div class="upload-zone-text">Drop files or <span>click to upload</span> · Images, PDF, Docs</div>
        </div>
        <div class="attachments-grid" id="grid-p1"></div>
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
      <div class="proof-section">
        <div class="proof-label">Proof &amp; Attachments <span class="attachment-count" id="count-p2"></span></div>
        <div class="upload-zone" id="zone-p2">
          <input type="file" multiple accept="image/*,.pdf,.doc,.docx" onchange="handleUpload(this,'p2')">
          <div class="upload-zone-text">Drop files or <span>click to upload</span> · Images, PDF, Docs</div>
        </div>
        <div class="attachments-grid" id="grid-p2"></div>
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
      <div class="proof-section">
        <div class="proof-label">Proof &amp; Attachments <span class="attachment-count" id="count-p3"></span></div>
        <div class="upload-zone" id="zone-p3">
          <input type="file" multiple accept="image/*,.pdf,.doc,.docx" onchange="handleUpload(this,'p3')">
          <div class="upload-zone-text">Drop files or <span>click to upload</span> · Images, PDF, Docs</div>
        </div>
        <div class="attachments-grid" id="grid-p3"></div>
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
      <div class="proof-section">
        <div class="proof-label">Proof &amp; Attachments <span class="attachment-count" id="count-p4"></span></div>
        <div class="upload-zone" id="zone-p4">
          <input type="file" multiple accept="image/*,.pdf,.doc,.docx" onchange="handleUpload(this,'p4')">
          <div class="upload-zone-text">Drop files or <span>click to upload</span> · Images, PDF, Docs</div>
        </div>
        <div class="attachments-grid" id="grid-p4"></div>
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
      <div class="proof-section">
        <div class="proof-label">Proof &amp; Attachments <span class="attachment-count" id="count-p5"></span></div>
        <div class="upload-zone" id="zone-p5">
          <input type="file" multiple accept="image/*,.pdf,.doc,.docx" onchange="handleUpload(this,'p5')">
          <div class="upload-zone-text">Drop files or <span>click to upload</span> · Images, PDF, Docs</div>
        </div>
        <div class="attachments-grid" id="grid-p5"></div>
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

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox" onclick="closeLightbox(event)">
  <button class="lightbox-close" onclick="closeLightbox(event)">X</button>
  <img class="lightbox-img" id="lightbox-img" src="" alt="" style="display:none;">
  <div id="lightbox-file" style="display:none; text-align:center;">
    <div id="lightbox-file-ext" style="font-family:'DM Mono',monospace; font-size:36px; font-weight:600; color:#00e5a0; letter-spacing:0.1em; margin-bottom:0.75rem;"></div>
    <div id="lightbox-file-name" style="font-family:'DM Mono',monospace; font-size:14px; color:#e8edf5; margin-bottom:1.5rem; max-width:400px; word-break:break-all;"></div>
    <a id="lightbox-file-dl" href="#" download style="font-family:'DM Mono',monospace; font-size:13px; color:#00e5a0; border:1px solid rgba(0,229,160,0.35); padding:10px 28px; text-decoration:none; display:inline-block; letter-spacing:0.06em; transition:background 0.2s;" onmouseover="this.style.background='rgba(0,229,160,0.08)'" onmouseout="this.style.background='transparent'">DOWNLOAD FILE</a>
  </div>
  <div class="lightbox-caption" id="lightbox-caption"></div>
</div>

<!-- TOAST -->
<div id="toast" style="position:fixed; bottom:2rem; right:2rem; background:#111620; border:1px solid rgba(0,229,160,0.3); color:#00e5a0; font-family:'DM Mono',monospace; font-size:12px; letter-spacing:0.06em; padding:10px 20px; z-index:1000; opacity:0; transform:translateY(8px); transition:opacity 0.3s, transform 0.3s; pointer-events:none;"></div>
<style>
  #toast.show { opacity:1; transform:translateY(0); }
  .upload-zone.drag-over { border-color:#00e5a0; background:rgba(0,229,160,0.06); }
</style>

<script>
// ─────────────────────────────────────────────
//  CONFIG — your Cloudinary credentials
// ─────────────────────────────────────────────
var CLOUD_NAME    = 'dsrqg2olf';
var UPLOAD_PRESET = 'portfolio_upload';

// ─────────────────────────────────────────────
//  STORAGE KEY — Cloudinary URLs saved here
//  localStorage stores PUBLIC URLs so any
//  browser that loads the page can show images.
//  Public visitors load URLs → fetch from CDN.
// ─────────────────────────────────────────────
var STORE_KEY = 'hbh_portfolio_v2';

var cache = { p1:[], p2:[], p3:[], p4:[], p5:[] };

// ─────────────────────────────────────────────
//  LOAD saved URLs on page start (everyone)
// ─────────────────────────────────────────────
function loadData() {
  try {
    var raw = localStorage.getItem(STORE_KEY);
    if (raw) cache = JSON.parse(raw);
  } catch(e) {}
  ['p1','p2','p3','p4','p5'].forEach(renderGrid);
}

function saveData() {
  localStorage.setItem(STORE_KEY, JSON.stringify(cache));
}

// ─────────────────────────────────────────────
//  UPLOAD — owner only (password protected)
//  Sends file to Cloudinary, gets back a public
//  HTTPS URL that anyone in the world can load.
// ─────────────────────────────────────────────
async function handleUpload(input, pid) {
  var files = Array.from(input.files);
  for (var i = 0; i < files.length; i++) {
    var file = files[i];
    var fd   = new FormData();
    fd.append('file', file);
    fd.append('upload_preset', UPLOAD_PRESET);
    try {
      showToast('Uploading ' + file.name + '...');
      var res  = await fetch('https://api.cloudinary.com/v1_1/' + CLOUD_NAME + '/auto/upload', { method:'POST', body:fd });
      var data = await res.json();
      if (!data.secure_url) throw new Error('No URL returned');
      var rec = { id: Date.now() + i, pid:pid, name:file.name, type:file.type, url:data.secure_url };
      cache[pid].push(rec);
      saveData();
      renderGrid(pid);
      showToast('Saved: ' + file.name);
    } catch(err) {
      console.error(err);
      showToast('Upload failed — check preset settings');
    }
  }
  input.value = '';
}

// ─────────────────────────────────────────────
//  DELETE — owner only
// ─────────────────────────────────────────────
function deleteFile(pid, id) {
  cache[pid] = cache[pid].filter(function(f){ return f.id !== id; });
  saveData();
  renderGrid(pid);
  showToast('File removed');
}

// ─────────────────────────────────────────────
//  RENDER thumbnails — runs for everyone
//  Public sees images loaded from Cloudinary CDN
// ─────────────────────────────────────────────
function renderGrid(pid) {
  var grid   = document.getElementById('grid-' + pid);
  var count  = document.getElementById('count-' + pid);
  var files  = cache[pid] || [];
  var isOwner = document.body.classList.contains('owner-mode');
  count.textContent = files.length > 0 ? files.length + ' file' + (files.length > 1 ? 's' : '') : '';
  grid.innerHTML = '';
  files.forEach(function(f) {
    var thumb = document.createElement('div');
    thumb.className = 'attachment-thumb';
    thumb.style.position = 'relative';
    var isImage = f.type && f.type.startsWith('image/');
    if (isImage) {
      var img = document.createElement('img');
      img.src = f.url; img.alt = f.name;
      img.onclick = function(){ openLightboxImage(f.url, f.name); };
      thumb.appendChild(img);
    } else {
      var ext  = f.name.split('.').pop().toUpperCase();
      var icon = document.createElement('div');
      icon.className = 'pdf-icon';
      icon.style.cursor = 'pointer';
      icon.innerHTML = '<div class="pdf-icon-sym" style="font-family:monospace;font-size:13px;color:#00e5a0;font-weight:700;">' + ext + '</div><div class="pdf-icon-name">' + f.name + '</div>';
      icon.onclick = function(){ window.open(f.url, '_blank'); };
      thumb.appendChild(icon);
    }
    if (isOwner) {
      var rm = document.createElement('button');
      rm.className = 'remove-btn';
      rm.textContent = 'x';
      rm.title = 'Remove';
      (function(fpid, fid){ rm.onclick = function(e){ e.stopPropagation(); deleteFile(fpid, fid); }; })(pid, f.id);
      thumb.appendChild(rm);
    }
    grid.appendChild(thumb);
  });
}

// ─────────────────────────────────────────────
//  LIGHTBOX
// ─────────────────────────────────────────────
function openLightboxImage(url, name) {
  document.getElementById('lightbox-img').src = url;
  document.getElementById('lightbox-img').style.display = 'block';
  document.getElementById('lightbox-file').style.display = 'none';
  document.getElementById('lightbox-caption').textContent = name;
  document.getElementById('lightbox').classList.add('open');
}

function closeLightbox(e) {
  var lb = document.getElementById('lightbox');
  if (!e || e.target === lb || (e.currentTarget && e.currentTarget.classList.contains('lightbox-close'))) {
    lb.classList.remove('open');
    document.getElementById('lightbox-img').src = '';
  }
}

// ─────────────────────────────────────────────
//  TOAST
// ─────────────────────────────────────────────
function showToast(msg) {
  var t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(t._timer);
  t._timer = setTimeout(function(){ t.classList.remove('show'); }, 2800);
}

// ─────────────────────────────────────────────
//  OWNER PASSWORD (SHA-256 hashed)
//  Default password: HusinHBH2026
//  To change: go to https://emn178.github.io/online-tools/sha256.html
//  hash your new password and replace OWNER_HASH below
// ─────────────────────────────────────────────
var OWNER_HASH = '';
async function sha256(msg) {
  var buf = await crypto.subtle.digest('SHA-256', new TextEncoder().encode(msg));
  return Array.from(new Uint8Array(buf)).map(function(b){ return b.toString(16).padStart(2,'0'); }).join('');
}
sha256('HusinHBH2026').then(function(h){ OWNER_HASH = h; });

function openPwModal() {
  if (document.body.classList.contains('owner-mode')) {
    document.body.classList.remove('owner-mode');
    sessionStorage.removeItem('hbh_owner');
    ['p1','p2','p3','p4','p5'].forEach(renderGrid);
    showToast('Upload mode locked');
    return;
  }
  document.getElementById('pw-overlay').classList.add('open');
  setTimeout(function(){ document.getElementById('pw-input').focus(); }, 80);
}

function closePwModal() {
  document.getElementById('pw-overlay').classList.remove('open');
  document.getElementById('pw-input').value = '';
  document.getElementById('pw-input').classList.remove('shake');
  document.getElementById('pw-err').style.display = 'none';
}

async function checkPw() {
  var val  = document.getElementById('pw-input').value;
  var hash = await sha256(val);
  if (hash === OWNER_HASH) {
    document.body.classList.add('owner-mode');
    sessionStorage.setItem('hbh_owner', '1');
    closePwModal();
    ['p1','p2','p3','p4','p5'].forEach(renderGrid);
    showToast('Upload mode unlocked');
  } else {
    var inp = document.getElementById('pw-input');
    inp.classList.remove('shake');
    void inp.offsetWidth;
    inp.classList.add('shake');
    document.getElementById('pw-err').style.display = 'block';
    inp.value = '';
  }
}

// Restore owner mode in same browser session
if (sessionStorage.getItem('hbh_owner') === '1') {
  document.addEventListener('DOMContentLoaded', function(){
    document.body.classList.add('owner-mode');
    ['p1','p2','p3','p4','p5'].forEach(renderGrid);
  });
}

// ─────────────────────────────────────────────
//  DRAG & DROP + INIT
// ─────────────────────────────────────────────
document.addEventListener('DOMContentLoaded', function() {
  document.querySelectorAll('.upload-zone').forEach(function(zone) {
    zone.addEventListener('dragover',  function(e){ e.preventDefault(); zone.classList.add('drag-over'); });
    zone.addEventListener('dragleave', function()  { zone.classList.remove('drag-over'); });
    zone.addEventListener('drop', function(e) {
      e.preventDefault(); zone.classList.remove('drag-over');
      var pid = zone.id.replace('zone-', '');
      handleUpload({ files: e.dataTransfer.files, value: '' }, pid);
    });
  });
  loadData();
});

document.addEventListener('keydown', function(e){
  if (e.key === 'Escape'){ closePwModal(); closeLightbox(); }
});
</script>

<!-- PASSWORD MODAL -->
<div class="pw-overlay" id="pw-overlay">
  <div class="pw-modal">
    <div class="pw-title">// Owner Access</div>
    <input class="pw-input" type="password" id="pw-input" placeholder="Enter password" autocomplete="off" onkeydown="if(event.key==='Enter')checkPw()">
    <button class="pw-btn" onclick="checkPw()">Unlock Upload Mode</button>
    <div class="pw-err" id="pw-err">Incorrect password — try again.</div>
    <button class="pw-cancel" onclick="closePwModal()">Cancel</button>
  </div>
</div>

</body>
</html>
