<style>
  .custom-layout {
    display: flex;
    gap: 40px;
    align-items: flex-start;
    font-family: 'IBM Plex Sans', sans-serif;
    color: #1a1a2e;
    max-width: 1200px;
    margin: 0 auto;
  }

  .custom-sidebar {
    flex: 0 0 300px;
    position: sticky;
    top: 20px;
    background-color: #f5f7fa;
    padding: 25px;
    border-radius: 12px;
    border-top: 5px solid #004a99;
    height: fit-content;
  }

  .sidebar-name {
    font-family: 'Playfair Display', serif;
    color: #002b5c;
    font-size: 1.6em;
    margin-bottom: 15px;
  }

  .profile-circle {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    overflow: hidden;
    border: 3px solid #004a99;
    margin-bottom: 15px;
  }

  .profile-circle img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .sidebar-title {
    font-weight: bold;
    color: #004a99;
    font-size: 1em;
    margin-bottom: 15px;
  }

  .github-link {
    display: inline-block;
    background: #24292e;
    color: white !important;
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 5px;
    font-size: 0.85em;
    margin-bottom: 25px;
  }

  .main-content {
    flex: 1;
    min-width: 0;
  }

  .project-card {
    background: white;
    padding: 25px;
    border-left: 5px solid #004a99;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    margin-bottom: 30px;
  }

  @media (max-width: 768px) {
    .custom-layout { flex-direction: column; }
    .custom-sidebar { flex: 1 1 auto; position: relative; width: 100%; }
  }
</style>

<div class="custom-layout">

  <aside class="custom-sidebar">
    <h2 class="sidebar-name">Brightone Onyango</h2>
    
    <div class="profile-circle">
      <img src="assets/profile-pic.png" alt="Brightone Onyango">
    </div>

    <p class="sidebar-title">Data Automation Specialist & Technical Writer</p>
    
    <a href="https://github.com/georgixxx" class="github-link">View My GitHub Profile</a>

    <div style="margin-top: 20px; border-top: 1px solid #dde3ec; padding-top: 15px;">
      <h3 style="font-size: 0.8em; text-transform: uppercase; color: #004a99;">Education</h3>
      <p style="font-size: 0.9em;"><strong>BSc. Computer Science</strong><br>Chuka University</p>
    </div>

    <div style="margin-top: 15px;">
      <h3 style="font-size: 0.8em; text-transform: uppercase; color: #004a99;">Certifications</h3>
      <ul style="font-size: 0.9em; padding-left: 15px;">
        <li>n8n Certified Professional</li>
        <li>Certified Data Annotator</li>
      </ul>
    </div>
  </aside>

  <main class="main-content">
    <h1 style="font-family: 'Playfair Display', serif; color: #002b5c; border-bottom: 1px solid #dde3ec; padding-bottom: 10px;">Technical Portfolio</h1>
    
    <p style="margin: 20px 0; line-height: 1.6; color: #556070;">
      I bridge the gap between raw data ingestion and analytical reliability. I specialize in building <strong>"Gatekeeper" pipelines</strong> that ensure data integrity.
    </p>

    <div class="project-card">
      <h3 style="color: #002b5c;">1. Automated Data Validation Pipeline</h3>
      <p style="font-family: monospace; color: #004a99; font-size: 0.85em;">n8n • Python • JSON Schema</p>
      
      <a href="assets/architecture diagram.png" target="_blank">
        <img src="assets/architecture diagram.png" alt="Architecture Diagram" style="width: 100%; margin-top: 15px; border-radius: 8px;">
      </a>
      <p style="font-size: 0.8em; font-style: italic; text-align: center; margin-top: 5px;">Figure 1: Click to enlarge diagram.</p>

      <p style="margin-top: 15px; font-size: 0.95em; line-height: 1.6;">
        Developed a production-ready integrity layer to intercept payloads via Webhooks, ensuring 100% schema compliance before storage.
      </p>
    </div>
  </main>

</div>
