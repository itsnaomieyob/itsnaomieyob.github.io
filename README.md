# itsnaomieyob.github.io
My Personal Portfolio Site
index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Naomi Eyob — Workplace Experience Manager, Gen</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=Inter:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #13151A;
    --bg-alt: #1A1D24;
    --surface: #20232B;
    --line: rgba(242,241,236,0.12);
    --line-strong: rgba(242,241,236,0.22);
    --text: #F3F1EA;
    --text-dim: #9BA1AD;
    --text-faint: #6B7280;
    --accent: #C9A227;
    --accent-soft: rgba(201,162,39,0.14);
    --accent-line: rgba(201,162,39,0.4);
    --radius: 2px;
    --maxw: 1200px;
  }

  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important;}
  }

  body{
    background:var(--bg);
    color:var(--text);
    font-family:'Inter',sans-serif;
    font-weight:400;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }

  a{color:inherit;text-decoration:none;}
  ul{list-style:none;}

  ::selection{background:var(--accent); color:#13151A;}

  :focus-visible{
    outline:2px solid var(--accent);
    outline-offset:3px;
  }

  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 48px;}
  @media (max-width:768px){ .wrap{padding:0 24px;} }

  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--accent);
    display:flex;
    align-items:center;
    gap:10px;
    margin-bottom:18px;
  }
  .eyebrow::before{
    content:"";
    display:inline-block;
    width:18px;height:1px;
    background:var(--accent);
  }

  h1,h2,h3{
    font-family:'Archivo Black', sans-serif;
    font-weight:400;
    text-transform:uppercase;
    line-height:1.02;
    letter-spacing:-0.01em;
  }

  /* ---------- NAV ---------- */
  header{
    position:fixed; top:0; left:0; right:0; z-index:100;
    background:rgba(19,21,26,0.85);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{
    max-width:var(--maxw); margin:0 auto; padding:20px 48px;
    display:flex; align-items:center; justify-content:space-between;
  }
  @media (max-width:768px){ .nav-inner{padding:18px 24px;} }
  .brand{
    font-family:'Archivo Black', sans-serif;
    font-size:15px;
    letter-spacing:0.02em;
    display:flex; align-items:baseline; gap:10px;
  }
  .brand small{
    font-family:'IBM Plex Mono', monospace;
    font-size:10px;
    color:var(--accent);
    font-weight:500;
    letter-spacing:0.1em;
    text-transform:uppercase;
  }
  nav.links{display:flex; gap:36px;}
  nav.links a{
    font-size:13px; letter-spacing:0.04em; text-transform:uppercase;
    color:var(--text-dim); font-weight:600;
    transition:color .2s ease;
    padding:4px 0;
    border-bottom:1px solid transparent;
  }
  nav.links a:hover{ color:var(--text); border-color:var(--accent-line); }
  @media (max-width:900px){ nav.links{display:none;} }
  .menu-btn{
    display:none;
    background:none;border:1px solid var(--line-strong);
    color:var(--text); width:38px; height:38px; border-radius:var(--radius);
    cursor:pointer; align-items:center; justify-content:center;
  }
  @media (max-width:900px){ .menu-btn{display:flex;} }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    min-height:100vh;
    display:flex; align-items:center;
    padding:140px 0 100px;
    overflow:hidden;
    background:
      linear-gradient(180deg, rgba(19,21,26,0.2), rgba(19,21,26,0.92) 78%),
      repeating-linear-gradient(0deg, transparent, transparent 39px, rgba(242,241,236,0.035) 40px),
      repeating-linear-gradient(90deg, transparent, transparent 39px, rgba(242,241,236,0.035) 40px);
    background-color:var(--bg);
  }
  .hero-inner{
    max-width:var(--maxw); margin:0 auto; padding:0 48px; width:100%;
  }
  @media (max-width:768px){ .hero-inner{padding:0 24px;} }
  .hero h1{
    font-size:clamp(40px, 6.6vw, 92px);
    max-width:16ch;
    margin-bottom:28px;
  }
  .hero h1 .accent-word{ color:var(--accent); }
  .hero p.sub{
    font-size:19px;
    color:var(--text-dim);
    max-width:640px;
    margin-bottom:44px;
    font-weight:400;
  }
  .cta-row{display:flex; gap:16px; flex-wrap:wrap;}
  .btn{
    font-family:'IBM Plex Mono', monospace;
    font-size:12.5px; letter-spacing:0.06em; text-transform:uppercase;
    padding:15px 26px;
    border-radius:var(--radius);
    display:inline-flex; align-items:center; gap:10px;
    transition:all .2s ease;
    font-weight:500;
  }
  .btn-primary{ background:var(--accent); color:#13151A; }
  .btn-primary:hover{ background:#DDBB3E; }
  .btn-ghost{ border:1px solid var(--line-strong); color:var(--text); }
  .btn-ghost:hover{ border-color:var(--accent); color:var(--accent); }

  .hero-stats{
    margin-top:88px;
    display:grid; grid-template-columns:repeat(4,1fr); gap:0;
    border-top:1px solid var(--line);
  }
  .hero-stats div{
    padding:22px 24px 0 0; border-right:1px solid var(--line);
  }
  .hero-stats div:last-child{border-right:none;}
  @media (max-width:768px){
    .hero-stats{grid-template-columns:1fr 1fr; row-gap:24px;}
    .hero-stats div{border-right:none; padding-right:16px;}
  }
  .stat-num{
    font-family:'IBM Plex Mono', monospace;
    font-size:30px; color:var(--accent); font-weight:600;
  }
  .stat-label{
    font-size:12px; color:var(--text-faint); text-transform:uppercase;
    letter-spacing:0.06em; margin-top:6px;
  }

  /* ---------- SECTION SHELL ---------- */
  section{ padding:120px 0; border-bottom:1px solid var(--line); }
  @media (max-width:768px){ section{padding:80px 0;} }
  section.alt{ background:var(--bg-alt); }
  .section-head{
    display:flex; justify-content:space-between; align-items:flex-end;
    gap:40px; margin-bottom:64px; flex-wrap:wrap;
  }
  .section-head h2{ font-size:clamp(28px,3.4vw,44px); max-width:14ch; }
  .section-head p{ color:var(--text-dim); max-width:38ch; font-size:15px; }

  /* ---------- WHO I AM ---------- */
  .about-grid{
    display:grid; grid-template-columns:1.3fr 1fr; gap:80px;
  }
  @media (max-width:900px){ .about-grid{grid-template-columns:1fr; gap:48px;} }
  .about-grid p{ font-size:18px; color:#D7D5CE; margin-bottom:20px; max-width:60ch;}
  .about-grid p.lede{ font-size:23px; color:var(--text); font-weight:500; line-height:1.45; }
  .ledger{ border-top:1px solid var(--line); }
  .ledger-row{
    display:flex; justify-content:space-between; padding:18px 0;
    border-bottom:1px solid var(--line);
    font-family:'IBM Plex Mono', monospace; font-size:13px;
  }
  .ledger-row span:first-child{ color:var(--text-dim); }
  .ledger-row span:last-child{ color:var(--text); font-weight:500; text-align:right; }

  /* ---------- PILLARS ---------- */
  .pillar-grid{
    display:grid; grid-template-columns:repeat(2,1fr); gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  @media (max-width:768px){ .pillar-grid{grid-template-columns:1fr;} }
  .pillar{
    background:var(--bg); padding:44px 40px;
    transition:background .2s ease;
  }
  .pillar:hover{ background:var(--surface); }
  .pillar .num{
    font-family:'IBM Plex Mono', monospace; color:var(--accent);
    font-size:13px; margin-bottom:20px; display:block;
  }
  .pillar h3{
    font-family:'Inter',sans-serif; font-weight:700; text-transform:none;
    font-size:20px; margin-bottom:12px; letter-spacing:0;
  }
  .pillar p{ color:var(--text-dim); font-size:14.5px; max-width:38ch; }

  /* ---------- SKILLS ---------- */
  .skill-cols{
    display:grid; grid-template-columns:repeat(4,1fr); gap:40px;
  }
  @media (max-width:900px){ .skill-cols{grid-template-columns:1fr 1fr;} }
  @media (max-width:520px){ .skill-cols{grid-template-columns:1fr;} }
  .skill-col h4{
    font-family:'IBM Plex Mono', monospace; font-size:11.5px;
    text-transform:uppercase; letter-spacing:0.08em; color:var(--accent);
    margin-bottom:18px; padding-bottom:14px; border-bottom:1px solid var(--line-strong);
  }
  .skill-col li{
    font-size:14px; color:var(--text-dim); padding:7px 0;
  }

  /* ---------- CASE STUDIES ---------- */
  .case{
    padding:80px 0; border-bottom:1px solid var(--line);
    display:grid; grid-template-columns:0.85fr 1.15fr; gap:64px;
  }
  .case:last-child{border-bottom:none;}
  @media (max-width:900px){ .case{grid-template-columns:1fr; gap:36px;} }

  .case-left .case-tag{
    font-family:'IBM Plex Mono', monospace; font-size:12px; color:var(--accent);
    letter-spacing:0.08em; margin-bottom:16px; display:block;
  }
  .case-left h3{
    font-family:'Archivo Black', sans-serif; font-size:clamp(24px,2.6vw,32px);
    text-transform:none; letter-spacing:-0.01em; line-height:1.1; margin-bottom:22px;
    max-width:15ch;
  }
  .case-block{ margin-bottom:22px; }
  .case-block h5{
    font-family:'IBM Plex Mono', monospace; font-size:11px; text-transform:uppercase;
    letter-spacing:0.08em; color:var(--text-faint); margin-bottom:8px;
  }
  .case-block p{ font-size:15px; color:#CFCDC6; max-width:46ch; }

  .case-steps{ counter-reset:step; margin-bottom:32px; }
  .case-steps li{
    counter-increment:step;
    position:relative;
    padding-left:36px;
    padding-bottom:16px;
    font-size:14.5px; color:var(--text-dim);
    border-left:1px solid var(--line);
    margin-left:9px;
  }
  .case-steps li:last-child{ border-color:transparent; padding-bottom:0;}
  .case-steps li::before{
    content:counter(step);
    position:absolute; left:-9px; top:-2px;
    width:18px; height:18px; border-radius:50%;
    background:var(--bg-alt); border:1px solid var(--accent-line);
    color:var(--accent);
    font-family:'IBM Plex Mono', monospace; font-size:10px; font-weight:600;
    display:flex; align-items:center; justify-content:center;
  }
  section.alt .case-steps li::before{ background:var(--surface); }

  .impact-panel{
    background:var(--surface);
    border:1px solid var(--line-strong);
    border-radius:var(--radius);
    padding:28px 30px;
    position:relative;
    overflow:hidden;
  }
  .impact-panel h5{
    font-family:'IBM Plex Mono', monospace; font-size:11px; text-transform:uppercase;
    letter-spacing:0.08em; color:var(--accent); margin-bottom:16px;
  }
  .impact-stats{ display:flex; flex-wrap:wrap; gap:28px; margin-bottom:18px;}
  .impact-stat .num{
    font-family:'IBM Plex Mono', monospace; font-size:26px; color:var(--text); font-weight:600;
  }
  .impact-stat .label{ font-size:12px; color:var(--text-faint); margin-top:4px; max-width:16ch;}
  .impact-panel p.note{ font-size:14px; color:var(--text-dim); border-top:1px solid var(--line); padding-top:16px; }

  .artifact-tag{
    margin-top:18px;
    font-family:'IBM Plex Mono', monospace; font-size:11.5px;
    color:var(--text-faint); border:1px dashed var(--line-strong);
    padding:12px 14px; border-radius:var(--radius);
  }

  .stamp{
    position:absolute; top:20px; right:22px;
    width:64px; height:64px;
    border:1px solid var(--accent-line);
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    transform:rotate(-14deg);
    opacity:0.9;
  }
  .stamp::before{
    content:"";
    position:absolute; inset:6px;
    border:1px dashed var(--accent-line);
    border-radius:50%;
  }
  .stamp span{
    font-family:'IBM Plex Mono', monospace;
    font-size:8.5px; letter-spacing:0.06em; color:var(--accent);
    text-transform:uppercase; text-align:center; line-height:1.3;
  }
  @media (max-width:600px){ .stamp{width:50px; height:50px; top:14px; right:14px;} .stamp span{font-size:7px;} }

  /* ---------- WHY GEN ---------- */
  .why-gen{ display:grid; grid-template-columns:0.9fr 1.1fr; gap:72px; align-items:start;}
  @media (max-width:900px){ .why-gen{grid-template-columns:1fr; gap:40px;} }
  .why-gen blockquote{
    font-family:'Archivo Black', sans-serif;
    font-size:clamp(22px,2.6vw,30px);
    text-transform:none; line-height:1.25; letter-spacing:-0.01em;
    color:var(--text); max-width:16ch;
  }
  .why-gen blockquote .accent-word{ color:var(--accent); }
  .why-copy p{ font-size:16px; color:#D2D0C9; margin-bottom:20px; max-width:58ch;}
  .why-copy p strong{ color:var(--text); font-weight:600; }

  /* ---------- CONTACT ---------- */
  .contact-grid{
    display:grid; grid-template-columns:1.1fr 0.9fr; gap:64px; align-items:end;
  }
  @media (max-width:900px){ .contact-grid{grid-template-columns:1fr; gap:40px;} }
  .contact-grid h2{ font-size:clamp(34px,5vw,64px); max-width:12ch; margin-bottom:24px;}
  .contact-links{ display:flex; flex-direction:column; gap:0; border-top:1px solid var(--line);}
  .contact-link-row{
    display:flex; justify-content:space-between; align-items:center;
    padding:20px 0; border-bottom:1px solid var(--line);
  }
  .contact-link-row span:first-child{
    font-family:'IBM Plex Mono', monospace; font-size:11px; text-transform:uppercase;
    letter-spacing:0.08em; color:var(--text-faint);
  }
  .contact-link-row a{
    font-size:16px; font-weight:600; transition:color .2s ease;
  }
  .contact-link-row a:hover{ color:var(--accent); }

  footer{
    padding:36px 0; text-align:center;
  }
  footer p{ font-family:'IBM Plex Mono', monospace; font-size:11.5px; color:var(--text-faint); }

  /* mobile menu */
  .mobile-menu{
    position:fixed; inset:0; background:var(--bg); z-index:200;
    display:flex; flex-direction:column; align-items:flex-start; justify-content:center;
    padding:48px; gap:28px; transform:translateY(-100%);
    transition:transform .3s ease;
  }
  .mobile-menu.open{ transform:translateY(0); }
  .mobile-menu a{ font-family:'Archivo Black', sans-serif; font-size:32px; text-transform:uppercase; color:var(--text);}
  .mobile-menu-close{
    position:absolute; top:20px; right:24px;
    background:none;border:1px solid var(--line-strong); color:var(--text);
    width:38px; height:38px; border-radius:var(--radius); cursor:pointer;
  }

  .reveal{ opacity:0; transform:translateY(18px); transition:opacity .6s ease, transform .6s ease; }
  .reveal.visible{ opacity:1; transform:translateY(0); }
</style>
</head>
<body>

<header>
  <div class="nav-inner">
    <div class="brand">NAOMI EYOB <small>→ Gen, NYC</small></div>
    <nav class="links">
      <a href="#about">About</a>
      <a href="#pillars">Approach</a>
      <a href="#work">Case Studies</a>
      <a href="#why-gen">Why Gen</a>
      <a href="#contact">Contact</a>
    </nav>
    <button class="menu-btn" id="menuBtn" aria-label="Open menu">☰</button>
  </div>
</header>

<div class="mobile-menu" id="mobileMenu">
  <button class="mobile-menu-close" id="menuClose" aria-label="Close menu">✕</button>
  <a href="#about">About</a>
  <a href="#pillars">Approach</a>
  <a href="#work">Case Studies</a>
  <a href="#why-gen">Why Gen</a>
  <a href="#contact">Contact</a>
</div>

<!-- HERO -->
<section class="hero" id="home" style="border-bottom:1px solid var(--line); padding-bottom:0;">
  <div class="hero-inner">
    <div class="eyebrow">Workplace Experience Manager — Candidate</div>
    <h1>The physical layer of <span class="accent-word">trust.</span></h1>
    <p class="sub">Nine years leading workplace operations for organizations where the details matter — now applying that same standard of care to Gen's NYC site, where the mission is protecting how nearly 500 million people live their digital and financial lives.</p>
    <div class="cta-row">
      <a href="#work" class="btn btn-primary">View Case Studies →</a>
      <a href="mailto:naomi.eyob@gmail.com" class="btn btn-ghost">Get In Touch</a>
    </div>
    <div class="hero-stats">
      <div><div class="stat-num">9+</div><div class="stat-label">Years in Workplace Ops</div></div>
      <div><div class="stat-num">$55K+</div><div class="stat-label">Budget Administered</div></div>
      <div><div class="stat-num">200+</div><div class="stat-label">Employees Supported</div></div>
      <div><div class="stat-num">80+</div><div class="stat-label">Annual Events Led</div></div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="wrap">
    <div class="about-grid">
      <div class="reveal">
        <div class="eyebrow">Who I Am</div>
        <p class="lede">A hands-on operator who owns the full on-site experience — not just the ticket queue.</p>
        <p>My background is in hospitality management, where things go sideways constantly and you learn to think on your feet and figure it out without waiting for someone to hand you a solution. That instinct carried directly into my current role at Compass, where I've led workplace operations well beyond my title: identifying a rooftop HVAC unit that had never been properly installed, initiating a six-month infrastructure upgrade, building 80+ employee events and programs, and owning communications to 200+ employees.</p>
        <p>I recently built a Gemini-powered budget tool because I wanted visibility into spend <em>before</em> problems surfaced — not after. That's the posture I bring to every part of the job: scrappy, accountable, and thinking several steps ahead of the ticket.</p>
      </div>
      <div class="reveal">
        <div class="ledger">
          <div class="ledger-row"><span>Current Title</span><span>Workplace Experience Coordinator & Regional Communications Lead, Compass</span></div>
          <div class="ledger-row"><span>Tenure</span><span>Jul 2021 – Present</span></div>
          <div class="ledger-row"><span>Prior</span><span>Bar Manager, Barrel + Crow</span></div>
          <div class="ledger-row"><span>Education</span><span>B.A. Communications, University of Maryland</span></div>
          <div class="ledger-row"><span>Certification</span><span>Google Project Management Cert. (Exp. Sept 2026)</span></div>
          <div class="ledger-row"><span>Systems</span><span>Brivo · Envoy · Zendesk · Workday · Coupa · Concur</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PILLARS -->
<section class="alt" id="pillars">
  <div class="wrap">
    <div class="section-head">
      <h2>How I Operate</h2>
      <p>Four disciplines, one standard: the workplace should never be the reason something goes wrong.</p>
    </div>
    <div class="pillar-grid reveal">
      <div class="pillar">
        <span class="num">01 / Space</span>
        <h3>Space Management & Real Estate</h3>
        <p>Space planning, seating logistics, and desk allocation for flexible hybrid models — plus direct landlord and property management relationships to resolve build-out and lease-obligation issues.</p>
      </div>
      <div class="pillar">
        <span class="num">02 / Process</span>
        <h3>Operational Efficiency & Process Optimization</h3>
        <p>SOPs, ticketing workflows, and self-built tooling — including a Gemini-powered budget dashboard and a new accountability-driven check-confirmation process.</p>
      </div>
      <div class="pillar">
        <span class="num">03 / Vendor</span>
        <h3>Vendor & Budget Management</h3>
        <p>End-to-end contractor oversight across cleaning, maintenance, and food programs — negotiating contracts, enforcing SLAs, and administering a $55K+ annual budget.</p>
      </div>
      <div class="pillar">
        <span class="num">04 / Culture</span>
        <h3>Workplace Experience & Culture</h3>
        <p>80+ employee events annually, onboarding, and internal communications to 200+ employees — building environments people actually want to work in.</p>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="wrap">
    <div class="section-head">
      <h2>Skill Snapshot</h2>
      <p>The systems and disciplines behind the day-to-day.</p>
    </div>
    <div class="skill-cols reveal">
      <div class="skill-col">
        <h4>Operations & Facilities</h4>
        <ul>
          <li>Facilities Issue Resolution</li>
          <li>Space Activation & Planning</li>
          <li>Health & Safety Compliance</li>
          <li>Access Control & Security</li>
        </ul>
      </div>
      <div class="skill-col">
        <h4>Vendor & Budget</h4>
        <ul>
          <li>Contract Negotiation</li>
          <li>SLA Oversight</li>
          <li>Budget Administration & Forecasting</li>
          <li>Invoice Compliance & PO Creation</li>
        </ul>
      </div>
      <div class="skill-col">
        <h4>Experience & Culture</h4>
        <ul>
          <li>Event Planning & Execution</li>
          <li>Food Program & Catering Mgmt</li>
          <li>Internal Communications</li>
          <li>Onboarding & Team Development</li>
        </ul>
      </div>
      <div class="skill-col">
        <h4>Systems & Tools</h4>
        <ul>
          <li>Brivo · Envoy · Zendesk</li>
          <li>Workday · Coupa · Concur</li>
          <li>Monday.com · Power BI</li>
          <li>AI-Enabled Productivity Tools</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- CASE STUDIES -->
<section class="alt" id="work">
  <div class="wrap">
    <div class="section-head">
      <h2>Selected Work</h2>
      <p>Five problems I found, owned, and closed out — with the numbers to prove it.</p>
    </div>

    <!-- CASE 1: HVAC -->
    <div class="case reveal">
      <div class="case-left">
        <span class="case-tag">Case 01 — Space & Real Estate</span>
        <h3>Recovering Four Years of Missed Infrastructure</h3>
        <div class="case-block">
          <h5>The Problem</h5>
          <p>A rooftop HVAC unit had never been properly installed — an undetected, landlord-responsibility gap that sat unresolved for four years, putting a 100+ agent office at risk of a major failure with zero warning.</p>
        </div>
        <div class="case-block">
          <h5>My Role & Strategy</h5>
          <p>I caught the gap during routine facilities diagnostics, built the case for the landlord and property manager (Kimco), and refused to accept the first number that came back.</p>
        </div>
      </div>
      <div class="case-right">
        <ol class="case-steps">
          <li>Diagnosed the missing unit and documented four years of undetected risk.</li>
          <li>Built the full scope of work and brought it to the landlord and property manager.</li>
          <li>Solicited competitive vendor pricing instead of accepting the first quote.</li>
          <li>Negotiated final scope and managed installation logistics end-to-end.</li>
        </ol>
        <div class="impact-panel">
          <div class="stamp"><span>Resolved<br>0 Disruption</span></div>
          <h5>The Impact</h5>
          <div class="impact-stats">
            <div class="impact-stat"><div class="num">$9,000</div><div class="label">Saved vs. initial $30K quote</div></div>
            <div class="impact-stat"><div class="num">30%</div><div class="label">Cost reduction via vendor solicitation</div></div>
            <div class="impact-stat"><div class="num">0</div><div class="label">Days of disruption to agents</div></div>
          </div>
          <p class="note">Full rooftop replacement executed for $21,000 against a $30,000 initial quote — with zero impact to daily agent operations throughout.</p>
        </div>
        <div class="artifact-tag">Artifact Showcase → Insert vendor bid comparison / scope-of-work summary table</div>
      </div>
    </div>

    <!-- CASE 2: Budget tool -->
    <div class="case reveal">
      <div class="case-left">
        <span class="case-tag">Case 02 — Process Optimization</span>
        <h3>Building Real-Time Visibility Into a $55K Budget</h3>
        <div class="case-block">
          <h5>The Problem</h5>
          <p>Budget data lived inside a master tracker split by regional tab. Getting a read on weekly spend meant digging — so overages surfaced only after the money was already gone.</p>
        </div>
        <div class="case-block">
          <h5>My Role & Strategy</h5>
          <p>I built a Gemini-powered dashboard for at-a-glance weekly visibility, and separately designed a new check-confirmation process to create real accountability between employees and the stakeholders being paid.</p>
        </div>
      </div>
      <div class="case-right">
        <ol class="case-steps">
          <li>Mapped weekly spend categories across the regional budget tracker.</li>
          <li>Built a Gemini-powered tool summarizing weekly cost trends at a glance.</li>
          <li>Designed a check-confirmation process with clear accountability checkpoints.</li>
          <li>Rolled the tool and process out across office leads.</li>
        </ol>
        <div class="impact-panel">
          <div class="stamp"><span>Verified<br>Weekly</span></div>
          <h5>The Impact</h5>
          <div class="impact-stats">
            <div class="impact-stat"><div class="num">20+ min</div><div class="label">Saved per check, weekly</div></div>
            <div class="impact-stat"><div class="num">100%</div><div class="label">Of offices moved to underspend</div></div>
          </div>
          <p class="note">Every office using the tool shifted to underspend against budget — and the new check-confirmation process built a documented accountability trail between employees and paid stakeholders.</p>
        </div>
        <div class="artifact-tag">Artifact Showcase → Insert budget dashboard screenshot / check-confirmation workflow diagram</div>
      </div>
    </div>

    <!-- CASE 3: Network -->
    <div class="case reveal">
      <div class="case-left">
        <span class="case-tag">Case 03 — Space & Real Estate</span>
        <h3>Doubling Site Connectivity Through Cross-Functional Coordination</h3>
        <div class="case-block">
          <h5>The Problem</h5>
          <p>A long-standing bandwidth ceiling — running in the low 30 Mbps range — was quietly constraining day-to-day workflow for a 100+ agent office.</p>
        </div>
        <div class="case-block">
          <h5>My Role & Strategy</h5>
          <p>I initiated and co-led a six-month upgrade, coordinating internal networking teams, National Workplace Operations, property management, and outside vendors.</p>
        </div>
      </div>
      <div class="case-right">
        <ol class="case-steps">
          <li>Diagnosed the root cause of the persistent bandwidth ceiling.</li>
          <li>Aligned internal IT, National Workplace Operations, and property management.</li>
          <li>Managed outside vendor scheduling and install logistics over six months.</li>
          <li>Tested and validated performance post-installation.</li>
        </ol>
        <div class="impact-panel">
          <div class="stamp"><span>Resolved<br>6 Months</span></div>
          <h5>The Impact</h5>
          <div class="impact-stats">
            <div class="impact-stat"><div class="num">~2x</div><div class="label">Connectivity, ~30 → ~60 Mbps</div></div>
            <div class="impact-stat"><div class="num">100+</div><div class="label">Agents on uninterrupted workflow</div></div>
          </div>
          <p class="note">Site bandwidth effectively doubled, removing a long-standing bottleneck and ensuring uninterrupted workflow for the full office.</p>
        </div>
        <div class="artifact-tag">Artifact Showcase → Insert before/after bandwidth chart</div>
      </div>
    </div>

    <!-- CASE 4: Events -->
    <div class="case reveal">
      <div class="case-left">
        <span class="case-tag">Case 04 — Workplace Experience & Culture</span>
        <h3>Scaling Culture: 80+ Events, 90% Average Engagement</h3>
        <div class="case-block">
          <h5>The Problem</h5>
          <p>A growing, hybrid population of 200+ agents needed consistent, high-quality touchpoints to build culture and connection — not a handful of one-off events.</p>
        </div>
        <div class="case-block">
          <h5>My Role & Strategy</h5>
          <p>I own the full workplace events calendar and led Summer of Success, a six-week engagement program for 400+ agents spanning venue sourcing, vendor coordination, and speaker logistics.</p>
        </div>
      </div>
      <div class="case-right">
        <ol class="case-steps">
          <li>Built an annual calendar: quarterly activations, monthly lunch & learns, regional programs.</li>
          <li>Sourced venues, vendors, and speakers for each program.</li>
          <li>Executed on-site, end-to-end, including Summer of Success for 400+ agents.</li>
          <li>Collected post-event feedback surveys and iterated on the format.</li>
        </ol>
        <div class="impact-panel">
          <div class="stamp"><span>Verified<br>Feedback</span></div>
          <h5>The Impact</h5>
          <div class="impact-stats">
            <div class="impact-stat"><div class="num">80+</div><div class="label">Events executed annually</div></div>
            <div class="impact-stat"><div class="num">90%</div><div class="label">Avg. post-event survey score</div></div>
            <div class="impact-stat"><div class="num">400+</div><div class="label">Agents in Summer of Success</div></div>
          </div>
          <p class="note">Post-event surveys across all 80+ annual events averaged a 90% success rate spanning turnout and participation.</p>
        </div>
        <div class="artifact-tag">Artifact Showcase → Insert event calendar / post-event survey results snapshot</div>
      </div>
    </div>

    <!-- CASE 5: Vendor -->
    <div class="case reveal">
      <div class="case-left">
        <span class="case-tag">Case 05 — Vendor & Budget Management</span>
        <h3>Turning Vendor Contracts Into a Cost Center Win</h3>
        <div class="case-block">
          <h5>The Problem</h5>
          <p>Facilities and food-program vendor contracts across cleaning, maintenance, and catering carried unchecked cost creep without active SLA oversight.</p>
        </div>
        <div class="case-block">
          <h5>My Role & Strategy</h5>
          <p>I lead end-to-end vendor management and contractor oversight — renegotiating terms and enforcing SLA compliance across every vendor category.</p>
        </div>
      </div>
      <div class="case-right">
        <ol class="case-steps">
          <li>Audited existing vendor contracts and SLA terms.</li>
          <li>Benchmarked market pricing across categories.</li>
          <li>Renegotiated contract terms with underperforming or overpriced vendors.</li>
          <li>Implemented ongoing SLA monitoring to prevent drift.</li>
        </ol>
        <div class="impact-panel">
          <div class="stamp"><span>Verified<br>Savings</span></div>
          <h5>The Impact</h5>
          <div class="impact-stats">
            <div class="impact-stat"><div class="num">$15K–$20K</div><div class="label">Saved via renegotiation & SLA mgmt</div></div>
            <div class="impact-stat"><div class="num">$55K+</div><div class="label">Total annual budget administered</div></div>
          </div>
          <p class="note">Documented savings from contract renegotiation, vendor solicitation, and SLA management — on top of full administration of a $55K+ annual operating budget.</p>
        </div>
        <div class="artifact-tag">Artifact Showcase → Insert vendor scorecard / SLA compliance tracker</div>
      </div>
    </div>

  </div>
</section>

<!-- WHY GEN -->
<section id="why-gen">
  <div class="wrap">
    <div class="why-gen">
      <div class="reveal">
        <div class="eyebrow">Why Gen</div>
        <blockquote>A physical environment as <span class="accent-word">intentional</span> as the mission it houses.</blockquote>
      </div>
      <div class="why-copy reveal">
        <p>What draws me to Gen is the chance to shape the workplace for a company whose whole mission is about safety, trust, and protecting how nearly 500 million people live their digital and financial lives. <strong>That kind of high-impact, customer-driven culture deserves a physical environment that's just as intentional.</strong> As a Workplace Experience Manager, I'd want Gen's NYC employees and visitors to feel like my actual customers, so every part of the office reflects that same standard of care.</p>
        <p>Your values around being scrappy, thinking big, and playing to win together resonate with me because that's honestly how I've operated throughout my career. <strong>My background is in hospitality management</strong>, where things go sideways constantly and you learn to think on your feet and figure it out without waiting for someone to hand you a solution. That instinct carried directly into my current role at Compass — identifying a missing rooftop HVAC unit and managing the full replacement myself, initiating a six-month infrastructure upgrade, building 80+ employee events, owning communications to 200+ employees, and building a Gemini-powered budget tool because I wanted visibility before problems surfaced instead of after.</p>
        <p>What excites me most is being part of Gen's Global Workplace team, where workplace strategy is treated as a core operational partner. <strong>I want to work somewhere that uses the physical environment to energize people, foster real connection, and reinforce company culture</strong> — rather than just keep the lights on. I'd love to bring that same ownership to the NYC site from day one.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="alt" id="contact">
  <div class="wrap">
    <div class="contact-grid">
      <div class="reveal">
        <div class="eyebrow">Let's Talk</div>
        <h2>Ready to bring this standard to Gen's NYC site.</h2>
        <p style="color:var(--text-dim); font-size:16px; max-width:44ch;">I'd welcome the chance to talk through how this experience translates directly to Gen's Global Workplace team.</p>
      </div>
      <div class="contact-links reveal">
        <div class="contact-link-row"><span>Phone</span><a href="tel:3014552614">301.455.2614</a></div>
        <div class="contact-link-row"><span>Email</span><a href="mailto:naomi.eyob@gmail.com">naomi.eyob@gmail.com</a></div>
        <div class="contact-link-row"><span>Location</span><span style="color:var(--text-dim); font-size:14px;">Baltimore / DC Area</span></div>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>NAOMI EYOB — WORKPLACE EXPERIENCE MANAGER PORTFOLIO — PREPARED FOR GEN</p>
</footer>

<script>
  const menuBtn = document.getElementById('menuBtn');
  const menuClose = document.getElementById('menuClose');
  const mobileMenu = document.getElementById('mobileMenu');
  menuBtn.addEventListener('click', () => mobileMenu.classList.add('open'));
  menuClose.addEventListener('click', () => mobileMenu.classList.remove('open'));
  mobileMenu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => mobileMenu.classList.remove('open')));

  const revealEls = document.querySelectorAll('.reveal');
  if('IntersectionObserver' in window){
    const io = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('visible');
          io.unobserve(entry.target);
        }
      });
    }, {threshold:0.12});
    revealEls.forEach(el => io.observe(el));
  } else {
    revealEls.forEach(el => el.classList.add('visible'));
  }
</script>

</body>
</html>
