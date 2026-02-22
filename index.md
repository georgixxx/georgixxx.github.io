<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Brightone Onyango — Technical Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy:       #002b5c;
      --blue:       #004a99;
      --blue-light: #eef4fb;
      --blue-border:#d0e1f2;
      --sidebar-bg: #f0f4f8;
      --white:      #ffffff;
      --text:       #1a1a2e;
      --muted:      #556070;
      --accent:     #c8a84b;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'IBM Plex Sans', sans-serif;
      background: #e8edf3;
      color: var(--text);
      min-height: 100vh;
      padding: 40px 20px;
    }

    /* ── WRAPPER ─────────────────────────────────── */
    .portfolio-wrapper {
      display: flex;
      gap: 36px;
      max-width: 1200px;
      margin: 0 auto;
      align-items: flex-start;
    }

    /* ── SIDEBAR ─────────────────────────────────── */
    .sidebar {
      flex: 0 0 280px;
      position: sticky;
      top: 40px;
      background: var(--sidebar-bg);
      border-radius: 16px;
      border-top: 6px solid var(--blue);
      padding: 30px 24px;
      box-shadow: 0 8px 32px rgba(0,43,92,0.10);
      animation: fadeInLeft 0.7s ease both;
    }

    @keyframes fadeInLeft {
      from { opacity:0; transform: translateX(-24px); }
      to   { opacity:1; transform: translateX(0); }
    }

    .sidebar-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.35em;
      color: var(--navy);
      margin-bottom: 18px;
      line-height: 1.2;
    }

    .profile-pic-wrap {
      width: 100%;
      aspect-ratio: 1;
      border-radius: 50%;
      overflow: hidden;
      border: 4px solid var(--blue);
      margin-bottom: 18px;
      background: var(--blue-light);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .profile-pic-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* Placeholder shown when image is missing */
    .profile-placeholder {
      width: 100%;
      aspect-ratio: 1;
      border-radius: 50%;
      border: 4px solid var(--blue);
      margin-bottom: 18px;
      background: var(--blue-light);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--blue);
      font-size: 0.8em;
      font-family: 'IBM Plex Mono', monospace;
      text-align: center;
      line-height: 1.5;
    }

    .sidebar-title {
      font-size: 0.88em;
      font-weight: 600;
      color: var(--muted);
      margin-bottom: 26px;
      letter-spacing: 0.02em;
    }

    .sidebar-section {
      margin-bottom: 22px;
    }

    .sidebar-section h3 {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.75em;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--blue);
      border-bottom: 2px solid var(--blue);
      padding-bottom: 5px;
      margin-bottom: 10px;
    }

    .sidebar-section p,
    .sidebar-section li {
      font-size: 0.9em;
      line-height: 1.6;
      color: var(--text);
    }

    .sidebar-section ul {
      padding-left: 16px;
    }

    .sidebar-section a {
      display: block;
      font-size: 0.9em;
      font-weight: 600;
      color: var(--blue);
      text-decoration: none;
      line-height: 2;
      transition: color 0.2s;
    }

    .sidebar-section a:hover { color: var(--accent); }

    /* ── MAIN CONTENT ────────────────────────────── */
    .main-content {
      flex: 1;
      min-width: 0;
      animation: fadeInRight 0.7s ease both;
    }

    @keyframes fadeInRight {
      from { opacity:0; transform: translateX(24px); }
      to   { opacity:1; transform: translateX(0); }
    }

    .main-content h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.6em;
      color: var(--navy);
      border-bottom: 2px solid #d4dce8;
      padding-bottom: 14px;
      margin-bottom: 20px;
    }

    .intro-text {
      font-size: 1.05em;
      line-height: 1.75;
      color: var(--muted);
      margin-bottom: 40px;
    }

    .intro-text strong { color: var(--navy); }

    .section-heading {
      font-family: 'Playfair Display', serif;
      font-size: 1.6em;
      color: var(--blue);
      margin-bottom: 20px;
      margin-top: 44px;
    }

    /* ── PROJECT CARD ────────────────────────────── */
    .project-card {
      background: var(--white);
      border-left: 6px solid var(--blue);
      border-radius: 0 12px 12px 0;
      padding: 30px;
      box-shadow: 0 4px 18px rgba(0,43,92,0.07);
      margin-bottom: 36px;
      transition: box-shadow 0.25s, transform 0.25s;
    }

    .project-card:hover {
      box-shadow: 0 8px 32px rgba(0,74,153,0.14);
      transform: translateY(-2px);
    }

    .project-card h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.4em;
      color: var(--navy);
      margin-bottom: 6px;
    }

    .stack-label {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.82em;
      font-weight: 500;
      color: var(--blue);
      margin-bottom: 14px;
      letter-spacing: 0.03em;
    }

    .project-card p {
      font-size: 0.97em;
      line-height: 1.7;
      color: var(--muted);
      margin-bottom: 18px;
    }

    /* Architecture diagram placeholder */
    .arch-diagram {
      width: 100%;
      border-radius: 8px;
      border: 1px solid var(--blue-border);
      margin: 16px 0 6px;
      overflow: hidden;
      background: var(--blue-light);
      min-height: 160px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .arch-diagram img {
      width: 100%;
      border-radius: 8px;
      display: block;
    }

    .arch-diagram-placeholder {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.82em;
      color: var(--blue);
      text-align: center;
      padding: 40px;
      line-height: 1.6;
    }

    .diagram-caption {
      font-size: 0.82em;
      font-style: italic;
      color: #888;
      text-align: center;
      margin-bottom: 22px;
    }

    .impact-heading {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.8em;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--navy);
      margin-bottom: 10px;
    }

    .impact-list {
      list-style: none;
      padding: 0;
      margin-bottom: 24px;
    }

    .impact-list li {
      font-size: 0.93em;
      line-height: 1.65;
      color: var(--text);
      padding-left: 20px;
      position: relative;
      margin-bottom: 6px;
    }

    .impact-list li::before {
      content: '▸';
      color: var(--accent);
      position: absolute;
      left: 0;
    }

    .card-actions {
      display: flex;
      gap: 16px;
      align-items: center;
      flex-wrap: wrap;
    }

    .btn-primary {
      background: var(--blue);
      color: #fff;
      padding: 11px 22px;
      border-radius: 6px;
      text-decoration: none;
      font-weight: 600;
      font-size: 0.88em;
      transition: background 0.2s;
    }

    .btn-primary:hover { background: var(--navy); }

    .btn-link {
      color: var(--blue);
      font-weight: 600;
      font-size: 0.88em;
      text-decoration: underline;
      transition: color 0.2s;
    }

    .btn-link:hover { color: var(--accent); }

    /* Upcoming badge */
    .upcoming-badge {
      display: inline-block;
      background: var(--accent);
      color: var(--navy);
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.72em;
      font-weight: 500;
      padding: 3px 10px;
      border-radius: 20px;
      margin-left: 10px;
      vertical-align: middle;
      letter-spacing: 0.05em;
    }

    /* ── METHODOLOGY GRID ────────────────────────── */
    .methodology-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-bottom: 50px;
      margin-top: 8px;
    }

    .method-card {
      background: var(--blue-light);
      border: 1px solid var(--blue-border);
      border-radius: 12px;
      padding: 22px 18px;
      text-align: center;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .method-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(0,74,153,0.12);
    }

    .method-card strong {
      display: block;
      color: var(--blue);
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.85em;
      letter-spacing: 0.05em;
      margin-bottom: 8px;
      text-transform: uppercase;
    }

    .method-card span {
      font-size: 0.88em;
      color: var(--muted);
      line-height: 1.5;
    }

    /* ── RESPONSIVE ──────────────────────────────── */
    @media (max-width: 768px) {
      .portfolio-wrapper { flex-direction: column; }
      .sidebar { position: static; flex: none; width: 100%; }
      .methodology-grid { grid-template-columns: 1fr; }
      .main-content h1 { font-size: 1.9em; }
    }
  </style>
</head>
<body>

<div class="portfolio-wrapper">

  <!-- ── SIDEBAR ── -->
  <aside class="sidebar">
    <h2 class="sidebar-name">Brightone Onyango</h2>

    <!--
      Place your photo at: assets/profile-pic.png
      The placeholder below will show until the image is added.
    -->
    <div class="profile-placeholder" id="profileWrap">
      profile-pic.png<br>(assets/)
    </div>

    <p class="sidebar-title">Data Automation Specialist &amp;<br>Technical Writer</p>

    <div class="sidebar-section">
      <h3>Education</h3>
      <p><strong>BSc. Computer Science</strong><br>Chuka University</p>
    </div>

    <div class="sidebar-section">
      <h3>Certifications</h3>
      <ul>
        <li>n8n Certified Professional</li>
        <li>Certified Data Annotator</li>
      </ul>
    </div>

    <div class="sidebar-section">
      <h3>Contact</h3>
      <a href="https://www.linkedin.com/in/brightone-onyango-109614263" target="_blank">LinkedIn</a>
      <a href="mailto:georgebrixomuga@gmail.com">Email</a>
      <a href="https://georgixxx.github.io" target="_blank">Portfolio Hub</a>
    </div>
  </aside>

  <!-- ── MAIN CONTENT ── -->
  <main class="main-content">

    <h1>Technical Portfolio</h1>

    <p class="intro-text">
      Welcome to my portfolio! I specialise in engineering high-integrity data pipelines.
      Each project is open source and designed with a focus on
      <strong>Accuracy, Clarity, and Traceability</strong>.
    </p>

    <h2 class="section-heading">Featured Projects</h2>

    <!-- Project 1 -->
    <div class="project-card">
      <h3>1. Automated Data Validation Pipeline</h3>
      <p class="stack-label">Stack: n8n · Python · JSON Schema</p>

      <p>
        A production-ready implementation of data integrity layers for automated workflows.
        It intercepts incoming JSON payloads via Webhooks and validates them against a strict
        JSON Schema before routing to the appropriate downstream path.
      </p>

      <!--
        Place your architecture diagram at: assets/architecture diagram.png
        The placeholder below will swap for the image automatically.
      -->
      <div class="arch-diagram" id="archDiagram">
        <img
          src="assets/architecture diagram.png"
          alt="High-level system architecture"
          onerror="this.parentElement.innerHTML='<div class=\'arch-diagram-placeholder\'>[ architecture diagram.png ]<br><small>Place image in assets/ folder</small></div>'"
        />
      </div>
      <p class="diagram-caption">
        Figure 1: High-level system architecture showing the flow from ingestion to final routing.
      </p>

      <p class="impact-heading">Business Impact</p>
      <ul class="impact-list">
        <li><strong>Reliability:</strong> Reduces database corruption by ensuring 100% schema compliance.</li>
        <li><strong>Efficiency:</strong> Eliminates manual data cleaning, allowing teams to focus on core tasks.</li>
        <li><strong>Traceability:</strong> Establishes a transparent audit trail for every rejected payload.</li>
      </ul>

      <div class="card-actions">
        <a class="btn-primary" href="https://github.com/georgixxx/n8n-json-validation-pipeline" target="_blank">View GitHub Repo</a>
        <a class="btn-link" href="https://github.com/georgixxx/n8n-json-validation-pipeline/blob/main/README.md" target="_blank">Full Project Documentation</a>
      </div>
    </div>

    <!-- Project 2 -->
    <div class="project-card">
      <h3>
        2. Python Data Analysis Dashboard
        <span class="upcoming-badge">Upcoming</span>
      </h3>
      <p class="stack-label">Stack: Python · Pandas · Matplotlib</p>
      <p>
        Utilising Pandas and Matplotlib to transform validated logs into actionable KPI dashboards
        and automated growth trend visualisations.
      </p>
    </div>

    <!-- Methodology -->
    <h2 class="section-heading">Technical Methodology</h2>
    <div class="methodology-grid">
      <div class="method-card">
        <strong>Ingestion</strong>
        <span>REST API Webhooks for decoupling sources.</span>
      </div>
      <div class="method-card">
        <strong>Validation</strong>
        <span>JSON Schema Draft 07 &amp; Python logic.</span>
      </div>
      <div class="method-card">
        <strong>Routing</strong>
        <span>Success storage vs. real-time error alerts.</span>
      </div>
    </div>

  </main>
</div>

</body>
</html>
