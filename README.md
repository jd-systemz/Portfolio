<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Judy Ann Gorre — Data Analyst & Automation Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700;800&family=Nunito+Sans:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#120E1B;
    --card:#1B1629;
    --card-2:#211A33;
    --ink:#F1EDFB;
    --muted:#A79FC2;
    --purple:#A78BFA;
    --purple-deep:#6030cf;
    --lav:#C7B9FF;
    --teal:#4ED9C4;
    --peach:#FF9E80;
    --line:#352B4D;
    --line-bright:rgba(167,139,250,0.45);
    --shadow: 0 12px 32px rgba(0,0,0,0.35);
    --radius:20px;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--ink);
    font-family:'Nunito Sans', sans-serif;
    line-height:1.65;
    overflow-x:hidden;
  }
  h1,h2,h3{font-family:'Poppins', sans-serif; letter-spacing:-0.01em;}
  a{color:inherit;}
  .wrap{max-width:1040px; margin:0 auto; padding:0 24px;}
  section{padding:80px 0;}

  /* NAV */
  nav{position:sticky; top:16px; z-index:50; margin:0 auto;}
  nav .pill{
    max-width:1040px; margin:0 24px; background:rgba(27,22,41,0.85);
    backdrop-filter:blur(12px); border-radius:100px; box-shadow:var(--shadow);
    border:1px solid var(--line);
    display:flex; align-items:center; justify-content:space-between;
    padding:10px 12px 10px 10px;
  }
  @media (min-width:1088px){ nav .pill{margin:0 auto;} }
  .brand{display:flex; align-items:center; gap:10px; font-weight:700; font-size:0.95rem;}
  .brand .logo{
    width:38px; height:38px; border-radius:50%;
    background:linear-gradient(135deg, var(--teal), var(--purple-deep));
    display:flex; align-items:center; justify-content:center;
    color:#fff; font-family:'Poppins'; font-weight:700; font-size:0.95rem;
  }
  nav ul{display:flex; gap:22px; list-style:none; align-items:center;}
  nav ul a{font-size:0.88rem; color:var(--muted); text-decoration:none; font-weight:600; transition:color .2s;}
  nav ul a:hover{color:var(--purple);}
  nav ul .resume-btn{
    background:linear-gradient(135deg, var(--purple-deep), var(--purple)); color:#fff; padding:9px 18px; border-radius:100px; font-size:0.82rem;
  }
  nav ul .resume-btn:hover{opacity:0.9; color:#fff;}
  @media (max-width:760px){ nav ul li:not(.resume-item){display:none;} }

  /* HERO */
  header.hero{position:relative; padding:150px 0 40px; overflow:hidden;}
  .blob{position:absolute; border-radius:50%; filter:blur(70px); opacity:0.35; z-index:0;}
  .blob-1{width:520px; height:520px; top:-220px; right:-160px; background:radial-gradient(circle at 30% 30%, var(--purple-deep), transparent 70%);}
  .blob-2{width:460px; height:460px; top:60px; left:-220px; background:radial-gradient(circle at 60% 40%, var(--lav), transparent 70%);}
  .blob-3{width:360px; height:360px; bottom:-180px; right:200px; background:radial-gradient(circle at 50% 50%, var(--teal), transparent 70%);}
  .hero-inner{position:relative; z-index:1; text-align:center; max-width:720px; margin:0 auto;}
  .eyebrow{
    display:inline-flex; align-items:center; gap:8px; font-size:0.82rem; font-weight:700;
    color:var(--lav); background:rgba(167,139,250,0.12); border:1px solid var(--line-bright);
    border-radius:100px; padding:7px 16px; margin-bottom:24px;
  }
  .eyebrow::before{content:''; width:7px; height:7px; border-radius:50%; background:var(--teal);}
  .hero h1{font-size:clamp(2.1rem, 5.2vw, 3.1rem); font-weight:700; line-height:1.18;}
  .hero h1 .accent{
    background:linear-gradient(90deg, var(--purple), var(--teal));
    -webkit-background-clip:text; background-clip:text; color:transparent;
  }
  .hero p.tagline{color:var(--muted); font-size:1.08rem; margin-top:20px; max-width:520px; margin-left:auto; margin-right:auto;}
  .hero .links{display:flex; gap:14px; margin-top:34px; flex-wrap:wrap; justify-content:center;}
  .btn{
    padding:13px 24px; border-radius:100px; font-size:0.92rem; font-weight:700;
    text-decoration:none; display:inline-flex; align-items:center; gap:8px;
    transition:transform .15s, box-shadow .15s; border:1px solid transparent;
  }
  .btn-primary{background:linear-gradient(135deg, var(--purple-deep), var(--purple)); color:#fff; box-shadow:0 10px 24px rgba(139,92,246,0.35);}
  .btn-primary:hover{transform:translateY(-2px); box-shadow:0 14px 28px rgba(139,92,246,0.45);}
  .btn-ghost{background:var(--card); border:1px solid var(--line); color:var(--ink);}
  .btn-ghost:hover{transform:translateY(-2px); border-color:var(--purple);}

  /* ABOUT CARD */
  .about-card{
    background:var(--card); border:1px solid var(--line); border-radius:24px; box-shadow:var(--shadow);
    padding:36px; display:flex; gap:28px; align-items:center; margin-top:60px;
    position:relative; z-index:1;
  }
  .avatar{
    flex:0 0 auto; width:96px; height:96px; border-radius:50%;
    background:linear-gradient(135deg, var(--purple), var(--teal));
    border:2px solid var(--line-bright);
    display:flex; align-items:center; justify-content:center;
    color:#fff; font-family:'Poppins'; font-weight:700; font-size:1.7rem;
  }
  .about-card .greet{color:var(--muted); font-size:0.95rem; margin-bottom:2px;}
  .about-card .greet b{background:linear-gradient(90deg,var(--purple),var(--teal)); -webkit-background-clip:text; background-clip:text; color:transparent;}
  .about-card p{color:var(--muted); font-size:0.98rem; margin-top:6px;}
  @media (max-width:640px){ .about-card{flex-direction:column; text-align:center;} }

  /* SECTION HEAD */
  .section-head{text-align:center; max-width:560px; margin:0 auto 44px;}
  .section-head .kicker{color:var(--purple); font-weight:700; font-size:0.82rem; text-transform:uppercase; letter-spacing:0.06em;}
  .section-head h2{font-size:1.9rem; margin-top:8px;}
  .section-head p{color:var(--muted); margin-top:10px;}

  /* SKILLS — bordered cards */
  .skill-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:22px;}
  .skill-card{
    text-align:center; background:var(--card); border:1px solid var(--line); border-radius:18px;
    padding:28px 18px; transition:border-color .2s, transform .2s;
  }
  .skill-card:hover{border-color:var(--purple); transform:translateY(-3px);}
  .skill-circle{
    width:72px; height:72px; border-radius:50%; margin:0 auto 18px;
    display:flex; align-items:center; justify-content:center; font-size:1.6rem;
    border:1px solid rgba(255,255,255,0.15);
  }
  .c-teal{background:linear-gradient(135deg,#2FC9B8,#1FA893);}
  .c-purple{background:linear-gradient(135deg,#8B5CF6,#6D42D6);}
  .c-lav{background:linear-gradient(135deg,#C7B9FF,#A78BFA);}
  .c-peach{background:linear-gradient(135deg,#FFB199,#FF8C6B);}
  .skill-card h3{font-size:1.05rem; margin-bottom:8px;}
  .skill-card .tag-row{display:flex; flex-wrap:wrap; gap:6px; justify-content:center; margin-top:12px;}
  .tag{font-size:0.78rem; color:var(--lav); background:rgba(167,139,250,0.12); border:1px solid var(--line); padding:5px 12px; border-radius:100px; font-weight:600;}

  /* AUTOMATION FLOW */
  .flow-intro{color:var(--muted); text-align:center; max-width:620px; margin:0 auto 40px;}
  .flow-wrap{display:flex; align-items:stretch;}
  @media (max-width:900px){ .flow-wrap{display:block;} }
  .flow-step{
    flex:1; background:var(--card); border:1px solid var(--line); border-radius:18px;
    padding:22px 16px; text-align:center; position:relative; margin:0 8px; transition:border-color .2s;
  }
  .flow-step:hover{border-color:var(--purple);}
  @media (max-width:900px){ .flow-step{margin:0 0 20px;} }
  .flow-step .step-num{
    width:30px; height:30px; border-radius:50%; background:linear-gradient(135deg,var(--purple-deep),var(--purple)); color:#fff;
    display:flex; align-items:center; justify-content:center; font-size:0.8rem; font-weight:700;
    margin:0 auto 12px;
  }
  .flow-step h4{font-size:0.95rem; margin-bottom:6px;}
  .flow-step p{font-size:0.8rem; color:var(--muted);}
  .flow-arrow{display:flex; align-items:center; justify-content:center; color:var(--purple); font-size:1.4rem;}
  @media (max-width:900px){ .flow-arrow{display:none;} }

  /* EXPERIENCE */
  .timeline{max-width:720px; margin:0 auto; position:relative; padding-left:28px; border-left:2px solid var(--line);}
  .tl-item{
    position:relative; background:var(--card); border:1px solid var(--line); border-radius:16px;
    box-shadow:var(--shadow); padding:22px 22px 22px 26px; margin-bottom:22px; margin-left:6px;
    transition:border-color .2s;
  }
  .tl-item:hover{border-color:var(--purple);}
  .tl-item:last-child{margin-bottom:0;}
  .tl-item::before{
    content:''; position:absolute; left:-35px; top:26px;
    width:12px; height:12px; border-radius:50%; background:var(--purple); box-shadow:0 0 0 5px var(--bg), 0 0 10px var(--purple);
  }
  .tl-role{font-size:1.05rem; font-weight:700; font-family:'Poppins';}
  .tl-meta{font-size:0.8rem; color:var(--lav); font-weight:700; margin:4px 0 12px;}
  .tl-item ul{padding-left:18px; color:var(--muted); font-size:0.92rem;}
  .tl-item li{margin-bottom:6px;}
  .tl-item li b{color:var(--ink);}

  /* PROJECTS */
  .project-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:22px;}
  .project-card{
    background:var(--card); border:1px solid var(--line); border-radius:18px;
    padding:26px; display:flex; flex-direction:column; transition:transform .2s, border-color .2s;
  }
  .project-card:hover{transform:translateY(-4px); border-color:var(--purple);}
  .project-card h3{font-size:1.05rem; margin-bottom:8px;}
  .project-card p{color:var(--muted); font-size:0.9rem; flex-grow:1;}
  .project-card .tag-row{display:flex; flex-wrap:wrap; gap:6px; margin:14px 0;}
  .project-card a{font-size:0.85rem; color:var(--purple); font-weight:700; text-decoration:none;}
  .project-card a:hover{text-decoration:underline; color:var(--lav);}

  /* EDUCATION */
  .edu-grid{display:grid; grid-template-columns:1fr 1fr; gap:28px; max-width:800px; margin:0 auto;}
  @media (max-width:640px){ .edu-grid{grid-template-columns:1fr;} }
  .edu-card{background:var(--card); border:1px solid var(--line); border-radius:16px; padding:26px; transition:border-color .2s;}
  .edu-card:hover{border-color:var(--purple);}
  .edu-card h3{font-size:1rem; margin-bottom:14px;}
  .edu-card ul{list-style:none; color:var(--muted); font-size:0.9rem;}
  .edu-card li{margin-bottom:10px; padding-left:16px; position:relative;}
  .edu-card li::before{content:'•'; position:absolute; left:0; color:var(--purple); font-weight:700;}

  /* FOOTER */
  footer{padding:90px 0 50px; text-align:center;}
  .footer-card{
    background:linear-gradient(135deg,#403269,#1e113f); border:1px solid var(--line-bright); border-radius:28px; padding:60px 32px; color:#fff;
  }
  footer h2{font-size:1.9rem; margin-bottom:12px; font-family:'Poppins';}
  footer p{color:rgba(255,255,255,0.85); margin-bottom:28px;}
  footer .links{display:flex; justify-content:center; gap:14px; flex-wrap:wrap;}
  footer .btn-primary{background:#fff; color:var(--purple-deep); box-shadow:none;}
  footer .btn-ghost{background:rgba(255,255,255,0.1); border:1px solid rgba(255,255,255,0.4); color:#fff;}
  .bottom{font-size:0.78rem; color:var(--muted); padding-top:40px;}
</style>
</head>
<body>

<nav>
  <div class="pill wrap" style="padding-left:14px; padding-right:14px;">
    <div class="brand"><div class="logo">JG</div> Judy Ann Gorre</div>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#flow">How I Work</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li class="resume-item"><a class="resume-btn" href="https://drive.google.com/file/d/10jXYlO5qxZ4WodaWmQKJKTdV0TTKNC07/view?usp=sharing" target="_blank" rel="noopener">Resume</a></li>
    </ul>
  </div>
</nav>

<header class="hero">
  <div class="blob blob-1"></div>
  <div class="blob blob-2"></div>
  <div class="blob blob-3"></div>
  <div class="wrap hero-inner">
    <div class="eyebrow">Available for work · Quezon City, PH</div>
    <h1>Messy spreadsheets in. <span class="accent">Self-running systems out.</span></h1>
    <p class="tagline">I'm Judy — a Data Analyst &amp; Automation Developer who builds the pipelines, dashboards, and front-end tools that turn scattered data into something a whole team can actually use.</p>
    <div class="links">
      <a class="btn btn-primary" href="mailto:annjudy844@gmail.com">Get in touch</a>
      <a class="btn btn-ghost" href="https://drive.google.com/file/d/10jXYlO5qxZ4WodaWmQKJKTdV0TTKNC07/view?usp=sharing" target="_blank" rel="noopener">View Resume ↓</a>
      <a class="btn btn-ghost" href="https://github.com/jd-systemz" target="_blank" rel="noopener">GitHub ↗</a>
    </div>
  </div>

  <div class="wrap">
    <div class="about-card" id="about">
      <div class="avatar">JG</div>
      <div>
        <div class="greet">Hi, I'm <b>Judy</b> 👋</div>
        <p>I work at the point where operations meet code — migrating databases, wiring apps together with automation, and building dashboards clear enough for a whole company to actually use. I also build the front-end layer myself, because a pipeline only matters if people can see what comes out of it.</p>
      </div>
    </div>
  </div>
</header>

<section id="skills">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">What I bring</div>
      <h2>I'll be helping you with the following</h2>
      <p>Four areas that cover the full loop, from raw data to something your team can trust.</p>
    </div>
    <div class="skill-grid">
      <div class="skill-card">
        <div class="skill-circle c-teal">🗄️</div>
        <h3>Data &amp; Databases</h3>
        <div class="tag-row"><span class="tag">SQL</span><span class="tag">Power BI</span><span class="tag">Smartsheet</span><span class="tag">AppSheet</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-circle c-purple">⚙️</div>
        <h3>Automation</h3>
        <div class="tag-row"><span class="tag">n8n</span><span class="tag">Python</span><span class="tag">Docker</span><span class="tag">Apps Script</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-circle c-lav">💻</div>
        <h3>Front-End &amp; Dev</h3>
        <div class="tag-row"><span class="tag">HTML/CSS/JS</span><span class="tag">Flutter</span><span class="tag">Dart</span></div>
      </div>
      <div class="skill-card">
        <div class="skill-circle c-peach">📋</div>
        <h3>Process</h3>
        <div class="tag-row"><span class="tag">DB Migration</span><span class="tag">Root-Cause</span><span class="tag">SOPs</span></div>
      </div>
    </div>
  </div>
</section>

<section id="flow">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">How I work</div>
      <h2>What happens when I automate something</h2>
    </div>
    <p class="flow-intro">This is the actual shape of a project I shipped at Awards Central — raw records scattered across two tools, ending up as one dashboard leadership could trust without double-checking it.</p>
    <div class="flow-wrap">
      <div class="flow-step">
        <div class="step-num">1</div>
        <h4>Messy source data</h4>
        <p>Records live in Smartsheet, half-updated and duplicated across teams.</p>
      </div>
      <div class="flow-arrow">→</div>
      <div class="flow-step">
        <div class="step-num">2</div>
        <h4>Clean &amp; migrate</h4>
        <p>I rebuild it as one structured master database in Google Sheets.</p>
      </div>
      <div class="flow-arrow">→</div>
      <div class="flow-step">
        <div class="step-num">3</div>
        <h4>Automate the sync</h4>
        <p>n8n + Docker keep every tool updated in real time, with no manual re-entry.</p>
      </div>
      <div class="flow-arrow">→</div>
      <div class="flow-step">
        <div class="step-num">4</div>
        <h4>Build the dashboard</h4>
        <p>A live view that turns raw rows into something readable at a glance.</p>
      </div>
      <div class="flow-arrow">→</div>
      <div class="flow-step">
        <div class="step-num">5</div>
        <h4>Leadership decides</h4>
        <p>The CEO opens one dashboard instead of five spreadsheets.</p>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Experience</div>
      <h2>Where I've done this</h2>
    </div>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-role">IT &amp; BPM Specialist — Awards Central Philippines, Inc.</div>
        <div class="tl-meta">JAN 2026 – JUN 2026</div>
        <ul>
          <li><b>Database migration:</b> bulk-migrated company records from Smartsheet to Google Sheets and designed a new master database for faster reporting.</li>
          <li><b>Dashboards:</b> built Smartsheet dashboards and WIP-tracking tools used from general staff up to the CEO.</li>
          <li><b>Automation:</b> connected Respond.io, Google Sheets, and Smartsheet with n8n and Docker to keep logs in sync automatically.</li>
          <li><b>CRM &amp; HR:</b> centralized Facebook, Instagram, and GoDaddy messages into Respond.io; managed ZKTeco attendance databases.</li>
          <li><b>Web tooling:</b> built an internal announcement site with Apps Script that auto-emails updates to staff.</li>
        </ul>
      </div>
      <div class="tl-item">
        <div class="tl-role">Logistics Supervisor — Awards Central Philippines, Inc.</div>
        <div class="tl-meta">OCT 2025 – JAN 2026</div>
        <ul>
          <li>Built and managed the company's logistics expense database for reimbursements and liquidations.</li>
          <li>Supervised daily logistics operations and coordinated multi-channel cargo routing across air, sea, and land.</li>
        </ul>
      </div>
      <div class="tl-item">
        <div class="tl-role">IT &amp; BPM Associate — Awards Central Philippines, Inc.</div>
        <div class="tl-meta">JUN 2025 – OCT 2025</div>
        <ul>
          <li>Authored standardized workflows and compliance rules across departments to protect data accuracy.</li>
          <li>Led onboarding sessions and trained incoming employees.</li>
        </ul>
      </div>
      <div class="tl-item">
        <div class="tl-role">IT Intern (OJT) — Awards Central Philippines, Inc.</div>
        <div class="tl-meta">MAR 2025 – JUN 2025</div>
        <ul>
          <li>Supported the technical department's daily maintenance work — converted to a full-time hire afterward.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Projects</div>
      <h2>Things I've built</h2>
    </div>
    <div class="project-grid">
      <div class="project-card">
        <h3>WaveSync</h3>
        <p>My very first project during college — a full front-end UI kit for a dashboard-driven product: login, cart, orders, notifications, profile, and settings screens.</p>
        <div class="tag-row"><span class="tag">HTML</span><span class="tag">CSS</span></div>
        <a href="https://jd-systemz.github.io/WaveSync/" target="_blank" rel="noopener">Visit site ↗</a>
      </div>
      <div class="project-card">
        <h3>SolarSolves</h3>
        <p>A landing page built from scratch with vanilla HTML, CSS, and JavaScript — structuring content, styling, and interactivity without a framework.</p>
        <div class="tag-row"><span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JS</span></div>
        <a href="https://jd-systemz.github.io/SolarSolves/" target="_blank" rel="noopener">Visit site ↗</a>
      </div>
      <div class="project-card">
        <h3>Inventory Scanner</h3>
        <p>A tool for tracking inventory counts, echoing the custom tracking infrastructure I built at Awards Central for sales leads and project calendars.</p>
        <div class="tag-row"><span class="tag">HTML/CSS/JS</span><span class="tag">Apps Script</span></div>
        <a href="https://jd-systemz.github.io/inventory-scanner/" target="_blank" rel="noopener">Visit site ↗</a>
      </div>
      <div class="project-card">
        <h3>Internal Announcement Site</h3>
        <p>A company-wide announcement website built with Apps Script, wired to automatically email updates to every staff account.</p>
        <div class="tag-row"><span class="tag">HTML/CSS/JS</span><span class="tag">Apps Script</span></div>
        <a href="https://script.google.com/macros/s/AKfycbzEfirhVbcza5e4t53ytWxp6CDn_UkXpWxcY04V28oDCDC924iCuYuZmpR5w_LjytzC/exec" target="_blank" rel="noopener">Visit site ↗</a>
      </div>
    </div>
  </div>
</section>

<section id="education">
  <div class="wrap">
    <div class="section-head">
      <div class="kicker">Background</div>
      <h2>Education &amp; certifications</h2>
    </div>
    <div class="edu-grid">
      <div class="edu-card">
        <h3>Education</h3>
        <ul>
          <li>B.S. in Information Technology — Bestlink College of the Philippines, Quezon City (2021–2025, Graduate)</li>
        </ul>
      </div>
      <div class="edu-card">
        <h3>Certifications</h3>
        <ul>
          <li>Special Program for Employment of Students (SPES) — DOLE</li>
          <li>BITZ: Understanding the Innovators' Role in Digital Transformation</li>
          <li>Research Trends in ICT &amp; Engineering</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <div class="footer-card">
      <h2>Let's build something that runs itself.</h2>
      <p>Open to Data Analyst and Front-End Developer roles — Quezon City, Philippines.</p>
      <div class="links">
        <a class="btn btn-primary" href="mailto:annjudy844@gmail.com">annjudy844@gmail.com</a>
        <a class="btn btn-ghost" href="Judy-Ann-Gorre-Resume.pdf" target="_blank" rel="noopener">Download Resume</a>
        <a class="btn btn-ghost" href="https://github.com/jd-systemz" target="_blank" rel="noopener">GitHub</a>
        <a class="btn btn-ghost" href="https://www.linkedin.com/in/judy-ann-gorre-5b652b32a" target="_blank" rel="noopener">LinkedIn</a>
      </div>
    </div>
    <div class="bottom">© 2026 Judy Ann Gorre</div>
  </div>
</footer>

</body>
</html>
