[id8_advisors_landing (1).html](https://github.com/user-attachments/files/26094877/id8_advisors_landing.1.html)
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ID8 Advisors — Energy Transition Advisory</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --teal:    #1D9E75;
    --teal-l:  #5DCAA5;
    --teal-d:  #0F6E56;
    --blue:    #2A7AB8;
    --blue-l:  #5BA3D4;
    --ink:     #0A0F0D;
    --ink-2:   #111A16;
    --ink-3:   #182119;
    --surface: #1A2420;
    --muted:   #6B8A7A;
    --text:    #C8D9D0;
    --text-d:  #8FADA0;
    --white:   #EEF5F1;
    --rule:    rgba(29,158,117,0.18);
    --serif:   'Cormorant Garamond', Georgia, serif;
    --sans:    'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--ink);
    color: var(--text);
    font-family: var(--sans);
    font-weight: 300;
    font-size: 16px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── Noise texture overlay ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
    opacity: 0.6;
  }

  /* ── Nav ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.4rem 4rem;
    border-bottom: 1px solid var(--rule);
    background: rgba(10,15,13,0.85);
    backdrop-filter: blur(12px);
  }
  .nav-logo {
    font-family: var(--serif);
    font-size: 1.35rem;
    font-weight: 600;
    color: var(--white);
    letter-spacing: 0.02em;
    text-decoration: none;
  }
  .nav-logo span { color: var(--teal-l); }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.78rem;
    font-weight: 400;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-d);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--teal-l); }
  .nav-cta {
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--teal-l);
    text-decoration: none;
    border: 1px solid rgba(93,202,165,0.35);
    padding: 0.5rem 1.3rem;
    border-radius: 2px;
    transition: all 0.2s;
  }
  .nav-cta:hover { background: rgba(93,202,165,0.1); border-color: var(--teal-l); }

  /* ── Hero ── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 8rem 4rem 6rem;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 60% 70% at 70% 40%, rgba(29,158,117,0.12) 0%, transparent 60%),
      radial-gradient(ellipse 40% 50% at 20% 80%, rgba(42,122,184,0.08) 0%, transparent 55%);
    z-index: 0;
  }
  /* Subtle grid lines */
  .hero-bg::after {
    content: '';
    position: absolute; inset: 0;
    background-image:
      linear-gradient(var(--rule) 1px, transparent 1px),
      linear-gradient(90deg, var(--rule) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: radial-gradient(ellipse 80% 80% at 70% 30%, black 20%, transparent 70%);
    opacity: 0.4;
  }
  .hero-content {
    position: relative; z-index: 1;
    max-width: 760px;
  }
  .hero-eyebrow {
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 1.8rem;
    display: flex; align-items: center; gap: 0.8rem;
  }
  .hero-eyebrow::before {
    content: '';
    display: block;
    width: 32px; height: 1px;
    background: var(--teal);
  }
  .hero-headline {
    font-family: var(--serif);
    font-size: clamp(3rem, 6vw, 5.2rem);
    font-weight: 300;
    line-height: 1.08;
    color: var(--white);
    margin-bottom: 2rem;
    letter-spacing: -0.01em;
  }
  .hero-headline em {
    font-style: italic;
    color: var(--teal-l);
  }
  .hero-sub {
    font-size: 1.05rem;
    font-weight: 300;
    color: var(--text-d);
    max-width: 520px;
    line-height: 1.75;
    margin-bottom: 3rem;
  }
  .hero-actions { display: flex; gap: 1.2rem; align-items: center; flex-wrap: wrap; }
  .btn-primary {
    font-size: 0.8rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink);
    background: var(--teal-l);
    text-decoration: none;
    padding: 0.85rem 2rem;
    border-radius: 2px;
    transition: all 0.2s;
    border: 1px solid var(--teal-l);
  }
  .btn-primary:hover { background: var(--teal); border-color: var(--teal); }
  .btn-ghost {
    font-size: 0.8rem;
    font-weight: 400;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text-d);
    text-decoration: none;
    padding: 0.85rem 2rem;
    border-radius: 2px;
    border: 1px solid var(--rule);
    transition: all 0.2s;
  }
  .btn-ghost:hover { color: var(--teal-l); border-color: rgba(93,202,165,0.35); }

  /* Floating stat cards */
  .hero-stats {
    position: absolute;
    right: 4rem; top: 50%;
    transform: translateY(-50%);
    z-index: 1;
    display: flex; flex-direction: column; gap: 1rem;
  }
  .stat-card {
    background: rgba(26,36,32,0.8);
    border: 1px solid var(--rule);
    backdrop-filter: blur(8px);
    padding: 1.2rem 1.6rem;
    min-width: 200px;
    border-radius: 3px;
    animation: floatCard 6s ease-in-out infinite;
  }
  .stat-card:nth-child(2) { animation-delay: -2s; margin-left: 1.5rem; }
  .stat-card:nth-child(3) { animation-delay: -4s; }
  @keyframes floatCard {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
  }
  .stat-val {
    font-family: var(--serif);
    font-size: 2rem;
    font-weight: 600;
    color: var(--teal-l);
    line-height: 1;
    margin-bottom: 0.3rem;
  }
  .stat-label {
    font-size: 0.72rem;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
  }

  /* ── Section commons ── */
  section { position: relative; z-index: 1; }
  .container { max-width: 1120px; margin: 0 auto; padding: 0 4rem; }
  .section-pad { padding: 7rem 0; }
  .section-rule {
    width: 100%;
    height: 1px;
    background: var(--rule);
  }
  .section-eyebrow {
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 1.2rem;
    display: flex; align-items: center; gap: 0.8rem;
  }
  .section-eyebrow::before {
    content: '';
    display: block;
    width: 24px; height: 1px;
    background: var(--teal);
  }
  .section-title {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 300;
    color: var(--white);
    line-height: 1.15;
    margin-bottom: 1.4rem;
  }
  .section-title em { font-style: italic; color: var(--teal-l); }
  .section-body {
    font-size: 1rem;
    color: var(--text-d);
    max-width: 560px;
    line-height: 1.8;
  }

  /* ── What we do ── */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--rule);
    border: 1px solid var(--rule);
    margin-top: 4rem;
  }
  .service-card {
    background: var(--ink-2);
    padding: 2.5rem 2rem;
    transition: background 0.3s;
    cursor: default;
  }
  .service-card:hover { background: var(--ink-3); }
  .service-num {
    font-family: var(--serif);
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--teal-d);
    letter-spacing: 0.1em;
    margin-bottom: 1.6rem;
  }
  .service-title {
    font-family: var(--serif);
    font-size: 1.35rem;
    font-weight: 400;
    color: var(--white);
    line-height: 1.3;
    margin-bottom: 1rem;
  }
  .service-desc {
    font-size: 0.88rem;
    color: var(--text-d);
    line-height: 1.75;
    margin-bottom: 1.6rem;
  }
  .service-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .tag {
    font-size: 0.68rem;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--teal);
    border: 1px solid rgba(29,158,117,0.3);
    padding: 0.25rem 0.65rem;
    border-radius: 1px;
  }
  .service-dl {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    margin-top: 1.6rem;
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.09em;
    text-transform: uppercase;
    color: var(--teal-l);
    text-decoration: none;
    border-bottom: 1px solid rgba(93,202,165,0.25);
    padding-bottom: 2px;
    transition: border-color 0.2s, color 0.2s;
  }
  .service-dl:hover { color: var(--teal); border-color: rgba(93,202,165,0.6); }
  .service-dl svg { flex-shrink: 0; }

  /* ── How it works ── */
  .how-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
    margin-top: 4rem;
  }
  .how-steps { display: flex; flex-direction: column; gap: 0; }
  .how-step {
    display: flex; gap: 1.5rem;
    padding: 1.8rem 0;
    border-bottom: 1px solid var(--rule);
    align-items: flex-start;
  }
  .how-step:first-child { padding-top: 0; }
  .how-step:last-child { border-bottom: none; }
  .step-num {
    font-family: var(--serif);
    font-size: 2.2rem;
    font-weight: 300;
    color: var(--teal-d);
    line-height: 1;
    flex-shrink: 0;
    width: 48px;
    padding-top: 0.1rem;
  }
  .step-title {
    font-family: var(--serif);
    font-size: 1.1rem;
    font-weight: 400;
    color: var(--white);
    margin-bottom: 0.4rem;
  }
  .step-desc { font-size: 0.88rem; color: var(--text-d); line-height: 1.75; }
  .how-callout {
    background: var(--surface);
    border: 1px solid var(--rule);
    padding: 3rem;
    border-radius: 3px;
    position: relative;
    overflow: hidden;
  }
  .how-callout::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--teal-d), var(--blue-l));
  }
  .callout-quote {
    font-family: var(--serif);
    font-size: 1.55rem;
    font-weight: 300;
    font-style: italic;
    color: var(--white);
    line-height: 1.5;
    margin-bottom: 2rem;
  }
  .callout-meta { font-size: 0.8rem; color: var(--muted); letter-spacing: 0.05em; }
  .callout-stat {
    margin-top: 2rem;
    padding-top: 2rem;
    border-top: 1px solid var(--rule);
    display: flex; gap: 2rem;
  }
  .cs { }
  .cs-val {
    font-family: var(--serif);
    font-size: 1.8rem;
    font-weight: 600;
    color: var(--teal-l);
    line-height: 1;
    margin-bottom: 0.25rem;
  }
  .cs-label { font-size: 0.75rem; color: var(--muted); line-height: 1.4; }

  /* ── Work / case studies ── */
  .work-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1px;
    background: var(--rule);
    border: 1px solid var(--rule);
    margin-top: 4rem;
  }
  .work-card {
    background: var(--ink-2);
    padding: 2.8rem 2.4rem;
    transition: background 0.25s;
  }
  .work-card:hover { background: var(--ink-3); }
  .work-badge {
    display: inline-block;
    font-size: 0.68rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--teal);
    border: 1px solid rgba(29,158,117,0.3);
    padding: 0.25rem 0.7rem;
    border-radius: 1px;
    margin-bottom: 1.5rem;
  }
  .work-title {
    font-family: var(--serif);
    font-size: 1.25rem;
    font-weight: 400;
    color: var(--white);
    line-height: 1.35;
    margin-bottom: 0.8rem;
  }
  .work-desc { font-size: 0.88rem; color: var(--text-d); line-height: 1.75; margin-bottom: 1.8rem; }
  .work-outcome {
    font-size: 0.82rem;
    color: var(--teal-l);
    padding-top: 1.4rem;
    border-top: 1px solid var(--rule);
    line-height: 1.6;
  }
  .work-outcome strong { font-weight: 500; }

  /* ── CTA band ── */
  .cta-band {
    background: var(--surface);
    border-top: 1px solid var(--rule);
    border-bottom: 1px solid var(--rule);
    padding: 6rem 0;
    position: relative;
    overflow: hidden;
  }
  .cta-band::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 50% 100% at 50% 50%, rgba(29,158,117,0.08) 0%, transparent 60%);
  }
  .cta-inner {
    position: relative; z-index: 1;
    text-align: center;
    max-width: 640px;
    margin: 0 auto;
    padding: 0 2rem;
  }
  .cta-title {
    font-family: var(--serif);
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 300;
    color: var(--white);
    line-height: 1.2;
    margin-bottom: 1.2rem;
  }
  .cta-title em { font-style: italic; color: var(--teal-l); }
  .cta-sub { font-size: 0.95rem; color: var(--text-d); margin-bottom: 2.5rem; line-height: 1.75; }
  .cta-email {
    font-family: var(--serif);
    font-size: 1.2rem;
    font-weight: 300;
    color: var(--teal-l);
    text-decoration: none;
    border-bottom: 1px solid rgba(93,202,165,0.35);
    padding-bottom: 2px;
    transition: border-color 0.2s;
  }
  .cta-email:hover { border-color: var(--teal-l); }

  /* ── Footer ── */
  footer {
    padding: 3rem 4rem;
    border-top: 1px solid var(--rule);
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .footer-logo {
    font-family: var(--serif);
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--white);
  }
  .footer-logo span { color: var(--teal-l); }
  .footer-copy { font-size: 0.78rem; color: var(--muted); }
  .footer-links { display: flex; gap: 2rem; }
  .footer-links a {
    font-size: 0.75rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--teal-l); }

  /* ── Fade-in on scroll ── */
  .reveal {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }

  /* ── Responsive ── */
  @media (max-width: 1000px) {
    nav { padding: 1.2rem 2rem; }
    .nav-links { display: none; }
    .hero { padding: 7rem 2rem 4rem; flex-direction: column; }
    .hero-stats { position: static; transform: none; flex-direction: row; flex-wrap: wrap; margin-top: 3rem; }
    .stat-card { min-width: 140px; }
    .container { padding: 0 2rem; }
    .services-grid { grid-template-columns: 1fr; }
    .how-grid { grid-template-columns: 1fr; gap: 3rem; }
    .work-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 1.5rem; text-align: center; padding: 2.5rem 2rem; }
  }
</style>
</head>
<body>

<!-- Nav -->
<nav>
  <a class="nav-logo" href="#"><span>ID8</span> Advisors</a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#approach">Approach</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a class="nav-cta" href="#contact">Get in touch</a>
</nav>

<!-- Hero -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-content">
    <p class="hero-eyebrow">Energy transition advisory</p>
    <h1 class="hero-headline">Commercial clarity<br>for <em>complex</em><br>energy decisions.</h1>
    <p class="hero-sub">We help large-load customers, renewable developers, and strategic investors navigate power procurement, project origination, and portfolio acquisitions — with rigorous analysis and an independent perspective.</p>
    <div class="hero-actions">
      <a href="#services" class="btn-primary">Our services</a>
      <a href="#work" class="btn-ghost">See our work</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat-card">
      <div class="stat-val">$61</div>
      <div class="stat-label">per MWh value delta<br>from deliverability analysis</div>
    </div>
    <div class="stat-card">
      <div class="stat-val">Multi-GW</div>
      <div class="stat-label">portfolios screened<br>across U.S. markets</div>
    </div>
    <div class="stat-card">
      <div class="stat-val">3–4 wk</div>
      <div class="stat-label">to decision-quality<br>commercial analysis</div>
    </div>
  </div>
</section>

<div class="section-rule"></div>

<!-- Services -->
<section id="services" class="section-pad">
  <div class="container">
    <p class="section-eyebrow reveal">What we do</p>
    <h2 class="section-title reveal reveal-delay-1">Three service lines.<br><em>One commercial lens.</em></h2>
    <p class="section-body reveal reveal-delay-2">We work at the intersection of energy economics, regulatory complexity, and market structure — where most of the value is created or lost.</p>

    <div class="services-grid">
      <div class="service-card reveal">
        <div class="service-num">01</div>
        <h3 class="service-title">Large-Load Power Procurement</h3>
        <p class="service-desc">Structured cost management and supply strategy for industrial customers and data centers in regulated utility territories where retail choice is unavailable.</p>
        <div class="service-tags">
          <span class="tag">Tariff optimization</span>
          <span class="tag">Financial hedging</span>
          <span class="tag">Capacity planning</span>
          <span class="tag">Bilateral supply</span>
        </div>
        <a class="service-dl" href="Power_Cost_Diagnostic_Proposal.docx" download>
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6.5 1v7M3.5 5.5l3 3 3-3M2 10.5h9" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          Download engagement scope
        </a>
      </div>
      <div class="service-card reveal reveal-delay-1">
        <div class="service-num">02</div>
        <h3 class="service-title">Project Development & Origination</h3>
        <p class="service-desc">Commercial positioning for late-stage solar, storage, and hybrid assets — clarifying offtake pathways, value stacks, and the risks that matter most before buyer conversations begin.</p>
        <div class="service-tags">
          <span class="tag">Offtake strategy</span>
          <span class="tag">Deliverability analysis</span>
          <span class="tag">Buyer fit</span>
          <span class="tag">CAISO · MISO · SPP</span>
        </div>
        <a class="service-dl" href="Commercial_Positioning_Sprint_Proposal.docx" download>
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6.5 1v7M3.5 5.5l3 3 3-3M2 10.5h9" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          Download engagement scope
        </a>
      </div>
      <div class="service-card reveal reveal-delay-2">
        <div class="service-num">03</div>
        <h3 class="service-title">M&A Portfolio Screening</h3>
        <p class="service-desc">Independent commercial due diligence on renewable development portfolios — separating near-term acquisition platforms from option value before capital is committed.</p>
        <div class="service-tags">
          <span class="tag">Portfolio screening</span>
          <span class="tag">Return modeling</span>
          <span class="tag">Bankability assessment</span>
          <span class="tag">Deal structuring</span>
        </div>
        <a class="service-dl" href="MA_Portfolio_Screening_Proposal.docx" download>
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6.5 1v7M3.5 5.5l3 3 3-3M2 10.5h9" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          Download engagement scope
        </a>
      </div>
    </div>
  </div>
</section>

<div class="section-rule"></div>

<!-- Approach -->
<section id="approach" class="section-pad">
  <div class="container">
    <div class="how-grid">
      <div>
        <p class="section-eyebrow reveal">How we work</p>
        <h2 class="section-title reveal reveal-delay-1">Structured analysis.<br><em>Actionable output.</em></h2>
        <div class="how-steps">
          <div class="how-step reveal">
            <div class="step-num">01</div>
            <div>
              <div class="step-title">Assess commercial realism</div>
              <p class="step-desc">Map the asset or situation against actual market conditions — active procurement, bilateral buyer appetite, regulatory constraints, and revenue stack assumptions that hold under scrutiny.</p>
            </div>
          </div>
          <div class="how-step reveal reveal-delay-1">
            <div class="step-num">02</div>
            <div>
              <div class="step-title">Identify what actually moves value</div>
              <p class="step-desc">Surface the two or three factors with the largest impact on economics, bankability, or execution risk — and quantify them clearly enough to support a real decision.</p>
            </div>
          </div>
          <div class="how-step reveal reveal-delay-2">
            <div class="step-num">03</div>
            <div>
              <div class="step-title">Deliver a clear path forward</div>
              <p class="step-desc">Every engagement ends with a specific recommendation — not a menu of options. A prioritized action path, a phased strategy, or a selective investment thesis.</p>
            </div>
          </div>
        </div>
      </div>
      <div class="reveal reveal-delay-1">
        <div class="how-callout">
          <p class="callout-quote">"Commercial value in CAISO is not created by interconnection position alone. It is created by how well the project is structured around deliverability, congestion, and buyer fit."</p>
          <p class="callout-meta">— ID8 Advisors, East County Substation engagement</p>
          <div class="callout-stat">
            <div class="cs">
              <div class="cs-val">$165</div>
              <div class="cs-label">Indicative value<br>with deliverability ($/MWh)</div>
            </div>
            <div class="cs">
              <div class="cs-val">$104</div>
              <div class="cs-label">Indicative value<br>without deliverability ($/MWh)</div>
            </div>
            <div class="cs">
              <div class="cs-val">13.2%</div>
              <div class="cs-label">Modeled levered IRR<br>with deliverability</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="section-rule"></div>

<!-- Work -->
<section id="work" class="section-pad">
  <div class="container">
    <p class="section-eyebrow reveal">Selected work</p>
    <h2 class="section-title reveal reveal-delay-1">Engagements that<br><em>changed the decision.</em></h2>

    <div class="work-grid">
      <div class="work-card reveal">
        <span class="work-badge">Large-load procurement</span>
        <h3 class="work-title">Power Cost Management Strategy — Regulated Utility Territory</h3>
        <p class="work-desc">A large-load industrial customer needed a practical path to manage electricity cost and wholesale market exposure in a regulated service territory with no retail choice. We assessed the tariff framework, evaluated procurement pathways, and built a phased resource strategy spanning multiple generation technologies.</p>
        <p class="work-outcome"><strong>Outcome:</strong> Identified near-term tariff and hedge opportunities. Delivered a phased procurement roadmap linking cost management to load growth and long-term supply security.</p>
      </div>
      <div class="work-card reveal reveal-delay-1">
        <span class="work-badge">Project origination · CAISO</span>
        <h3 class="work-title">CAISO Hybrid Commercialization — SDG&E East County Substation</h3>
        <p class="work-desc">A 139.9 MWac solar + 4-hour BESS project at SDG&E's East County node needed a sharper commercial strategy before offtake discussions. We evaluated buyer segments, quantified the deliverability impact, and built a prioritized commercialization framework.</p>
        <p class="work-outcome"><strong>Outcome:</strong> $61/MWh value difference between deliverable and non-deliverable outcomes quantified. LSE-oriented strategy recommended, investor narrative strengthened.</p>
      </div>
      <div class="work-card reveal">
        <span class="work-badge">BESS retrofit · MISO</span>
        <h3 class="work-title">PV-to-Hybrid Storage Retrofit Program</h3>
        <p class="work-desc">A utility-scale PV developer across multiple MISO states needed a repeatable approach to add battery storage to existing interconnections — without triggering restudy or exceeding POI export limits. We built a standardized AC-coupled retrofit template with a controls-first operating envelope.</p>
        <p class="work-outcome"><strong>Outcome:</strong> Scalable retrofit playbook deployed. PV-only assets repositioned as dispatchable, contractable hybrids without changing the POI export cap.</p>
      </div>
      <div class="work-card reveal reveal-delay-1">
        <span class="work-badge">M&A advisory</span>
        <h3 class="work-title">Multi-GW Renewable Portfolio Acquisition Screening</h3>
        <p class="work-desc">A strategic renewable investor evaluating a multi-gigawatt solar and storage development portfolio across western and central U.S. markets needed a commercial view on acquisition timing and structure. We screened portfolio quality, tested commercial realism, and modeled return ranges across the asset set.</p>
        <p class="work-outcome"><strong>Outcome:</strong> Higher-conviction subset identified. Selective origination strategy recommended over broad portfolio takeout. Milestone-based entry structure proposed.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-rule"></div>

<!-- CTA -->
<section id="contact" class="cta-band">
  <div class="cta-inner">
    <p class="section-eyebrow reveal" style="justify-content:center;">Get started</p>
    <h2 class="cta-title reveal reveal-delay-1">Ready to bring <em>clarity</em><br>to your next decision?</h2>
    <p class="cta-sub reveal reveal-delay-2">Most engagements begin with a 30-minute call. We'll tell you quickly whether we're the right fit and what a scoped engagement would look like.</p>
    <a href="mailto:beau@id8advisors.com" class="cta-email reveal reveal-delay-3">beau@id8advisors.com</a>
  </div>
</section>

<!-- Footer -->
<footer>
  <div class="footer-logo"><span>ID8</span> Advisors</div>
  <p class="footer-copy">© 2026 ID8 Advisors. Independent energy transition advisory.</p>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#work">Work</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  const observer = new Intersedvisors_landing (1).html…]()
