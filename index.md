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

    /* ── TWO-COLUMN LAYOUT ── */
    .layout {
      display: grid;
      grid-template-columns: 300px 1fr;
      min-height: 100vh;
    }

    /* ── LEFT SIDEBAR ── */
    .sidebar {
      background: var(--light);
      border-right: 1px solid var(--border);
      padding: 40px 28px;
      position: sticky;
      top: 0;
      height: 100vh;
      overflow-y: auto;
    }

    .sidebar h1 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5em;
      color: var(--navy);
      margin-bottom: 20px;
      line-height: 1.2;
    }

    .profile-img {
      width: 180px;
      height: 180px;
      border-radius: 50%;
      overflow: hidden;
      border: 3px solid var(--blue);
      margin-bottom: 20px;
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

    .sidebar-role {
      font-size: 0.95em;
      font-weight: 600;
      color: var(--blue);
      margin-bottom: 15px;
      line-height: 1.4;
    }

    .github-btn {
      display: block;
      background: #24292e;
      color: #fff;
      text-align: center;
      padding: 10px;
      border-radius: 6px;
      text-decoration: none;
      font-size: 0.85em;
      font-weight: 600;
      margin-bottom: 30px;
    }

    .sidebar-section {
      margin-bottom: 26px;
    }

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

    .sidebar-section p, .sidebar-section ul {
      font-size: 0.9em;
      line-height: 1.6;
      list-style: none;
    }

    .sidebar-section a {
      display: block;
      font-size: 0.9em;
      color: var(--blue);
      text-decoration: none;
      line-height: 2;
      font-weight: 500;
    }

    /* ── RIGHT MAIN ── */
    .main {
      padding: 48px 56px;
      max-width: 900px;
    }

    .main h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.5em;
      color: var(--navy);
      margin-bottom: 16px;
      border-bottom: 1px solid var(--border);
      padding-bottom: 14px;
    }

    .arch-link {
        cursor: zoom-in;
        display: block;
        transition: opacity 0.2s;
    }
    .arch-link:hover { opacity: 0.9; }

    .project-card { margin-bottom: 45px; }

    /* Add same styles from your previous prompt here for cards, methodology, etc. */
    /* ... (Style content truncated for brevity, same as your original) ... */
    
    .method-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 10px; }
    .method-card { background: #eef3fb; border: 1px solid #d0e1f2; border-radius: 10px; padding: 20px 16px; text-align: center; }
    .btn { background: var(--blue); color: #fff; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-size: 0.88em; font-weight: 600; }
  </style>
</head>
<body>

<div class="layout">

  <aside class="sidebar">
    <h1>Brightone Onyango</h1>

    <div class="profile-img">
      <img src="assets/profile-pic.png" alt="Brightone Onyango" 
           onerror="this.style.display='none'; this.parentElement.innerHTML='<div style=\'padding:10px; font-size:0.7em; color:navy;\'>profile-pic.png<br>missing</div>'"/>
    </div>

    <p class="sidebar-role">Data Automation Specialist &amp; Technical Writer</p>
    
    <a href="https://github.com/georgixxx" target="_blank" class="github-btn">View My GitHub Profile</a>

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
    </div>
  </aside>

  <main class="main">
    <h1>Technical Portfolio</h1>
    <p style="color: #556070; line-height: 1.8; margin-bottom: 40px;">
        I bridge the gap between raw data ingestion and analytical reliability. I specialize in building <strong>"Gatekeeper" pipelines</strong> that utilize workflow orchestration and automated validation to ensure data integrity.
    </p>

    <h2>Featured Projects</h2>

    <div class="project-card">
      <h3 style="color: #002b5c; margin-bottom: 5px;">1. Automated Data Validation Pipeline</h3>
      <p style="font-family: monospace; color: #004a99; font-size: 0.85em; margin-bottom: 15px;">n8n · Python · JSON Schema</p>
      
      <a href="assets/architecture%20diagram.png" target="_blank" class="arch-link" title="Click to view full size">
        <div style="background: #eef3fb; border: 1px solid #dde3ec; border-radius: 8px; overflow: hidden;">
            <img src="assets/architecture diagram.png" alt="Architecture Diagram" style="width: 100%; display: block;"
                 onerror="this.style.display='none'; this.parentElement.innerHTML='<p style=\'padding:40px; text-align:center;\'>[ architecture diagram.png ]</p>'"/>
        </div>
      </a>
      <p style="font-size: 0.8em; font-style: italic; color: #999; text-align: center; margin: 10px 0 20px;">
          Figure 1: System architecture — Click to enlarge diagram.
      </p>

      <p style="color: #556070; line-height: 1.7; margin-bottom: 20px;">
          Developed a robust integrity layer that intercepts JSON payloads via Webhooks. The system utilizes Python validation logic and JSON Schema to prevent database corruption and downstream model failures.
      </p>

      <div style="display: flex; gap: 20px; align-items: center;">
        <a class="btn" href="https://github.com/georgixxx/n8n-json-validation-pipeline" target="_blank">GitHub Repo</a>
        <a style="color: #004a99; font-weight: 600; font-size: 0.9em;" href="https://github.com/georgixxx/n8n-json-validation-pipeline/blob/main/README.md" target="_blank">Documentation</a>
      </div>
    </div>

    <h2>Technical Methodology</h2>
    <div class="method-grid">
      <div class="method-card">
        <strong>Ingestion</strong>
        <span style="font-size: 0.85em;">REST API Webhooks</span>
      </div>
      <div class="method-card">
        <strong>Validation</strong>
        <span style="font-size: 0.85em;">Python & Schema Logic</span>
      </div>
      <div class="method-card">
        <strong>Routing</strong>
        <span style="font-size: 0.85em;">Production vs. Alerts</span>
      </div>
    </div>
  </main>
</div>

</body>
</html>
