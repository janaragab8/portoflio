# portoflio


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Jana Ragab — CV</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --ink:       #1a1a2e;
      --soft:      #4a4a6a;
      --accent:    #c2773a;
      --accent2:   #7b5ea7;
      --bg:        #f9f7f4;
      --white:     #ffffff;
      --rule:      #e0dbd3;
      --tag-bg:    #f0ebf8;
      --tag-text:  #5c3d8f;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--ink);
      line-height: 1.65;
      font-size: 15px;
    }

    header {
      background: var(--ink);
      color: var(--white);
      padding: 60px 48px 52px;
      position: relative;
      overflow: hidden;
    }
    header::before {
      content: '';
      position: absolute;
      top: -60px; right: -60px;
      width: 320px; height: 320px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(194,119,58,.35) 0%, transparent 70%);
      pointer-events: none;
    }
    header::after {
      content: '';
      position: absolute;
      bottom: -80px; left: 30%;
      width: 220px; height: 220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(123,94,167,.25) 0%, transparent 70%);
      pointer-events: none;
    }

    .hero-eyebrow {
      font-size: 11px;
      letter-spacing: .18em;
      text-transform: uppercase;
      color: var(--accent);
      font-weight: 600;
      margin-bottom: 12px;
    }
    h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(36px, 6vw, 58px);
      font-weight: 700;
      line-height: 1.05;
      letter-spacing: -.5px;
      margin-bottom: 20px;
    }
    .contact-row {
      display: flex;
      flex-wrap: wrap;
      gap: 6px 20px;
      font-size: 13px;
      color: rgba(255,255,255,.7);
    }
    .contact-row span::before {
      content: '·';
      margin-right: 8px;
      color: var(--accent);
    }
    .contact-row span:first-child::before { content: ''; margin-right: 0; }

    .wrapper {
      max-width: 900px;
      margin: 0 auto;
      padding: 0 24px 64px;
    }

    .summary-band {
      background: var(--white);
      border-left: 4px solid var(--accent);
      margin: 40px 0 0;
      padding: 24px 28px;
      border-radius: 0 8px 8px 0;
      font-size: 14.5px;
      color: var(--soft);
      line-height: 1.75;
      box-shadow: 0 2px 12px rgba(0,0,0,.05);
    }

    section { margin-top: 44px; }

    .section-label {
      font-size: 10.5px;
      letter-spacing: .2em;
      text-transform: uppercase;
      font-weight: 600;
      color: var(--accent2);
      margin-bottom: 18px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .section-label::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--rule);
    }

    .exp-card {
      background: var(--white);
      border-radius: 10px;
      padding: 22px 26px;
      margin-bottom: 16px;
      box-shadow: 0 2px 10px rgba(0,0,0,.045);
      transition: box-shadow .2s;
    }
    .exp-card:hover { box-shadow: 0 6px 22px rgba(0,0,0,.09); }

    .exp-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
      gap: 4px;
      margin-bottom: 6px;
    }
    .exp-title {
      font-family: 'Playfair Display', serif;
      font-size: 17px;
      font-weight: 600;
    }
    .exp-date {
      font-size: 12px;
      color: var(--accent);
      font-weight: 500;
      white-space: nowrap;
      margin-top: 2px;
    }
    .exp-company {
      font-size: 13px;
      color: var(--soft);
      margin-bottom: 12px;
    }
    .exp-card ul {
      padding-left: 18px;
      color: var(--soft);
      font-size: 13.5px;
    }
    .exp-card ul li { margin-bottom: 4px; }

    .edu-card {
      background: var(--white);
      border-radius: 10px;
      padding: 22px 26px;
      box-shadow: 0 2px 10px rgba(0,0,0,.045);
    }
    .edu-degree {
      font-family: 'Playfair Display', serif;
      font-size: 17px;
      font-weight: 600;
      margin-bottom: 4px;
    }
    .edu-school { font-size: 13px; color: var(--soft); margin-bottom: 8px; }
    .edu-note { font-size: 13px; color: var(--soft); font-style: italic; }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }
    .tag {
      background: var(--tag-bg);
      color: var(--tag-text);
      font-size: 12.5px;
      font-weight: 500;
      padding: 5px 13px;
      border-radius: 20px;
    }
    .tag.tech {
      background: #fff0e6;
      color: #8a4a10;
    }

    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 24px;
    }
    @media (max-width: 600px) {
      .two-col { grid-template-columns: 1fr; }
      header { padding: 40px 24px 36px; }
      .wrapper { padding: 0 16px 48px; }
    }

    footer {
      text-align: center;
      font-size: 12px;
      color: #bbb;
      padding: 24px;
      border-top: 1px solid var(--rule);
      margin-top: 48px;
    }
  </style>
</head>
<body>

<header>
  <p class="hero-eyebrow"> My Resume</p>
  <h1>Jana Ragab</h1>
  <div class="contact-row">
    <span>Alexandria, Egypt</span>
    <span>+20 15 05723123</span>
    <span>janaragab8@icloud.com</span>
  </div>
</header>

<div class="wrapper">

  <div class="summary-band">
    Business Informatics student at the Arab Academy for Science, Technology & Maritime Transport
    with experience in recruitment, customer engagement, cold calling, lead generation, and telesales.
    Growing technical foundation in Python, C++, and JavaScript. Bilingual (Arabic & English),
    highly adaptable, and passionate about technology and customer experience.
  </div>

  <section>
    <p class="section-label">Professional Experience</p>

    <div class="exp-card">
      <div class="exp-header">
        <span class="exp-title">HR Recruiter</span>
        <span class="exp-date">May 2026 – Present</span>
      </div>
      <p class="exp-company">Alexandria, Egypt</p>
      <ul>
        <li>Source, screen, and evaluate candidates for various positions.</li>
        <li>Conduct initial interviews and candidate assessments.</li>
        <li>Manage recruitment pipelines and candidate databases.</li>
        <li>Coordinate interview scheduling and follow-up communications.</li>
        <li>Support talent acquisition and hiring initiatives.</li>
      </ul>
    </div>

    <div class="exp-card">
      <div class="exp-header">
        <span class="exp-title">Cold Caller</span>
        <span class="exp-date">April 2026 – Present</span>
      </div>
      <p class="exp-company">MyVA</p>
      <ul>
        <li>Conduct outbound calls to prospective customers and qualify leads for sales.</li>
        <li>Present services professionally and handle objections effectively.</li>
        <li>Maintain customer records and meet performance metrics consistently.</li>
        <li>Build rapport with clients in a fast-paced, results-driven environment.</li>
      </ul>
    </div>
  </section>

  <section>
    <p class="section-label">Education</p>
    <div class="edu-card">
      <p class="edu-degree">Bachelor of Business Administration — Business Informatics</p>
      <p class="edu-school">Arab Academy for Science, Technology & Maritime Transport · Sep 2024 – Present</p>
      <p class="edu-note">Relevant Coursework: Python, C++, JavaScript fundamentals (2024–2025).</p>
    </div>
  </section>

  <section>
    <p class="section-label">Skills</p>
    <div class="two-col">
      <div>
        <p style="font-size:12px;font-weight:600;color:var(--soft);margin-bottom:10px;text-transform:uppercase;letter-spacing:.1em;">Technical</p>
        <div class="tags">
          <span class="tag tech">Python</span>
          <span class="tag tech">C++</span>
          <span class="tag tech">JavaScript</span>
          <span class="tag tech">Microsoft Excel</span>
          <span class="tag tech">CRM Systems</span>
          <span class="tag tech">Data Analysis</span>
          <span class="tag tech">Microsoft Office</span>
        </div>
      </div>
      <div>
        <p style="font-size:12px;font-weight:600;color:var(--soft);margin-bottom:10px;text-transform:uppercase;letter-spacing:.1em;">Core Competencies</p>
        <div class="tags">
          <span class="tag">Recruitment</span>
          <span class="tag">Cold Calling</span>
          <span class="tag">Lead Generation</span>
          <span class="tag">Telesales</span>
          <span class="tag">Customer Service</span>
          <span class="tag">Relationship Building</span>
          <span class="tag">Active Listening</span>
          <span class="tag">Problem Solving</span>
          <span class="tag">Bilingual (AR / EN)</span>
          <span class="tag">Adaptability</span>
          <span class="tag">Time Management</span>
        </div>
      </div>
    </div>
  </section>

</div>

<footer>Jana Ragab · Alexandria, Egypt · 2026</footer>

</body>
</html>
