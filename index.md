<style>
  /* ── MAIN LAYOUT ── */
  .portfolio-wrapper {
    display: flex;
    height: 100vh;
    overflow: hidden;
    font-family: 'IBM Plex Sans', sans-serif;
    color: #1a1a2e;
  }

  /* ── LEFT SIDEBAR ── */
  .sidebar {
    flex: 0 0 350px;
    background-color: #f8fafc;
    border-right: 1px solid #e2e8f0;
    display: flex;
    flex-direction: column;
    height: 100vh;
  }

  /* Fixed Profile Section */
  .sidebar-fixed-top {
    padding: 40px 20px 20px;
    text-align: center;
    background-color: #f8fafc;
    border-bottom: 2px solid #004a99;
  }

  .name-header {
    font-family: 'Playfair Display', serif;
    font-size: 1.8em;
    color: #002b5c;
    margin-bottom: 15px;
    white-space: nowrap; /* Forces name on one line */
  }

  .profile-circle {
    width: 170px;
    height: 170px;
    border-radius: 50%;
    border: 4px solid #004a99;
    margin: 0 auto 15px;
    overflow: hidden;
  }

  .profile-circle img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .centered-title {
    font-weight: 600;
    color: #004a99;
    font-size: 0.95em;
    text-align: center; /* Centered as requested */
    margin: 0 auto 20px;
    max-width: 250px;
    line-height: 1.4;
  }

  /* Scrollable Info Section */
  .sidebar-scrollable-bottom {
    flex: 1;
    overflow-y: auto;
    padding: 20px 30px;
  }

  .section-title {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.75em;
    text-transform: uppercase;
    color: #64748b;
    border-bottom: 1px solid #cbd5e1;
    padding-bottom: 5px;
    margin-bottom: 15px;
  }

  /* ── RIGHT CONTENT (SCROLLABLE) ── */
  .main-content {
    flex: 1;
    overflow-y: auto;
    padding: 60px 5%;
    background: #ffffff;
  }

  .portfolio-title {
    font-family: 'Playfair Display', serif;
    font-size: 2.5em;
    color: #002b5c;
    margin-bottom: 30px;
    border-bottom: 1px solid #e2e8f0;
    padding-bottom: 15px;
  }

  .project-card {
    background: #ffffff;
    padding: 30px;
    border-radius: 8px;
    border-left: 6px solid #004a99;
    box-shadow: 0 4px 20px rgba(0,0,0,0.05);
    margin-bottom: 40px;
  }

  .tech-stack {
    font-family: 'IBM Plex Mono', monospace;
    color: #004a99;
    font-size: 0.85em;
    margin-bottom: 15px;
  }

  .arch-diagram {
    width: 100%;
    border-radius: 4px;
    border: 1px solid #e2e8f0;
    margin: 20px 0;
    cursor: zoom-in;
  }

  .btn {
    background: #1a1a2e;
    color: #ffffff !important;
    padding: 10px 20px;
    border-radius: 4px;
    text-decoration: none;
    font-size: 0.9em;
    font-weight: 500;
    display: inline-block;
  }

  /* Mobile Responsiveness */
  @media (max-width: 850px) {
    .portfolio-wrapper { flex-direction: column; height: auto; overflow: visible; }
    .sidebar { width: 100%; height: auto; border-right: none; }
    .sidebar-fixed-top { position: static; }
    .main-content { padding: 40px 20px; }
  }
</style>

<div class="portfolio-wrapper">

  <aside class="sidebar">
    <div class="sidebar-fixed-top">
      <h1 class="name-header">Brightone Onyango</h1>
      <div class="profile-circle">
        <img src="assets/profile-pic.png" alt="Brightone Onyango">
      </div>
      <p class="centered-title">Data Automation Specialist & Technical Writer</p>
      <a href="https://github.com/georgixxx" target="_blank" class="btn">GitHub Profile</a>
    </div>

    <div class="sidebar-scrollable-bottom">
      <div style="margin-bottom: 30px;">
        <h3 class="section-title">Education</h3>
        <p style="font-size: 0.95em; margin: 0;"><strong>BSc. Computer Science</strong></p>
        <p style="font-size: 0.9em; color: #475569;">Chuka University</p>
      </div>

      <div style="margin-bottom: 30px;">
        <h3 class="section-title">Certifications</h3>
        <ul style="font-size: 0.9em; padding-left: 15px; line-height: 1.6; color: #334155;">
          <li>n8n Certified Professional</li>
          <li>Certified Data Annotator</li>
        </ul>
      </div>

      <div>
        <h3 class="section-title">Contact</h3>
        <p style="font-size: 0.9em;">
          <a href="mailto:georgebrixomuga@gmail.com" style="color: #004a99; text-decoration: none; font-weight: 600;">Email Me</a><br>
          <a href="https://www.linkedin.com/in/brightone-onyango-109614263" target="_blank" style="color: #004a99; text-decoration: none; font-weight: 600;">LinkedIn Profile</a>
        </p>
      </div>
    </div>
  </aside>

  <main class="main-content">
    <h1 class="portfolio-title">Technical Portfolio</h1>
    
    <p style="font-size: 1.1em; line-height: 1.8; color: #475569; margin-bottom: 40px;">
        I engineering production ready data integrity layers to bridge the gap between raw data ingestion and analytical reliability. My work focuses on building gatekeeper pipelines that ensure high fidelity data streams through strict validation and automated workflow orchestration.
    </p>

    <h2 style="color: #004a99; margin-bottom: 25px;">Featured Projects</h2>

    <div class="project-card">
      <h3 style="font-size: 1.4em; color: #002b5c; margin-bottom: 5px;">1. Automated Data Validation Pipeline</h3>
      <p class="tech-stack">n8n • Python • JSON Schema</p>
      
      <p style="line-height: 1.7; color: #334155;">
          This implementation creates a robust integrity layer for automated workflows. It intercepts incoming JSON payloads via Webhooks and validates them against a strict JSON Schema before routing. This prevents database corruption and ensures downstream analytical tools receive only high quality data.
      </p>

      <a href="assets/architecture diagram.png" target="_blank">
        <img src="assets/architecture diagram.png" alt="System Architecture Diagram" class="arch-diagram">
      </a>
      <p style="font-size: 0.8em; font-style: italic; color: #64748b; text-align: center;">Figure 1: System architecture showing ingestion to final routing.</p>

      <h4 style="color: #002b5c; margin-top: 25px;">Key Deliverables</h4>
      <ul style="line-height: 1.8; color: #334155; font-size: 0.95em;">
        <li>Eliminated manual data cleaning by enforcing schema compliance at the entry point.</li>
        <li>Established a transparent audit trail for every rejected payload.</li>
        <li>Implemented real-time error reporting to reduce response time for data source issues.</li>
      </ul>

      <div style="margin-top: 25px;">
        <a href="https://github.com/georgixxx/n8n-json-validation-pipeline" target="_blank" class="btn">Source Code</a>
      </div>
    </div>

    <div class="project-card">
      <h3 style="font-size: 1.4em; color: #002b5c; margin-bottom: 5px;">2. Python Data Analysis Dashboard</h3>
      <p class="tech-stack">Python • Pandas • Matplotlib • SQL</p>
      
      <p style="line-height: 1.7; color: #334155;">
          Following the data validation phase, this project focuses on transforming raw, validated logs into actionable business insights. Using Pandas and Matplotlib, the system generates automated KPI dashboards that track growth trends and data quality metrics over time.
      </p>

      <div style="background: #f1f5f9; padding: 15px; border-radius: 4px; border-left: 4px solid #64748b; margin-top: 20px;">
        <p style="margin: 0; font-size: 0.9em; font-style: italic; color: #475569;">This project is currently in the final development stage. GitHub release is expected shortly.</p>
      </div>
    </div>

  </main>
</div>
