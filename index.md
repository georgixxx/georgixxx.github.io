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
    .main { 
      padding: 48px 1in; /* Changed to 1 inch left and right margin */
      max-width: none;   /* Removed max-width to allow margins to be absolute */
    }

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
