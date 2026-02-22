<style>
  /* ── LAYOUT ── */
  .portfolio-wrapper {
    display: flex;
    height: 100vh;
    overflow: hidden;
    font-family: 'IBM Plex Sans', sans-serif;
    color: #1a1a2e;
  }

  /* ── LEFT SIDEBAR (FIXED) ── */
  .sidebar-fixed {
    flex: 0 0 350px;
    background-color: #f5f7fa;
    border-right: 1px solid #dde3ec;
    display: flex;
    flex-direction: column;
    height: 100vh;
  }

  /* Fixed Top Part of Sidebar */
  .sidebar-top {
    padding: 40px 30px 20px;
    text-align: center;
    border-bottom: 2px solid #004a99;
  }

  .name-line {
    font-family: 'Playfair Display', serif;
    font-size: 1.8em;
    color: #002b5c;
    margin-bottom: 20px;
    white-space: nowrap;
  }

  .profile-circle {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    border: 4px solid #004a99;
    margin: 0 auto 20px;
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
    font-size: 1em;
    text-align: center;
    margin-bottom: 10px;
  }

  /* Scrollable Bottom Part of Sidebar */
  .sidebar-scrollable {
    flex: 1;
    overflow-y: auto;
    padding: 20px 30px;
  }

  .sidebar-section h3 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.75em;
    text-transform: uppercase;
    color: #556070;
    border-bottom: 1px solid #dde3ec;
    padding-bottom: 5px;
    margin-bottom: 12px;
  }

  /* ── RIGHT MAIN CONTENT (SCROLLABLE) ── */
  .main-scrollable {
    flex: 1;
    overflow-y: auto;
    padding: 60px 80px;
    background: white;
  }

  .project-card {
    background: #ffffff;
    padding: 40px;
    border-radius: 8px;
    border-left: 6px solid #004a99;
    box-shadow: 0 10px 30px rgba(0,0,0,0.05);
    margin-bottom: 50px;
  }

  .arch-link {
    display: block;
    margin: 25px 0;
    cursor: zoom-in;
    transition: transform 0.2s ease;
  }

  .arch-link:hover { transform: scale(1.01); }

  .btn-github {
    background: #24292e;
    color: white !important;
    padding: 12px 24px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 600;
    display: inline-block;
  }

  @media (max-width: 900px) {
    .portfolio-wrapper { flex-direction: column; height: auto; overflow: visible; }
    .sidebar-fixed { width: 100%; height: auto; position: relative; }
    .main-scrollable { padding: 40px 20px; }
  }
</style>

<div class="portfolio-wrapper">

  <aside class="sidebar-fixed">
    <div class="sidebar-top">
      <h1 class="name-line">Brightone Onyango</h1>
      <div class="profile-circle">
        <img src="assets/profile-pic.png" alt="Brightone Onyango">
      </div>
      <p class="centered-title">Data Automation Specialist & Technical Writer</p>
      <a href="https://github.com/georgixxx" class="btn-github" style="font-size: 0.8em;">GitHub Profile</a>
    </div>

    <div class="sidebar-scrollable">
      <div class="sidebar-section">
        <h3>Education</h3>
        <p style="font-size: 0.9em; margin-bottom: 15px;">
          <strong>BSc. Computer Science</strong><br>
          Chuka University
        </p>
      </div>

      <div class="sidebar-section">
        <h3>Certifications</h3>
        <ul style="font-size: 0.85em; padding-left: 15px; line-height: 1.8;">
          <li>n8n Certified Professional</li>
          <li>Certified Data Annotator</li>
        </ul>
      </div>

      <div class="sidebar-section">
        <h3>Contact</h3>
        <p style="font-size: 0.85em;">
          <a href="mailto:georgebrixomuga@gmail.com" style="color: #004a99; text-decoration: none;">Email Me</a><br>
          <a href="https://www.linkedin.com/in/brightone-onyango-109614263" style="color: #004a99; text-decoration: none;">LinkedIn</a>
        </p>
      </div>
    </div>
  </aside>

  <main class="main-scrollable">
    <h1 style="font-family: 'Playfair Display', serif; font-size: 2.8em; color: #002b5c; margin-bottom: 20px;">Technical Portfolio</h1>
    
    <p style="font-size: 1.15em; line-height: 1.8; color: #556070; margin-bottom: 50px; max-width: 800px;">
        I engineering production-ready data integrity layers to bridge the gap between raw data ingestion and analytical reliability. My work focuses on <strong>"Gatekeeper" pipelines</strong>—automated systems that ensure high-fidelity data streams through strict validation and workflow orchestration.
    </p>

    <h2 style="color: #004a99; border-bottom: 1px solid #dde3ec; padding-bottom: 10px; margin-bottom: 30px;">Featured Projects</h2>

    <div class="project-card">
      <h3 style="font-size: 1.6em; color: #002b5c; margin-bottom: 5px;">1. Automated Data Validation Pipeline</h3>
      <p style="font-family: 'IBM Plex Mono', monospace; color: #004a99; font-size: 0.9em; margin-bottom: 20px;">n8n • Python • JSON Schema</p>
      
      <p style="line-height: 1.7; margin-bottom: 20px;">
          This project implements a robust integrity layer for automated data workflows. It intercepts incoming JSON payloads via Webhooks and utilizes <strong>JSON Schema Draft 07</strong> alongside custom <strong>Python validation logic</strong> to verify data structure and content accuracy before storage.
      </p>

      <a href="assets/architecture diagram.png" target="_blank" class="arch-link" title="Click to view full size">
        <img src="assets/architecture diagram.png" alt="System Architecture Diagram" style="width: 100%; border-radius: 5px; border: 1px solid #dde3ec;">
      </a>
      <p style="font-size: 0.85em; font-style: italic; color: #999; text-align: center;">Figure 1: High-level system architecture — from ingestion to routing.</p>

      <h4 style="margin-top: 30px; color: #002b5c;">Technical Impact:</h4>
      <ul style="line-height: 1.8; margin-bottom: 25px;">
        <li><strong>Data Integrity:</strong> Prevents "silent failures" by rejecting non-compliant payloads.</li>
        <li><strong>Orchestration:</strong> Uses n8n for flexible routing of valid vs. invalid data.</li>
        <li><strong>Auditability:</strong> Generates real-time error logs and alerts for immediate troubleshooting.</li>
      </ul>

      <a href="https://github.com/georgixxx/n8n-json-validation-pipeline" class="btn-github">View Project on GitHub</a>
    </div>

    <div class="project-card">
      <h3 style="font-size: 1.6em; color: #002b5c; margin-bottom: 5px;">2. Python Data Analysis Dashboard</h3>
      <p style="font-family: 'IBM Plex Mono', monospace; color: #004a99; font-size: 0.9em; margin-bottom: 20px;">Python • Pandas • Matplotlib • SQL</p>
      
      <p style="line-height: 1.7; margin-bottom: 20px;">
          Building on the validated data streams from Project 1, this upcoming dashboard focuses on <strong>automated KPI reporting</strong>. It utilizes Pandas to transform raw logs into actionable business insights, identifying trends and data quality patterns over time.
      </p>

      <div style="background: #f0f4f8; padding: 20px; border-radius: 5px; border: 1px dashed #004a99; text-align: center;">
        <p style="font-style: italic; color: #004a99; margin: 0;">Currently in development — Stay tuned for the GitHub release.</p>
      </div>
    </div>

  </main>
</div>
