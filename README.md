
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>N2R2 Consulting | IAM & Cybersecurity</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    :root {
      --ink: #0d0d0d;
      --paper: #f5f2ec;
      --accent: #c84b2f;
      --accent2: #1a3a5c;
      --muted: #7a7670;
      --border: #d8d4cc;
      --card: #eceae3;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--paper);
      color: var(--ink);
      font-family: 'DM Sans', sans-serif;
      font-size: 16px;
      line-height: 1.6;
      overflow-x: hidden;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(30px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to   { opacity: 1; }
    }

    /* NAV */
    nav {
      position: fixed; top: 0; left: 0; right: 0;
      display: flex; justify-content: space-between; align-items: center;
      padding: 1.25rem 2.5rem;
      background: rgba(245,242,236,0.93);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      z-index: 100;
    }
    .nav-logo {
      font-family: 'DM Mono', monospace;
      font-size: 1rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent2);
      font-weight: 500;
    }
    .nav-logo span { color: var(--accent); }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--muted);
      text-decoration: none;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }

    /* HERO */
    .hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      padding-top: 5rem;
      overflow: hidden;
    }
    .hero-left {
      display: flex; flex-direction: column; justify-content: center;
      padding: 5rem 3rem 5rem 5rem;
      animation: fadeUp 0.9s ease both;
    }
    .hero-eyebrow {
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 1.5rem;
    }
    .hero-title {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(2.8rem, 4.5vw, 4rem);
      line-height: 1.08;
      margin-bottom: 1.5rem;
    }
    .hero-title em { font-style: italic; color: var(--accent); }
    .hero-sub {
      font-size: 1.05rem;
      color: var(--muted);
      max-width: 460px;
      margin-bottom: 2.5rem;
      line-height: 1.8;
    }
    .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
    .btn-primary {
      display: inline-block;
      background: var(--accent);
      color: #fff;
      font-family: 'DM Mono', monospace;
      font-size: 0.75rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      text-decoration: none;
      padding: 0.9rem 1.8rem;
      border: 2px solid var(--accent);
      transition: background 0.2s, color 0.2s;
    }
    .btn-primary:hover { background: transparent; color: var(--accent); }
    .btn-secondary {
      display: inline-block;
      background: transparent;
      color: var(--accent2);
      font-family: 'DM Mono', monospace;
      font-size: 0.75rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      text-decoration: none;
      padding: 0.9rem 1.8rem;
      border: 2px solid var(--accent2);
      transition: background 0.2s, color 0.2s;
    }
    .btn-secondary:hover { background: var(--accent2); color: #fff; }

    .hero-right {
      position: relative;
      background: var(--accent2);
      display: flex; align-items: center; justify-content: center;
      overflow: hidden;
      animation: fadeIn 1.2s ease both 0.3s;
    }
    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(rgba(255,255,255,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.04) 1px, transparent 1px);
      background-size: 40px 40px;
    }
    .hero-wordmark {
      position: absolute; bottom: 2.5rem; right: 2.5rem;
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: rgba(255,255,255,0.2);
    }
    .hero-stat-block {
      position: relative; z-index: 2;
      display: flex; flex-direction: column; gap: 2.5rem;
      padding: 3rem;
    }
    .stat-item { border-left: 3px solid var(--accent); padding-left: 1.5rem; }
    .stat-num {
      font-family: 'DM Serif Display', serif;
      font-size: 3rem; color: #fff; line-height: 1;
    }
    .stat-label {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem; letter-spacing: 0.15em;
      text-transform: uppercase;
      color: rgba(255,255,255,0.45);
      margin-top: 0.4rem;
    }

    /* SECTION BASE */
    section { padding: 6rem 5rem; }
    .section-label {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem; letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 1rem;
    }
    .section-title {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(1.9rem, 3vw, 2.6rem);
      line-height: 1.15;
      margin-bottom: 1.25rem;
    }

    /* ABOUT */
    .about {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 5rem; align-items: start;
      border-top: 1px solid var(--border);
    }
    .about-text p {
      color: var(--muted); font-size: 1rem;
      line-height: 1.85; margin-bottom: 1.25rem;
    }
    .about-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 2rem; }
    .tag {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem; letter-spacing: 0.1em;
      text-transform: uppercase;
      padding: 0.4rem 0.85rem;
      border: 1px solid var(--border);
      color: var(--muted);
    }
    .about-right {
      background: var(--card);
      padding: 2.5rem;
      border: 1px solid var(--border);
    }
    .about-right h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.35rem; margin-bottom: 1.5rem;
    }
    .about-list { list-style: none; display: flex; flex-direction: column; gap: 1rem; }
    .about-list li {
      display: flex; gap: 1rem; align-items: flex-start;
      font-size: 0.93rem; color: var(--muted);
    }
    .about-list li::before {
      content: '→'; color: var(--accent);
      font-family: 'DM Mono', monospace; flex-shrink: 0;
    }

    /* SERVICES */
    .services { background: var(--ink); color: var(--paper); border-top: 1px solid #1a1a1a; }
    .services .section-label { color: #c84b2f; }
    .services .section-title { color: var(--paper); }
    .services-grid {
      display: grid; grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem; margin-top: 3rem;
    }
    .service-card {
      background: #141414;
      border: 1px solid #252525;
      padding: 2.5rem;
      position: relative;
      transition: border-color 0.25s, transform 0.25s;
    }
    .service-card:hover { border-color: var(--accent); transform: translateY(-5px); }
    .service-num {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem; letter-spacing: 0.2em;
      color: var(--accent); margin-bottom: 1.5rem;
    }
    .service-card h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.35rem; color: var(--paper);
      margin-bottom: 0.5rem;
    }
    .service-price {
      font-family: 'DM Mono', monospace;
      font-size: 0.9rem; color: var(--accent);
      margin-bottom: 1.25rem;
    }
    .service-card p {
      font-size: 0.88rem; color: #777;
      line-height: 1.75; margin-bottom: 1.5rem;
    }
    .service-card ul { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
    .service-card ul li {
      font-size: 0.83rem; color: #666;
      padding-left: 1rem; position: relative;
    }
    .service-card ul li::before {
      content: '·'; position: absolute; left: 0;
      color: var(--accent); font-size: 1.2rem; line-height: 1;
    }
    .service-badge {
      position: absolute; top: 1.5rem; right: 1.5rem;
      background: var(--accent); color: #fff;
      font-family: 'DM Mono', monospace;
      font-size: 0.58rem; letter-spacing: 0.1em;
      text-transform: uppercase; padding: 0.25rem 0.6rem;
    }

    /* WHO I WORK WITH */
    .clients { border-top: 1px solid var(--border); }
    .clients-grid {
      display: grid; grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem; margin-top: 3rem;
    }
    .client-card {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 2rem;
      transition: border-color 0.2s;
    }
    .client-card:hover { border-color: var(--accent); }
    .client-icon { font-size: 2rem; margin-bottom: 1rem; }
    .client-card h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.1rem; margin-bottom: 0.75rem;
    }
    .client-card p { font-size: 0.88rem; color: var(--muted); line-height: 1.75; }

    /* PROCESS */
    .process { background: var(--accent2); color: var(--paper); }
    .process .section-label { color: rgba(200,75,47,0.9); }
    .process .section-title { color: var(--paper); }
    .process-steps {
      display: grid; grid-template-columns: repeat(4, 1fr);
      gap: 2rem; margin-top: 3rem;
    }
    .step {
      border-top: 3px solid rgba(255,255,255,0.12);
      padding-top: 1.5rem;
      transition: border-color 0.2s;
    }
    .step:hover { border-top-color: var(--accent); }
    .step-num {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem; letter-spacing: 0.2em;
      color: var(--accent); margin-bottom: 1rem;
    }
    .step h3 {
      font-family: 'DM Serif Display', serif;
      font-size: 1.15rem; color: var(--paper);
      margin-bottom: 0.75rem;
    }
    .step p { font-size: 0.85rem; color: rgba(255,255,255,0.5); line-height: 1.75; }

    /* CTA */
    .cta-section {
      text-align: center;
      border-top: 1px solid var(--border);
      padding: 7rem 5rem;
    }
    .cta-section .section-title { max-width: 580px; margin: 0 auto 1.25rem; }
    .cta-section > p {
      color: var(--muted); max-width: 460px;
      margin: 0 auto 3rem; font-size: 1rem; line-height: 1.8;
    }
    .cta-buttons { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }

    /* FOOTER */
    footer {
      background: var(--ink); color: rgba(255,255,255,0.35);
      padding: 2.5rem 5rem;
      display: flex; justify-content: space-between; align-items: center;
      border-top: 1px solid #1a1a1a;
    }
    .footer-logo {
      font-family: 'DM Mono', monospace;
      font-size: 0.9rem; letter-spacing: 0.18em;
      text-transform: uppercase; color: rgba(255,255,255,0.6);
    }
    .footer-logo span { color: var(--accent); }
    footer p {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem; letter-spacing: 0.1em;
    }

    /* RESPONSIVE */
    @media (max-width: 900px) {
      .hero { grid-template-columns: 1fr; }
      .hero-right { display: none; }
      .about { grid-template-columns: 1fr; gap: 2.5rem; }
      .services-grid, .clients-grid { grid-template-columns: 1fr; }
      .process-steps { grid-template-columns: 1fr 1fr; }
      section { padding: 4rem 2rem; }
      nav { padding: 1rem 1.5rem; }
      .nav-links { display: none; }
      footer { flex-direction: column; gap: 1rem; text-align: center; padding: 2rem; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="nav-logo">N2R2<span>.</span>Consulting</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#clients">Who We Help</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-left">
      <div class="hero-eyebrow">IAM · Cybersecurity · Data Governance</div>
      <h1 class="hero-title">
        Secure your identity.<br>
        <em>Before someone else</em><br>
        exploits it.
      </h1>
      <p class="hero-sub">
        N2R2 Consulting helps growing companies build enterprise-grade identity and access management frameworks — without the overhead of a full-time hire.
      </p>
      <div class="hero-ctas">
        <a href="#contact" class="btn-primary">Book a Free Call</a>
        <a href="#services" class="btn-secondary">View Services</a>
      </div>
    </div>
    <div class="hero-right">
      <div class="hero-grid"></div>
      <div class="hero-stat-block">
        <div class="stat-item">
          <div class="stat-num">$200–300</div>
          <div class="stat-label">Hourly consulting rate</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">2 wks</div>
          <div class="stat-label">Avg. time to first deliverable</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">SOC 2</div>
          <div class="stat-label">ISO 27001 · CCPA · GDPR ready</div>
        </div>
      </div>
      <div class="hero-wordmark">N2R2 Consulting</div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="about-text">
      <div class="section-label">About</div>
      <h2 class="section-title">Enterprise expertise.<br>Boutique attention.</h2>
      <p>
        N2R2 Consulting was founded by a senior IAM leader with hands-on experience managing identity and access management at enterprise scale — including leading a global Data, Identity & Access Management team at TikTok.
      </p>
      <p>
        We work with startups and mid-size companies navigating rapid growth, compliance audits, or security incidents — bringing the frameworks and rigor of a Fortune 500 security program to organizations that need it most.
      </p>
      <div class="about-tags">
        <span class="tag">IAM Architecture</span>
        <span class="tag">Access Governance</span>
        <span class="tag">SOC 2</span>
        <span class="tag">ISO 27001</span>
        <span class="tag">CCPA / GDPR</span>
        <span class="tag">Zero Trust</span>
        <span class="tag">Data Classification</span>
        <span class="tag">Incident Response</span>
      </div>
    </div>
    <div class="about-right">
      <h3>Why companies choose N2R2</h3>
      <ul class="about-list">
        <li>Enterprise-scale IAM experience at TikTok and beyond</li>
        <li>Deep cross-functional knowledge across legal, compliance, and security</li>
        <li>Practical, audit-ready deliverables — not just strategy decks</li>
        <li>Engagements designed to transfer knowledge, not create dependency</li>
        <li>Trusted advisor with active experience on legal hold and incident response</li>
      </ul>
    </div>
  </section>

  <!-- SERVICES -->
  <section class="services" id="services">
    <div class="section-label">Services</div>
    <h2 class="section-title">What we offer</h2>
    <div class="services-grid">

      <div class="service-card">
        <div class="service-num">01</div>
        <h3>IAM Quick Audit</h3>
        <div class="service-price">Starting at $4,500</div>
        <p>A focused 1-week engagement to assess your current access controls, surface critical gaps, and give you a clear remediation roadmap.</p>
        <ul>
          <li>Access control & permissions review</li>
          <li>User provisioning & offboarding audit</li>
          <li>Stakeholder interviews (IT, Eng, HR)</li>
          <li>Written risk report with prioritized actions</li>
        </ul>
      </div>

      <div class="service-card">
        <div class="service-badge">Most Popular</div>
        <div class="service-num">02</div>
        <h3>IAM Architecture & Roadmap</h3>
        <div class="service-price">Starting at $10,000</div>
        <p>A comprehensive 3-week deep dive into your identity infrastructure, benchmarked against leading frameworks with a 90-day remediation plan.</p>
        <ul>
          <li>Full identity infrastructure review</li>
          <li>Tooling & gap analysis</li>
          <li>NIST / ISO 27001 benchmarking</li>
          <li>90-day prioritized remediation roadmap</li>
        </ul>
      </div>

      <div class="service-card">
        <div class="service-num">03</div>
        <h3>Ongoing Advisory Retainer</h3>
        <div class="service-price">$6,000–$12,000 / month</div>
        <p>Dedicated ongoing advisory for companies that need a trusted IAM and security partner without a full-time hire.</p>
        <ul>
          <li>4 strategy calls per month</li>
          <li>Async access & policy reviews</li>
          <li>Incident response support</li>
          <li>24-hr priority response</li>
        </ul>
      </div>

    </div>
  </section>

  <!-- WHO I WORK WITH -->
  <section class="clients" id="clients">
    <div class="section-label">Who We Help</div>
    <h2 class="section-title">Built for companies<br>at an inflection point.</h2>
    <div class="clients-grid">
      <div class="client-card">
        <div class="client-icon">🔐</div>
        <h3>Pre-Audit Companies</h3>
        <p>Preparing for SOC 2, ISO 27001, or FedRAMP and need a structured IAM program that will hold up to scrutiny.</p>
      </div>
      <div class="client-card">
        <div class="client-icon">🚀</div>
        <h3>Fast-Growing Startups</h3>
        <p>Scaling quickly and realizing your access controls haven't kept up. Typically Series A–C, 50–500 employees.</p>
      </div>
      <div class="client-card">
        <div class="client-icon">⚠️</div>
        <h3>Post-Incident Teams</h3>
        <p>Navigating a data exposure, access breach, or regulatory inquiry and needing immediate expert guidance.</p>
      </div>
      <div class="client-card">
        <div class="client-icon">🏦</div>
        <h3>Fintech & Healthtech</h3>
        <p>Operating in regulated industries where identity and data governance aren't optional — they're existential.</p>
      </div>
      <div class="client-card">
        <div class="client-icon">🌐</div>
        <h3>Global Data Operations</h3>
        <p>Managing cross-border data flows that touch CCPA, GDPR, or other regional privacy frameworks.</p>
      </div>
      <div class="client-card">
        <div class="client-icon">🛡️</div>
        <h3>No In-House CISO</h3>
        <p>Companies that need senior security leadership and direction without the cost of a full-time executive.</p>
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section class="process">
    <div class="section-label">How It Works</div>
    <h2 class="section-title">From first call to deliverable<br>in weeks, not months.</h2>
    <div class="process-steps">
      <div class="step">
        <div class="step-num">Step 01</div>
        <h3>Discovery Call</h3>
        <p>A free 30-minute conversation to understand your situation, goals, and where the most urgent risk lives.</p>
      </div>
      <div class="step">
        <div class="step-num">Step 02</div>
        <h3>Scoping & Proposal</h3>
        <p>A clear, fixed-scope proposal within 48 hours — no vague hourly estimates, no surprises.</p>
      </div>
      <div class="step">
        <div class="step-num">Step 03</div>
        <h3>Engagement</h3>
        <p>Focused, structured work with regular check-ins. We move fast and keep you informed throughout.</p>
      </div>
      <div class="step">
        <div class="step-num">Step 04</div>
        <h3>Deliverable & Handoff</h3>
        <p>Practical, actionable outputs your team can immediately act on — and a knowledge transfer so you stay equipped.</p>
      </div>
    </div>
  </section>

  <!-- CTA / CONTACT -->
  <section class="cta-section" id="contact">
    <div class="section-label">Get Started</div>
    <h2 class="section-title">Ready to build a security program<br>your auditors will respect?</h2>
    <p>Book a free 30-minute discovery call. No pitch, no pressure — just a direct conversation about where you are and how we can help.</p>
    <div class="cta-buttons">
      <a href="mailto:reenanparekh@gmail.com" class="btn-primary">Book a Free Call</a>
      <a href="mailto:reenanparekh@gmail.com" class="btn-secondary">reenanparekh@gmail.com</a>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-logo">N2R2<span>.</span>Consulting</div>
    <p>IAM · Cybersecurity · Data Governance</p>
    <p>© 2026 N2R2 Consulting. All rights reserved.</p>
  </footer>

</body>
</html>
