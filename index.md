<style>
  /* Container to create the two-column look */
  .portfolio-container {
    display: flex;
    gap: 50px;
    align-items: flex-start;
    font-family: 'IBM Plex Sans', sans-serif;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
  }

  /* LEFT SIDEBAR */
  .sidebar {
    flex: 0 0 300px;
    position: sticky;
    top: 20px;
    background-color: #f5f7fa;
    padding: 30px;
    border-radius: 12px;
    border-top: 6px solid #004a99;
    text-align: left;
  }

  .name-header {
    font-family: 'Playfair Display', serif;
    font-size: 1.8em;
    color: #002b5c;
    margin-bottom: 20px;
    margin-top: 0;
  }

  .profile-image {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 3px solid #004a99;
    object-fit: cover;
    margin-bottom: 20px;
  }

  .role-title {
    font-weight: 700;
    color: #004a99;
    font-size: 1.1em;
    line-height: 1.4;
    margin-bottom: 25px;
  }

  .sidebar-section {
    margin-bottom: 25px;
    border-top: 1px solid #dde3ec;
    padding-top: 15px;
  }

  .sidebar-section h3 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.75em;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #556070;
    margin-bottom: 10px;
  }

  /* RIGHT MAIN CONTENT */
  .content-area {
    flex: 1;
    min-width: 0;
  }

  .project-box {
    background: #fff;
    padding: 30px;
    border-radius: 8px;
    border-left: 5px solid #004a99;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    margin-bottom: 40px;
  }

  .enlarge-img {
    width: 100%;
    border-radius: 5px;
    cursor: zoom-in;
    transition: transform 0.2s;
  }

  .enlarge-img:hover {
    transform: scale(1.01);
  }

  @media (max-width: 850px) {
    .portfolio-container { flex-direction: column; }
    .sidebar { width: 100%; position: relative; }
  }
</style>

<div class="portfolio-container">

  <aside class="sidebar">
    <h1 class="name-header">Brightone Onyango</h1>

    <img src="assets/profile-pic.png" alt="Brightone Onyango" class="profile-image">

    <p class="role-title">Data Automation Specialist & Technical Writer</p>

    <div class="sidebar-section">
      <h3>Education</h3>
      <p style="font-size: 0.95em;">
        <strong>BSc. Computer Science</strong><br>
        Chuka University
      </p>
    </div>

    <div class="sidebar-section">
      <h3>Certifications</h3>
      <ul style="font-size: 0.9em; padding-left: 18px; line-height: 1.6;">
        <li>n8n Certified Professional</li>
        <li>Certified Data Annotator</li>
      </ul>
    </div>

    <div class="sidebar-section">
      <h3>Connect</h3>
      <a href="https://github.com/georgixxx" style="display:block; margin-bottom:10px; color:#004a99; font-weight:600; text-decoration:none;">View GitHub Profile</a>
      <a href="mailto:georgebrixomuga@gmail.com" style="display:block; color:#004a99; font-weight:600; text-decoration:none;">Email Me</a>
    </div>
  </aside>

  <main class="content-area">
    <h2 style="font-family: 'Playfair Display', serif; font-size: 2.4em; color: #002b5c; margin-top: 0;">Technical Portfolio</h2>
    
    <p style="font-size: 1.1em; line-height: 1.7; color: #556070; margin-bottom: 35px;">
      I engineer production-ready data integrity layers. I specialize in <strong>"Gatekeeper" pipelines</strong> that intercept, validate, and route data using workflow orchestration.
    </p>

    <div class="project-box">
      <h3 style="color: #002b5c; margin-bottom: 10px;">1. Automated Data Validation Pipeline</h3>
      <p style="font-family: 'IBM Plex Mono', monospace; font-size: 0.85em; color: #004a99; margin-bottom: 20px;">
        STACK: n8n | Python | JSON Schema
      </p>
      
      <a href="assets/architecture diagram.png" target="_blank">
        <img src="assets/architecture diagram.png" alt="Architecture Diagram" class="enlarge-img">
      </a>
      <p style="font-size: 0.8em; font-style: italic; color: #999; text-align: center; margin-top: 10px;">
        Figure 1: High-level system architecture (Click to enlarge).
      </p>

      <p style="line-height: 1.7; color: #333; margin-top: 20px;">
        This pipeline ensures 100% data integrity for automated workflows by intercepting JSON payloads and validating them against strict schemas before they reach the database.
      </p>

      <div style="margin-top: 20px;">
        <a href="https://github.com/georgixxx/n8n-json-validation-pipeline" style="background:#004a99; color:white; padding:10px 20px; border-radius:4px; text-decoration:none; font-weight:600;">GitHub Repository</a>
      </div>
    </div>
  </main>

</div>
