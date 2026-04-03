---
layout: false
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CAM Clinic · Pueblo Chiropractic · Dr. Theodore Davis</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy: #0a1628;
      --blue: #378ADD;
      --blue-light: #E6F1FB;
      --blue-mid: #185FA5;
      --blue-muted: #7ba7d4;
      --cream: #f0ece4;
      --cream-dim: rgba(240,236,228,0.65);
      --text: #1a1a1a;
      --text-secondary: #555;
      --text-tertiary: #888;
      --bg: #f7f6f3;
      --bg-surface: #fff;
      --bg-secondary: #f2f0ec;
      --border: rgba(0,0,0,0.1);
      --border-light: rgba(0,0,0,0.06);
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    /* ── NAV ── */
    nav {
      background: var(--navy);
      padding: 16px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .nav-brand {
      font-family: 'Cormorant Garamond', serif;
      font-size: 20px;
      font-weight: 300;
      color: var(--cream);
      letter-spacing: 0.03em;
    }
    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }
    .nav-links a {
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: rgba(240,236,228,0.6);
      text-decoration: none;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--cream); }

    /* ── HERO ── */
    .hero {
      position: relative;
      background: var(--navy);
      padding: 80px 48px 72px;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: -80px; right: -80px;
      width: 360px; height: 360px;
      border: 1px solid rgba(255,255,255,0.06);
      border-radius: 50%;
    }
    .hero::after {
      content: '';
      position: absolute;
      bottom: -120px; right: 40px;
      width: 280px; height: 280px;
      border: 1px solid rgba(255,255,255,0.04);
      border-radius: 50%;
    }
    .spine-accent {
      position: absolute;
      left: 0; top: 0; bottom: 0;
      width: 3px;
      background: linear-gradient(to bottom, var(--blue) 0%, var(--navy) 100%);
    }
    .hero-eyebrow {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--blue-muted);
      margin-bottom: 20px;
    }
    .hero-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(44px, 6vw, 72px);
      font-weight: 300;
      color: var(--cream);
      line-height: 1.05;
      margin-bottom: 10px;
    }
    .hero-name em {
      font-style: italic;
      color: #b8cce0;
    }
    .hero-credentials {
      font-family: 'Cormorant Garamond', serif;
      font-size: 21px;
      font-weight: 300;
      color: var(--blue-muted);
      letter-spacing: 0.05em;
      margin-bottom: 32px;
    }
    .hero-divider {
      width: 48px; height: 1px;
      background: rgba(123,167,212,0.5);
      margin-bottom: 28px;
    }
    .hero-tagline {
      font-size: 15px;
      font-weight: 300;
      color: var(--cream-dim);
      line-height: 1.75;
      max-width: 480px;
    }

    /* ── STATS ── */
    .stat-strip {
      background: var(--navy);
      padding: 28px 36px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      border-top: 1px solid rgba(255,255,255,0.07);
    }
    .stat-item { text-align: center; padding: 0 20px; }
    .stat-item:not(:last-child) { border-right: 1px solid rgba(255,255,255,0.08); }
    .stat-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 44px;
      font-weight: 300;
      color: var(--cream);
      line-height: 1;
      display: block;
      margin-bottom: 6px;
    }
    .stat-label {
      font-size: 11px;
      font-weight: 400;
      letter-spacing: 0.1em;
      color: var(--blue-muted);
      text-transform: uppercase;
    }

    /* ── SECTION HEADER ── */
    .section-header {
      background: var(--bg-surface);
      padding: 48px 40px 0;
    }
    .section-eyebrow {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--text-tertiary);
      margin-bottom: 8px;
    }
    .section-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: 34px;
      font-weight: 400;
      color: var(--text);
      line-height: 1.2;
      margin-bottom: 32px;
    }
    .section-title em {
      font-style: italic;
      font-weight: 300;
    }

    /* ── ABOUT GRID ── */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1px;
      background: var(--border-light);
    }
    .content-block {
      background: var(--bg-surface);
      padding: 32px 36px;
    }
    .content-block.full-width { grid-column: 1 / -1; }
    .block-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--text-tertiary);
      margin-bottom: 16px;
    }
    .credential-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .credential-list li {
      display: flex;
      align-items: flex-start;
      gap: 14px;
      font-size: 14px;
      font-weight: 300;
      color: var(--text);
      line-height: 1.55;
    }
    .cred-dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: var(--blue);
      margin-top: 7px;
      flex-shrink: 0;
    }
    .specialty-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }
    .specialty-pill {
      background: var(--bg-secondary);
      border: 0.5px solid var(--border);
      border-radius: 4px;
      padding: 10px 14px;
      font-size: 13px;
      font-weight: 400;
      color: var(--text-secondary);
      line-height: 1.4;
    }
    .approach-block {
      background: var(--bg-secondary);
      border-left: 3px solid var(--blue);
      padding: 32px 36px;
    }
    .approach-quote {
      font-family: 'Cormorant Garamond', serif;
      font-size: 23px;
      font-style: italic;
      font-weight: 300;
      color: var(--text);
      line-height: 1.6;
    }
    .approach-attribution {
      margin-top: 14px;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--text-tertiary);
    }

    /* ── WHY CHOOSE US ── */
    .why-section {
      background: var(--bg-surface);
      padding: 56px 40px 0;
    }
    .why-intro {
      font-size: 15px;
      font-weight: 300;
      color: var(--text-secondary);
      line-height: 1.85;
      max-width: 780px;
      margin-bottom: 40px;
    }
    .conditions-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1px;
      background: var(--border-light);
      margin: 0 -40px;
    }
    .condition-card {
      background: var(--bg-surface);
      padding: 36px 40px;
      position: relative;
      transition: background 0.2s;
    }
    .condition-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: var(--blue);
      opacity: 0;
      transition: opacity 0.2s;
    }
    .condition-card:hover::before { opacity: 1; }
    .condition-card:hover { background: #fafaf8; }
    .condition-icon {
      width: 38px; height: 38px;
      background: var(--blue-light);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 18px;
    }
    .condition-icon svg { width: 18px; height: 18px; }
    .condition-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: 23px;
      font-weight: 400;
      color: var(--text);
      margin-bottom: 12px;
      line-height: 1.2;
    }
    .condition-text {
      font-size: 14px;
      font-weight: 300;
      color: var(--text-secondary);
      line-height: 1.8;
    }

    /* ── TREATMENTS BAND ── */
    .treatments-band {
      background: var(--navy);
      padding: 36px 40px;
    }
    .treatments-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--blue-muted);
      margin-bottom: 20px;
    }
    .treatments-list {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      list-style: none;
    }
    .treatments-list li {
      background: rgba(255,255,255,0.06);
      border: 0.5px solid rgba(123,167,212,0.25);
      border-radius: 4px;
      padding: 9px 18px;
      font-size: 13px;
      font-weight: 300;
      color: rgba(240,236,228,0.8);
    }

    /* ── CONTACT ── */
    .contact-section {
      background: var(--bg-surface);
      padding: 56px 40px 64px;
    }
    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1.6fr;
      gap: 56px;
      margin-top: 36px;
    }
    .info-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--text-tertiary);
      margin-bottom: 8px;
    }
    .info-value {
      font-size: 15px;
      font-weight: 300;
      color: var(--text);
      line-height: 1.65;
      margin-bottom: 28px;
    }
    .info-value a {
      color: var(--blue);
      text-decoration: none;
    }
    .info-value a:hover { text-decoration: underline; }
    .hours-grid { display: grid; gap: 0; }
    .hours-row {
      display: flex;
      justify-content: space-between;
      font-size: 13px;
      font-weight: 300;
      color: var(--text-secondary);
      padding: 8px 0;
      border-bottom: 0.5px solid var(--border-light);
    }
    .hours-day { font-weight: 400; color: var(--text); }
    .hours-note {
      font-size: 11px;
      color: var(--text-tertiary);
      margin-top: 8px;
    }

    /* ── FORM ── */
    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }
    .form-group {
      display: flex;
      flex-direction: column;
      gap: 7px;
    }
    .form-group.full { grid-column: 1 / -1; }
    label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text-secondary);
    }
    input[type="text"],
    input[type="tel"],
    input[type="email"],
    textarea {
      background: var(--bg-secondary);
      border: 0.5px solid var(--border);
      border-radius: 6px;
      padding: 11px 14px;
      font-family: 'DM Sans', sans-serif;
      font-size: 14px;
      font-weight: 300;
      color: var(--text);
      outline: none;
      width: 100%;
      transition: border-color 0.15s;
      -webkit-appearance: none;
    }
    input:focus, textarea:focus {
      border-color: var(--blue);
      background: #fff;
    }
    textarea { resize: vertical; min-height: 130px; }
    .submit-btn {
      margin-top: 10px;
      background: var(--navy);
      color: var(--cream);
      border: none;
      border-radius: 6px;
      padding: 14px 32px;
      font-family: 'DM Sans', sans-serif;
      font-size: 13px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: pointer;
      transition: background 0.2s;
    }
    .submit-btn:hover { background: var(--blue); }

    /* ── FOOTER ── */
    footer {
      background: var(--navy);
      padding: 22px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .footer-brand {
      font-family: 'Cormorant Garamond', serif;
      font-size: 16px;
      font-weight: 300;
      color: rgba(240,236,228,0.5);
    }
    .footer-policy {
      font-size: 12px;
      color: var(--blue-muted);
      text-decoration: none;
    }
    .footer-policy:hover { text-decoration: underline; }
    .footer-copy {
      font-size: 12px;
      color: rgba(240,236,228,0.3);
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav { padding: 14px 20px; }
      .nav-links { gap: 16px; }
      .nav-links a { font-size: 11px; }
      .hero { padding: 56px 24px 52px; }
      .stat-strip { padding: 20px 16px; }
      .stat-num { font-size: 32px; }
      .about-grid { grid-template-columns: 1fr; }
      .content-block { padding: 28px 24px; }
      .content-block.full-width { grid-column: 1; }
      .specialty-grid { grid-template-columns: 1fr; }
      .section-header { padding: 40px 24px 0; }
      .why-section { padding: 40px 24px 0; }
      .conditions-grid { grid-template-columns: 1fr; margin: 0 -24px; }
      .condition-card { padding: 28px 24px; }
      .treatments-band { padding: 28px 24px; }
      .contact-section { padding: 40px 24px 48px; }
      .contact-grid { grid-template-columns: 1fr; gap: 36px; }
      .form-grid { grid-template-columns: 1fr; }
      .form-group.full { grid-column: 1; }
      footer { padding: 18px 20px; flex-wrap: wrap; gap: 8px; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <span class="nav-brand">CAM Clinic · Pueblo</span>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#why">Why Choose Us</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero" id="about">
    <div class="spine-accent"></div>
    <p class="hero-eyebrow">Center for Alternative Medicine · Pueblo, Colorado</p>
    <h1 class="hero-name">We Got Your Message</em></h1>
    <h1 class="hero-name">Dr. Theodore<br><em>Davis</em></h1>
    <p class="hero-credentials">M.S. · D.C.</p>
    <div class="hero-divider"></div>
    <p class="hero-tagline">Combining advanced chiropractic care, acupuncture, and sports medicine to help you move better and live without pain.</p>
  </section>

  <!-- STATS -->
  <div class="stat-strip">
    <div class="stat-item">
      <span class="stat-num">3</span>
      <span class="stat-label">Advanced Degrees</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">500+</span>
      <span class="stat-label">Injury Cases Managed</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">3</span>
      <span class="stat-label">Athlete Levels Treated</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div style="background: #fff;">
    <div class="section-header">
      <p class="section-eyebrow">About Dr. Davis</p>
    </div>
    <div class="about-grid">
      <div class="content-block">
        <p class="block-label">Education & Training</p>
        <ul class="credential-list">
          <li><span class="cred-dot"></span>Doctorate in Chiropractic Medicine, Logan College of Chiropractic, Chesterfield, MO</li>
          <li><span class="cred-dot"></span>Master's in Sports Science & Rehabilitation, Logan College of Chiropractic, 2011</li>
          <li><span class="cred-dot"></span>B.S. in Biology, University of Washington, Seattle</li>
          <li><span class="cred-dot"></span>Certification in Acupuncture, Texas Chiropractic College</li>
          <li><span class="cred-dot"></span>Internship, University of Denver Sports Medicine Department</li>
        </ul>
      </div>
      <div class="content-block">
        <p class="block-label">Areas of Specialization</p>
        <div class="specialty-grid">
          <div class="specialty-pill">Disc Lesions</div>
          <div class="specialty-pill">Overuse Soft Tissue Injuries</div>
          <div class="specialty-pill">Traumatic Injuries</div>
          <div class="specialty-pill">Pain Management</div>
          <div class="specialty-pill">Peripheral Neuropathies</div>
          <div class="specialty-pill">Automotive Injury</div>
        </div>
      </div>
      <div class="content-block approach-block full-width">
        <p class="approach-quote">"You don't need to hear a crack or pop to achieve an adjustment. With delicate patients, delicate forms of treatment are always the right approach."</p>
        <p class="approach-attribution">— Dr. Theodore Davis, D.C.</p>
      </div>
      <div class="content-block">
        <p class="block-label">Patients Served</p>
        <ul class="credential-list">
          <li><span class="cred-dot"></span>Collegiate, professional, and Olympic-level athletes</li>
          <li><span class="cred-dot"></span>Infants and young children</li>
          <li><span class="cred-dot"></span>Pregnant women</li>
          <li><span class="cred-dot"></span>Geriatric patients</li>
          <li><span class="cred-dot"></span>Automotive injury patients</li>
        </ul>
      </div>
      <div class="content-block">
        <p class="block-label">Licensed in Colorado</p>
        <ul class="credential-list">
          <li><span class="cred-dot"></span>Chiropractic care</li>
          <li><span class="cred-dot"></span>Acupuncture</li>
          <li><span class="cred-dot"></span>Physiotherapy</li>
          <li><span class="cred-dot"></span>Electro-physiotherapy</li>
          <li><span class="cred-dot"></span>Advanced soft tissue & spinal rehabilitation</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- WHY CHOOSE US -->
  <div class="why-section" id="why">
    <p class="section-eyebrow">Why Choose Us</p>
    <p class="section-title">We treat the cause,<br><em>not just the symptom.</em></p>
    <p class="why-intro">Pain is rarely simple. What you feel on the surface is usually a signal of something more specific happening underneath. Dr. Davis and the CAM Clinic team are trained to look beyond the symptom and find the cause — starting with a thorough examination, every time. We treat a wide range of musculoskeletal conditions using conservative, non-surgical methods.</p>
    <div class="conditions-grid">
      <div class="condition-card">
        <div class="condition-icon">
          <svg viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="9" cy="9" r="7" stroke="#185FA5" stroke-width="1.2"/>
            <circle cx="9" cy="9" r="3" stroke="#185FA5" stroke-width="1.2"/>
            <line x1="9" y1="2" x2="9" y2="6" stroke="#185FA5" stroke-width="1.2" stroke-linecap="round"/>
            <line x1="9" y1="12" x2="9" y2="16" stroke="#185FA5" stroke-width="1.2" stroke-linecap="round"/>
          </svg>
        </div>
        <p class="condition-title">Joint Aches & Pain</p>
        <p class="condition-text">Your joints are constantly at work — holding you upright, absorbing impact, and making even ordinary movements possible. We treat rotator cuff injuries, frozen shoulder, impingement syndrome, hip and SI joint dysfunction, knee pain, and TMJ disorders. Every patient receives a careful evaluation before any care begins.</p>
      </div>
      <div class="condition-card">
        <div class="condition-icon">
          <svg viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M4 14 C4 10 8 9 9 6 C10 3 12 2 14 4" stroke="#185FA5" stroke-width="1.2" stroke-linecap="round"/>
            <path d="M4 14 C6 12 10 13 12 11" stroke="#185FA5" stroke-width="1.2" stroke-linecap="round"/>
          </svg>
        </div>
        <p class="condition-title">Tendonitis & Muscle Pain</p>
        <p class="condition-text">Tendonitis and tendonosis are often misidentified or undertreated, particularly when muscle pain is involved. We treat conditions affecting the rotator cuff, biceps, Achilles, calf, and many other structures. Our goal is always to exhaust conservative options before any surgical path is considered — and in the vast majority of cases, that approach is enough.</p>
      </div>
      <div class="condition-card">
        <div class="condition-icon">
          <svg viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <line x1="9" y1="2" x2="9" y2="16" stroke="#185FA5" stroke-width="1.2" stroke-linecap="round"/>
            <ellipse cx="9" cy="5" rx="3" ry="1.5" stroke="#185FA5" stroke-width="1"/>
            <ellipse cx="9" cy="9" rx="3.5" ry="1.5" stroke="#185FA5" stroke-width="1"/>
            <ellipse cx="9" cy="13" rx="3" ry="1.5" stroke="#185FA5" stroke-width="1"/>
          </svg>
        </div>
        <p class="condition-title">Spinal Pain</p>
        <p class="condition-text">Spinal pain can manifest almost anywhere — your neck, mid-back, lower back, arms, or even as headaches with no obvious source. Approximately nine out of ten headaches are tension-type originating in the cervical spine. We treat the full length of the spine and rule out serious underlying conditions before proceeding with care.</p>
      </div>
      <div class="condition-card">
        <div class="condition-icon">
          <svg viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M5 9 Q9 5 13 9 Q9 13 5 9Z" stroke="#185FA5" stroke-width="1.2" fill="none"/>
            <circle cx="9" cy="9" r="1.5" fill="#185FA5"/>
          </svg>
        </div>
        <p class="condition-title">Numbness & Tingling</p>
        <p class="condition-text">Among the most commonly misdiagnosed symptoms in musculoskeletal care. Conditions like sciatica and carpal tunnel are frequently used as catch-all diagnoses. Dr. Davis has specialized training in peripheral neuropathies — nerve compressions and irritations that most practitioners aren't equipped to identify.</p>
      </div>
    </div>
  </div>

  <!-- TREATMENTS BAND -->
  <div class="treatments-band">
    <p class="treatments-label">Treatment Modalities</p>
    <ul class="treatments-list">
      <li>Chiropractic Adjustment</li>
      <li>Active Release Technique</li>
      <li>Laser Therapy</li>
      <li>Acupuncture</li>
      <li>Corrective Exercise</li>
      <li>Nutritional Counseling</li>
      <li>Physiotherapy</li>
      <li>Electro-Physiotherapy</li>
    </ul>
  </div>

  <!-- CONTACT -->
  <section class="contact-section" id="contact">
    <p class="section-eyebrow">Get in Touch</p>
    <p class="section-title">Schedule a Consultation</p>
    <div class="contact-grid">
      <!-- Info -->
      <div>
        <p class="info-label">Address</p>
        <p class="info-value">2505 Kachina Dr<br>Pueblo, CO 81008</p>

        <p class="info-label">Phone</p>
        <p class="info-value"><a href="tel:7195442009">(719) 544-2009</a></p>

        <p class="info-label">Office Hours</p>
        <div class="hours-grid">
          <div class="hours-row">
            <span class="hours-day">Monday – Thursday</span>
            <span>9:00am – 6:00pm</span>
          </div>
          <div class="hours-row">
            <span class="hours-day">Friday</span>
            <span>9:00am – 6:00pm*</span>
          </div>
          <div class="hours-row">
            <span class="hours-day">Saturday – Sunday</span>
            <span>Closed</span>
          </div>
        </div>
        <p class="hours-note">*Closed 12:00–1:00pm on Fridays</p>
      </div>

      <!-- Form -->
      <div>
          <form
        id="contact-form"
        class="max-w-[90%] mt-10"
        name="Pueblo Chiro Contact Form"
        method="POST"
        data-netlify="true"
        action="/contact/success/"
      >
          <div class="form-grid">
            <div class="form-group">
              <label for="fname">First Name *</label>
              <input type="text" id="fname" name="first_name" placeholder="First" required>
            </div>
            <div class="form-group">
              <label for="lname">Last Name *</label>
              <input type="text" id="lname" name="last_name" placeholder="Last" required>
            </div>
            <div class="form-group">
              <label for="phone">Phone *</label>
              <input type="tel" id="phone" name="phone" placeholder="(719) 555-0000" required>
            </div>
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" id="email" name="email" placeholder="you@email.com">
            </div>
            <div class="form-group full">
              <label for="comments">Comments *</label>
              <textarea id="comments" name="comments" placeholder="Please let us know what's on your mind. Have a question for us? Ask away." required></textarea>
            </div>
          </div>
          <button type="submit" class="submit-btn">Send Message</button>
        </form>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <span class="footer-brand">CAM Clinic · Pueblo, Colorado</span>
    <a class="footer-policy" href="https://pueblochiropractor.com/privacy/">Privacy Policy</a>
    <span class="footer-copy">© 2026 Pueblo Chiropractic</span>
  </footer>

</body>
</html>
