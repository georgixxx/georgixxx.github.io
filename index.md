---
layout: null
---
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Brightone Onyango - Technical Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy:  #002b5c;
      --blue:  #004a99;
      --light: #f5f7fa;
      --white: #ffffff;
      --text:  #1a1a2e;
      --muted: #556070;
      --border:#dde3ec;
    }

    body {
      font-family: 'IBM Plex Sans', sans-serif;
      background: var(--white);
      color: var(--text);
      min-height: 100vh;
    }

    .layout {
      display: grid;
      grid-template-columns: 300px 1fr;
      min-height: 100vh;
    }

    /* LEFT SIDEBAR */
    .sidebar {
      background: var(--light);
      border-right: 1px solid var(--border);
      padding: 48px 28px;
      position: sticky;
      top: 0;
      height: 100vh;
      overflow-y: auto;
    }

    .sidebar h1 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5em;
      color: var(--blue);
      margin-bottom: 22px;
      line-height: 1.25;
    }

    .profile-img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      overflow: hidden;
      border: 3px solid var(--blue);
      margin-bottom: 22px;
      background: #dce8f5;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .profile-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .placeholder-text {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.72em;
      color: var(--blue);
      text-align: center;
      line-height: 1.6;
      padding: 10px;
    }

    .sidebar-role {
      font-size: 0.9em;
      color: var(--muted);
      margin-bottom: 28px;
      line-height: 1.5;
      text-align: center;
    }

    .sidebar-section { margin-bottom: 26px; }

    .sidebar-section h3 {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.72em;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--blue);
      border-bottom: 1px solid var(--border);
      padding-bottom: 5px;
      margin-bottom: 10px;
    }

    .sidebar-section p { font-size: 0.9em; line-height: 1.6; }

    .sidebar-section ul {
      padding-left: 16px;
      font-size: 0.9em;
      line-height: 1.8;
    }

    .sidebar-section a {
      display: block;
      font-size: 0.9em;
      color: var(--blue);
      text-decoration: none;
      line-height: 2;
      font-weight: 500;
    }

    .sidebar-section a:hover { text-decoration: underline; }

    /* RIGHT MAIN */
    .main { padding: 48px 56px; max-width: 860px; }

    .main h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2em;
      color: var(--navy);
      margin-bottom: 20px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 14px;
    }

    .intro {
      font-size: 1em;
      line-height: 1.85;
      color: var(--muted);
      margin-bottom: 16px;
    }

    .intro strong { color: var(--navy); }
    .intro a { color: var(--blue); font-weight: 600; text-decoration: none; }
    .intro a:hover { text-decoration: underline; }

    .intro-block { margin-bottom: 36px; }

    .main h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.45em;
      color: var(--blue);
      margin-bottom: 18px;
      margin-top: 42px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 8px;
    }

    .project-card {
      margin-bottom: 40px;
      padding-bottom: 40px;
      border-bottom: 1px solid var(--border);
    }

    .project-card h3 {
      font-size: 1.1em;
      font-weight: 600;
      color: var(--navy);
      margin-bottom: 4px;
    }

    .stack {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.82em;
      color: var(--blue);
      margin-bottom: 12px;
    }

    .project-card p {
      font-size: 0.97em;
      line-height: 1.75;
      color: var(--muted);
      margin-bottom: 14px;
    }

    /* ARCHITECTURE DIAGRAM */
    .arch-wrap {
      margin: 18px 0 6px;
      border-radius: 8px;
      overflow: hidden;
      border: 1px solid var(--border);
      background: #eef3fb;
      min-height: 140px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: zoom-in;
      position: relative;
    }

    .arch-wrap img {
      width: 100%;
      display: block;
      transition: transform 0.1s ease;
      transform-origin: center center;
    }

    .arch-wrap:hover::after {
      content: "Click to enlarge  |  Scroll to zoom";
      position: absolute;
      bottom: 10px;
      right: 12px;
      background: rgba(0,43,92,0.75);
      color: #fff;
      font-size: 0.72em;
      font-family: 'IBM Plex Mono', monospace;
      padding: 4px 10px;
      border-radius: 4px;
      pointer-events: none;
    }

    .arch-placeholder {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.8em;
      color: var(--blue);
      text-align: center;
      padding: 40px;
      line-height: 1.7;
    }

    .diagram-caption {
      font-size: 0.8em;
      font-style: italic;
      color: #999;
      text-align: center;
      margin-bottom: 18px;
    }

    /* LIGHTBOX */
    .lightbox {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.88);
      z-index: 1000;
      align-items: center;
      justify-content: center;
      cursor: zoom-out;
    }

    .lightbox.active { display: flex; }

    .lightbox-inner {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      overflow: hidden;
    }

    .lightbox img {
      max-width: 90vw;
      max-height: 90vh;
      border-radius: 6px;
      box-shadow: 0 20px 60px rgba(0,0,0,0.6);
      transform-origin: center center;
      transition: transform 0.05s ease;
      cursor: default;
      user-select: none;
    }

    .lightbox-close {
      position: fixed;
      top: 20px;
      right: 28px;
      color: #fff;
      font-size: 2em;
      cursor: pointer;
      line-height: 1;
      z-index: 1001;
      opacity: 0.8;
      font-family: sans-serif;
    }

    .lightbox-close:hover { opacity: 1; }

    .lightbox-hint {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      color: rgba(255,255,255,0.6);
      font-size: 0.8em;
      font-family: 'IBM Plex Mono', monospace;
      pointer-events: none;
    }

    .impact-title {
      font-weight: 600;
      font-size: 0.9em;
      color: var(--navy);
      margin-bottom: 8px;
    }

    .impact-list {
      list-style: disc;
      padding-left: 20px;
      font-size: 0.93em;
      line-height: 1.8;
      color: var(--text);
      margin-bottom: 20px;
    }

    .card-links {
      display: flex;
      gap: 20px;
      align-items: center;
      flex-wrap: wrap;
    }

    .btn {
      background: var(--blue);
      color: #fff;
      padding: 10px 20px;
      border-radius: 5px;
      text-decoration: none;
      font-size: 0.88em;
      font-weight: 600;
      transition: background 0.2s;
    }

    .btn:hover { background: var(--navy); }

    .link {
      color: var(--blue);
      font-size: 0.88em;
      font-weight: 600;
      text-decoration: underline;
    }

    .badge {
      display: inline-block;
      background: #c8a84b;
      color: var(--navy);
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.7em;
      padding: 2px 9px;
      border-radius: 20px;
      margin-left: 8px;
      vertical-align: middle;
    }

    .method-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
      margin-top: 10px;
    }

    .method-card {
      background: #eef3fb;
      border: 1px solid #d0e1f2;
      border-radius: 10px;
      padding: 20px 16px;
      text-align: center;
    }

    .method-card strong {
      display: block;
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.78em;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--blue);
      margin-bottom: 7px;
    }

    .method-card span {
      font-size: 0.87em;
      color: var(--muted);
      line-height: 1.5;
    }

    @media (max-width: 760px) {
      .layout { grid-template-columns: 1fr; }
      .sidebar { position: static; height: auto; }
      .main { padding: 32px 20px; }
      .method-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <span class="lightbox-close" id="lightboxClose">&times;</span>
  <div class="lightbox-inner">
    <img src="assets/architecture diagram.png" alt="Architecture diagram enlarged" id="lightboxImg"/>
  </div>
  <div class="lightbox-hint">Scroll to zoom in and out &nbsp;|&nbsp; Click outside image or press Esc to close</div>
</div>

<div class="layout">

  <!-- LEFT COLUMN -->
  <aside class="sidebar">

    <h1>Brightone Onyango</h1>

    <div class="profile-img">
      <img
        src="assets/profile-pic.png"
        alt="Brightone Onyango"
        onerror="this.style.display='none'; this.parentElement.innerHTML='<div class=\'placeholder-text\'>profile-pic.png<br>(assets/)</div>'"
      />
    </div>

    <p class="sidebar-role">Data Automation Specialist &amp; Technical Writer</p>

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

  <!-- RIGHT COLUMN -->
  <main class="main">

    <h1>Technical Portfolio</h1>

    <div class="intro-block">
      <p class="intro">
        Welcome, and thank you for stopping by! I'm glad you're here.
      </p>
      <p class="intro">
        I specialise in engineering high-integrity data pipelines that make automated workflows
        more reliable, auditable, and production-ready. My work sits at the intersection of
        data automation and technical communication. I don't just build systems; I document
        them clearly so that anyone on your team can understand, maintain, and extend them.
      </p>
      <p class="intro">
        Every project in this portfolio is open source, built from real-world use cases, and
        designed with a firm focus on <strong>Accuracy, Clarity, and Traceability</strong>.
        Whether it's validating incoming data before it ever touches a database, or structuring
        workflows that fail gracefully and log every error, the goal is always the same:
        systems you can trust.
      </p>
      <p class="intro">
        If you find any of these projects useful, whether for your own workflows, a team
        implementation, or simply as a learning reference, I'd love to hear from you.
        Feel free to reach out via
        <a href="mailto:georgebrixomuga@gmail.com">email</a>
        or connect with me on
        <a href="https://www.linkedin.com/in/brightone-onyango-109614263" target="_blank">LinkedIn</a>.
        I'm always open to collaboration, feedback, or just a good conversation about data.
      </p>
    </div>

    <h2>Featured Projects</h2>

    <div class="project-card">
      <h3>1. Automated Data Validation Pipeline</h3>
      <p class="stack">Stack: n8n · Python · JSON Schema</p>
      <p>
        A production-ready implementation of data integrity layers for automated workflows.
        It intercepts incoming JSON payloads via Webhooks and validates them against a strict
        JSON Schema before routing to the appropriate downstream path.
      </p>

      <!-- Clickable + zoomable diagram -->
      <div class="arch-wrap" id="archWrap">
        <img
          src="assets/architecture diagram.png"
          alt="System architecture diagram"
          id="archThumb"
          onerror="this.style.display='none'; this.parentElement.innerHTML='<div class=\'arch-placeholder\'>[ architecture diagram.png ]<br><small>Place image in assets/ folder</small></div>'"
        />
      </div>
      <p class="diagram-caption">Figure 1: High-level system architecture, from ingestion to final routing.</p>

      <p class="impact-title">Business Impact</p>
      <ul class="impact-list">
        <li><strong>Reliability:</strong> Reduces database corruption by ensuring 100% schema compliance.</li>
        <li><strong>Efficiency:</strong> Eliminates manual data cleaning, allowing teams to focus on core tasks.</li>
        <li><strong>Traceability:</strong> Establishes a transparent audit trail for every rejected payload.</li>
      </ul>

      <div class="card-links">
        <a class="btn" href="https://github.com/georgixxx/n8n-json-validation-pipeline" target="_blank">View GitHub Repo</a>
        <a class="link" href="https://github.com/georgixxx/n8n-json-validation-pipeline/blob/main/README.md" target="_blank">Full Project Documentation</a>
      </div>
    </div>

    <div class="project-card">
      <h3>2. Python Data Analysis Dashboard <span class="badge">Upcoming</span></h3>
      <p class="stack">Stack: Python · Pandas · Matplotlib</p>
      <p>
        Utilising Pandas and Matplotlib to transform validated logs into actionable KPI dashboards
        and automated growth trend visualisations.
      </p>
    </div>

    <h2>Technical Methodology</h2>
    <div class="method-grid">
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

<script>
  const lightbox     = document.getElementById('lightbox');
  const lightboxImg  = document.getElementById('lightboxImg');
  const lightboxClose= document.getElementById('lightboxClose');
  const archWrap     = document.getElementById('archWrap');

  let scale = 1;
  const MIN_SCALE = 0.5;
  const MAX_SCALE = 5;

  // Open lightbox on diagram click
  archWrap.addEventListener('click', () => {
    scale = 1;
    lightboxImg.style.transform = 'scale(1)';
    lightbox.classList.add('active');
  });

  // Close on X button
  lightboxClose.addEventListener('click', closeLightbox);

  // Close on click outside the image
  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox || e.target === lightbox.querySelector('.lightbox-inner')) {
      closeLightbox();
    }
  });

  // Close on Escape key
  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape') closeLightbox();
  });

  function closeLightbox() {
    lightbox.classList.remove('active');
    scale = 1;
    lightboxImg.style.transform = 'scale(1)';
  }

  // Mouse wheel zoom inside lightbox
  lightbox.addEventListener('wheel', (e) => {
    e.preventDefault();
    const delta = e.deltaY > 0 ? -0.15 : 0.15;
    scale = Math.min(MAX_SCALE, Math.max(MIN_SCALE, scale + delta));
    lightboxImg.style.transform = `scale(${scale})`;
  }, { passive: false });

  // Mouse wheel zoom on the thumbnail in the page
  archWrap.addEventListener('wheel', (e) => {
    e.preventDefault();
    const img = document.getElementById('archThumb');
    if (!img) return;
    let current = parseFloat(img.dataset.scale || 1);
    const delta = e.deltaY > 0 ? -0.1 : 0.1;
    current = Math.min(3, Math.max(0.5, current + delta));
    img.dataset.scale = current;
    img.style.transform = `scale(${current})`;
  }, { passive: false });
</script>

</body>
</html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Brightone Onyango - Technical Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy:  #002b5c;
      --blue:  #004a99;
      --light: #f5f7fa;
      --white: #ffffff;
      --text:  #1a1a2e;
      --muted: #556070;
      --border:#dde3ec;
    }

    body {
      font-family: 'IBM Plex Sans', sans-serif;
      background: var(--white);
      color: var(--text);
      min-height: 100vh;
    }

    .layout {
      display: grid;
      grid-template-columns: 300px 1fr;
      min-height: 100vh;
    }

    /* LEFT SIDEBAR */
    .sidebar {
      background: var(--light);
      border-right: 1px solid var(--border);
      padding: 48px 28px;
      position: sticky;
      top: 0;
      height: 100vh;
      overflow-y: auto;
    }

    .sidebar h1 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5em;
      color: var(--blue);
      margin-bottom: 22px;
      line-height: 1.25;
    }

    .profile-img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      overflow: hidden;
      border: 3px solid var(--blue);
      margin-bottom: 22px;
      background: #dce8f5;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .profile-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .placeholder-text {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.72em;
      color: var(--blue);
      text-align: center;
      line-height: 1.6;
      padding: 10px;
    }

    .sidebar-role {
      font-size: 0.9em;
      color: var(--muted);
      margin-bottom: 28px;
      line-height: 1.5;
      text-align: center;
    }

    .sidebar-section { margin-bottom: 26px; }

    .sidebar-section h3 {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.72em;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--blue);
      border-bottom: 1px solid var(--border);
      padding-bottom: 5px;
      margin-bottom: 10px;
    }

    .sidebar-section p { font-size: 0.9em; line-height: 1.6; }

    .sidebar-section ul {
      padding-left: 16px;
      font-size: 0.9em;
      line-height: 1.8;
    }

    .sidebar-section a {
      display: block;
      font-size: 0.9em;
      color: var(--blue);
      text-decoration: none;
      line-height: 2;
      font-weight: 500;
    }

    .sidebar-section a:hover { text-decoration: underline; }

    /* RIGHT MAIN */
    .main { padding: 48px 1in; }

    .main h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2em;
      color: var(--navy);
      margin-bottom: 20px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 14px;
    }

    .intro {
      font-size: 1em;
      line-height: 1.85;
      color: var(--muted);
      margin-bottom: 16px;
    }

    .intro strong { color: var(--navy); }
    .intro a { color: var(--blue); font-weight: 600; text-decoration: none; }
    .intro a:hover { text-decoration: underline; }

    .intro-block { margin-bottom: 36px; }

    .main h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.45em;
      color: var(--blue);
      margin-bottom: 18px;
      margin-top: 42px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 8px;
    }

    .project-card {
      margin-bottom: 40px;
      padding-bottom: 40px;
      border-bottom: 1px solid var(--border);
    }

    .project-card h3 {
      font-size: 1.1em;
      font-weight: 600;
      color: var(--navy);
      margin-bottom: 4px;
    }

    .stack {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.82em;
      color: var(--blue);
      margin-bottom: 12px;
    }

    .project-card p {
      font-size: 0.97em;
      line-height: 1.75;
      color: var(--muted);
      margin-bottom: 14px;
    }

    /* ARCHITECTURE DIAGRAM */
    .arch-wrap {
      margin: 18px 0 6px;
      border-radius: 8px;
      overflow: hidden;
      border: 1px solid var(--border);
      background: #eef3fb;
      min-height: 140px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: zoom-in;
      position: relative;
    }

    .arch-wrap img {
      width: 100%;
      display: block;
      transition: transform 0.1s ease;
      transform-origin: center center;
    }

    .arch-wrap:hover::after {
      content: "Click to enlarge  |  Scroll to zoom";
      position: absolute;
      bottom: 10px;
      right: 12px;
      background: rgba(0,43,92,0.75);
      color: #fff;
      font-size: 0.72em;
      font-family: 'IBM Plex Mono', monospace;
      padding: 4px 10px;
      border-radius: 4px;
      pointer-events: none;
    }

    .arch-placeholder {
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.8em;
      color: var(--blue);
      text-align: center;
      padding: 40px;
      line-height: 1.7;
    }

    .diagram-caption {
      font-size: 0.8em;
      font-style: italic;
      color: #999;
      text-align: center;
      margin-bottom: 18px;
    }

    /* LIGHTBOX */
    .lightbox {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.88);
      z-index: 1000;
      align-items: center;
      justify-content: center;
      cursor: zoom-out;
    }

    .lightbox.active { display: flex; }

    .lightbox-inner {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      overflow: hidden;
    }

    .lightbox img {
      max-width: 90vw;
      max-height: 90vh;
      border-radius: 6px;
      box-shadow: 0 20px 60px rgba(0,0,0,0.6);
      transform-origin: center center;
      transition: transform 0.05s ease;
      cursor: default;
      user-select: none;
    }

    .lightbox-close {
      position: fixed;
      top: 20px;
      right: 28px;
      color: #fff;
      font-size: 2em;
      cursor: pointer;
      line-height: 1;
      z-index: 1001;
      opacity: 0.8;
      font-family: sans-serif;
    }

    .lightbox-close:hover { opacity: 1; }

    .lightbox-hint {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      color: rgba(255,255,255,0.6);
      font-size: 0.8em;
      font-family: 'IBM Plex Mono', monospace;
      pointer-events: none;
    }

    .impact-title {
      font-weight: 600;
      font-size: 0.9em;
      color: var(--navy);
      margin-bottom: 8px;
    }

    .impact-list {
      list-style: disc;
      padding-left: 20px;
      font-size: 0.93em;
      line-height: 1.8;
      color: var(--text);
      margin-bottom: 20px;
    }

    .card-links {
      display: flex;
      gap: 20px;
      align-items: center;
      flex-wrap: wrap;
    }

    .btn {
      background: var(--blue);
      color: #fff;
      padding: 10px 20px;
      border-radius: 5px;
      text-decoration: none;
      font-size: 0.88em;
      font-weight: 600;
      transition: background 0.2s;
    }

    .btn:hover { background: var(--navy); }

    .link {
      color: var(--blue);
      font-size: 0.88em;
      font-weight: 600;
      text-decoration: underline;
    }

    .badge {
      display: inline-block;
      background: #c8a84b;
      color: var(--navy);
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.7em;
      padding: 2px 9px;
      border-radius: 20px;
      margin-left: 8px;
      vertical-align: middle;
    }

    .method-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
      margin-top: 10px;
    }

    .method-card {
      background: #eef3fb;
      border: 1px solid #d0e1f2;
      border-radius: 10px;
      padding: 20px 16px;
      text-align: center;
    }

    .method-card strong {
      display: block;
      font-family: 'IBM Plex Mono', monospace;
      font-size: 0.78em;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--blue);
      margin-bottom: 7px;
    }

    .method-card span {
      font-size: 0.87em;
      color: var(--muted);
      line-height: 1.5;
    }

    @media (max-width: 760px) {
      .layout { grid-template-columns: 1fr; }
      .sidebar { position: static; height: auto; }
      .main { padding: 32px 20px; }
      .method-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <span class="lightbox-close" id="lightboxClose">&times;</span>
  <div class="lightbox-inner">
    <img src="assets/architecture diagram.png" alt="Architecture diagram enlarged" id="lightboxImg"/>
  </div>
  <div class="lightbox-hint">Scroll to zoom in and out &nbsp;|&nbsp; Click outside image or press Esc to close</div>
</div>

<div class="layout">

  <!-- LEFT COLUMN -->
  <aside class="sidebar">

    <h1>Brightone Onyango</h1>

    <div class="profile-img">
      <img
        src="assets/profile-pic.png"
        alt="Brightone Onyango"
        onerror="this.style.display='none'; this.parentElement.innerHTML='<div class=\'placeholder-text\'>profile-pic.png<br>(assets/)</div>'"
      />
    </div>

    <p class="sidebar-role">Data Automation Specialist &amp; Technical Writer</p>

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
      <a href="/cdn-cgi/l/email-protection#bcdbd9d3cedbd9deced5c4d3d1c9dbddfcdbd1ddd5d092dfd3d1">Email</a>
      <a href="https://georgixxx.github.io" target="_blank">Portfolio Hub</a>
    </div>

  </aside>

  <!-- RIGHT COLUMN -->
  <main class="main">

    <h1>Technical Portfolio</h1>

    <div class="intro-block">
      <p class="intro">
        Welcome, and thank you for stopping by! I'm glad you're here.
      </p>
      <p class="intro">
        I specialise in engineering high-integrity data pipelines that make automated workflows
        more reliable, auditable, and production-ready. My work sits at the intersection of
        data automation and technical communication. I don't just build systems; I document
        them clearly so that anyone on your team can understand, maintain, and extend them.
      </p>
      <p class="intro">
        Every project in this portfolio is open source, built from real-world use cases, and
        designed with a firm focus on <strong>Accuracy, Clarity, and Traceability</strong>.
        Whether it's validating incoming data before it ever touches a database, or structuring
        workflows that fail gracefully and log every error, the goal is always the same:
        systems you can trust.
      </p>
      <p class="intro">
        If you find any of these projects useful, whether for your own workflows, a team
        implementation, or simply as a learning reference, I'd love to hear from you.
        Feel free to reach out via
        <a href="/cdn-cgi/l/email-protection#4d2a28223f2a282f3f24352220382a2c0d2a202c2421632e2220">email</a>
        or connect with me on
        <a href="https://www.linkedin.com/in/brightone-onyango-109614263" target="_blank">LinkedIn</a>.
        I'm always open to collaboration, feedback, or just a good conversation about data.
      </p>
    </div>

    <h2>Featured Projects</h2>

    <div class="project-card">
      <h3>1. Automated Data Validation Pipeline</h3>
      <p class="stack">Stack: n8n · Python · JSON Schema</p>
      <p>
        A production-ready implementation of data integrity layers for automated workflows.
        It intercepts incoming JSON payloads via Webhooks and validates them against a strict
        JSON Schema before routing to the appropriate downstream path.
      </p>

      <!-- Clickable + zoomable diagram -->
      <div class="arch-wrap" id="archWrap">
        <img
          src="assets/architecture diagram.png"
          alt="System architecture diagram"
          id="archThumb"
          onerror="this.style.display='none'; this.parentElement.innerHTML='<div class=\'arch-placeholder\'>[ architecture diagram.png ]<br><small>Place image in assets/ folder</small></div>'"
        />
      </div>
      <p class="diagram-caption">Figure 1: High-level system architecture, from ingestion to final routing.</p>

      <p class="impact-title">Business Impact</p>
      <ul class="impact-list">
        <li><strong>Reliability:</strong> Reduces database corruption by ensuring 100% schema compliance.</li>
        <li><strong>Efficiency:</strong> Eliminates manual data cleaning, allowing teams to focus on core tasks.</li>
        <li><strong>Traceability:</strong> Establishes a transparent audit trail for every rejected payload.</li>
      </ul>

      <div class="card-links">
        <a class="btn" href="https://github.com/georgixxx/n8n-json-validation-pipeline" target="_blank">View GitHub Repo</a>
        <a class="link" href="https://github.com/georgixxx/n8n-json-validation-pipeline/blob/main/README.md" target="_blank">Full Project Documentation</a>
      </div>
    </div>

    <div class="project-card">
      <h3>2. Python Data Analysis Dashboard <span class="badge">Upcoming</span></h3>
      <p class="stack">Stack: Python · Pandas · Matplotlib</p>
      <p>
        Utilising Pandas and Matplotlib to transform validated logs into actionable KPI dashboards
        and automated growth trend visualisations.
      </p>
    </div>

    <h2>Technical Methodology</h2>
    <div class="method-grid">
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

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  const lightbox     = document.getElementById('lightbox');
  const lightboxImg  = document.getElementById('lightboxImg');
  const lightboxClose= document.getElementById('lightboxClose');
  const archWrap     = document.getElementById('archWrap');

  let scale = 1;
  const MIN_SCALE = 0.5;
  const MAX_SCALE = 5;

  // Open lightbox on diagram click
  archWrap.addEventListener('click', () => {
    scale = 1;
    lightboxImg.style.transform = 'scale(1)';
    lightbox.classList.add('active');
  });

  // Close on X button
  lightboxClose.addEventListener('click', closeLightbox);

  // Close on click outside the image
  lightbox.addEventListener('click', (e) => {
    if (e.target === lightbox || e.target === lightbox.querySelector('.lightbox-inner')) {
      closeLightbox();
    }
  });

  // Close on Escape key
  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape') closeLightbox();
  });

  function closeLightbox() {
    lightbox.classList.remove('active');
    scale = 1;
    lightboxImg.style.transform = 'scale(1)';
  }

  // Mouse wheel zoom inside lightbox
  lightbox.addEventListener('wheel', (e) => {
    e.preventDefault();
    const delta = e.deltaY > 0 ? -0.15 : 0.15;
    scale = Math.min(MAX_SCALE, Math.max(MIN_SCALE, scale + delta));
    lightboxImg.style.transform = `scale(${scale})`;
  }, { passive: false });

  // Mouse wheel zoom on the thumbnail in the page
  archWrap.addEventListener('wheel', (e) => {
    e.preventDefault();
    const img = document.getElementById('archThumb');
    if (!img) return;
    let current = parseFloat(img.dataset.scale || 1);
    const delta = e.deltaY > 0 ?
