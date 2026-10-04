
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Nur A Alam — Data Scientist, Machine Learning and Business Analytics">
<title>Nur A Alam | Data Scientist</title>

<style>
:root{
  --bg:#0B0F14;
  --surface:#111827;
  --surface2:#172033;
  --text:#F8FAFC;
  --muted:#94A3B8;
  --dim:#64748B;
  --line:#263449;
  --blue:#38BDF8;
  --cyan:#22D3EE;
  --max:1180px;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  background:var(--bg);
  color:var(--text);
  font-family:Inter,"Segoe UI",Arial,sans-serif;
  line-height:1.65;
}

a{
  color:inherit;
  text-decoration:none;
}

.container{
  width:min(var(--max),92%);
  margin:auto;
}

/* =========================
   HERO
========================= */

.hero{
  position:relative;
  min-height:460px;
  overflow:hidden;
  display:flex;
  align-items:center;
  background:
    radial-gradient(circle at 15% 25%,#164E63 0,transparent 28%),
    radial-gradient(circle at 85% 70%,#172554 0,transparent 30%),
    linear-gradient(125deg,#070B11,#0F172A 50%,#172033);
  border-bottom:1px solid var(--line);
}

.hero-grid{
  position:absolute;
  inset:0;
  opacity:.18;
  background-image:
    linear-gradient(#38bdf81a 1px,transparent 1px),
    linear-gradient(90deg,#38bdf81a 1px,transparent 1px);
  background-size:46px 46px;
  -webkit-mask-image:linear-gradient(
    90deg,
    transparent,
    #000 20%,
    #000 80%,
    transparent
  );
  mask-image:linear-gradient(
    90deg,
    transparent,
    #000 20%,
    #000 80%,
    transparent
  );
}

.hero-glow{
  position:absolute;
  width:38%;
  height:150%;
  left:-45%;
  top:-25%;
  transform:rotate(18deg);
  background:linear-gradient(
    90deg,
    transparent,
    #38bdf84d,
    #22d3ee26,
    transparent
  );
  filter:blur(16px);
  animation:sweep 9s ease-in-out infinite;
}

@keyframes sweep{
  0%,18%{
    left:-45%;
    opacity:0;
  }
  35%{
    opacity:1;
  }
  75%{
    left:120%;
    opacity:.5;
  }
  100%{
    left:135%;
    opacity:0;
  }
}

.hero-wave{
  position:absolute;
  width:115%;
  height:180px;
  left:-7%;
  bottom:-125px;
  border-top:1px solid #38bdf833;
  border-radius:50%;
  background:linear-gradient(#38bdf812,transparent);
  transform:rotate(-2deg);
}

.hero-content{
  position:relative;
  z-index:3;
  width:100%;
  text-align:center;
  padding:65px 20px;
}

.eyebrow{
  color:var(--cyan);
  font-size:12px;
  font-weight:700;
  letter-spacing:5px;
  text-transform:uppercase;
  margin-bottom:14px;
}

.hero h1{
  font-size:clamp(42px,7vw,82px);
  line-height:1;
  letter-spacing:-3px;
  font-weight:800;
}

.hero h1 span{
  color:var(--blue);
}

.hero-line{
  width:210px;
  height:2px;
  margin:22px auto;
  background:linear-gradient(
    90deg,
    transparent,
    var(--cyan),
    var(--blue),
    transparent
  );
  position:relative;
  overflow:hidden;
}

.hero-line:after{
  content:"";
  position:absolute;
  left:-35%;
  top:0;
  width:35%;
  height:100%;
  background:#fff;
  filter:blur(2px);
  animation:lineMove 3.5s linear infinite;
}

@keyframes lineMove{
  to{
    left:135%;
  }
}

.hero-role{
  color:#CBD5E1;
  font-size:clamp(14px,2vw,21px);
  letter-spacing:1px;
}

.hero-role strong{
  color:#fff;
}

.hero-meta{
  margin-top:25px;
  display:flex;
  justify-content:center;
  gap:18px;
  flex-wrap:wrap;
  color:var(--muted);
  font-size:12px;
  letter-spacing:1.5px;
  text-transform:uppercase;
}

.hero-meta span:before{
  content:"•";
  margin-right:8px;
  color:var(--cyan);
}

/* =========================
   HERO DATA GRAPHICS
========================= */

.chart,
.ring{
  position:absolute;
  z-index:2;
  opacity:.5;
  pointer-events:none;
}

.chart{
  left:6%;
  bottom:20%;
  width:150px;
  height:90px;
  border-left:1px solid #38bdf899;
  border-bottom:1px solid #38bdf899;
}

.bar{
  position:absolute;
  bottom:0;
  width:14px;
  background:linear-gradient(
    var(--cyan),
    #155E75
  );
  animation:barPulse 3s ease-in-out infinite;
}

.bar:nth-child(1){
  left:15px;
  height:28px;
}

.bar:nth-child(2){
  left:45px;
  height:48px;
  animation-delay:.2s;
}

.bar:nth-child(3){
  left:75px;
  height:67px;
  animation-delay:.4s;
}

.bar:nth-child(4){
  left:105px;
  height:82px;
  animation-delay:.6s;
}

.bar:nth-child(5){
  left:135px;
  height:55px;
  animation-delay:.8s;
}

@keyframes barPulse{
  50%{
    transform:scaleY(.86);
  }
}

.ring{
  right:7%;
  top:25%;
  width:105px;
  height:105px;
  border:1px solid #38bdf899;
  border-radius:50%;
}

.ring:before,
.ring:after{
  content:"";
  position:absolute;
  border:1px solid #22d3ee66;
  border-radius:50%;
}

.ring:before{
  inset:15px;
}

.ring:after{
  inset:31px;
}

/* =========================
   NAVIGATION
========================= */

nav{
  position:sticky;
  top:0;
  z-index:20;
  background:#0B0F14ee;
  backdrop-filter:blur(14px);
  border-bottom:1px solid var(--line);
}

.nav-inner{
  min-height:58px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.brand{
  font-weight:800;
  letter-spacing:1px;
}

.brand span{
  color:var(--cyan);
}

.nav-links{
  display:flex;
  gap:24px;
}

.nav-links a{
  font-size:13px;
  color:var(--muted);
  transition:.2s;
}

.nav-links a:hover{
  color:var(--cyan);
}

/* =========================
   SECTIONS
========================= */

section{
  padding:85px 0;
  border-bottom:1px solid var(--line);
}

.section-head{
  margin-bottom:38px;
}

.kicker{
  color:var(--cyan);
  font-size:11px;
  font-weight:700;
  letter-spacing:3px;
  text-transform:uppercase;
  margin-bottom:8px;
}

h2{
  font-size:clamp(30px,4vw,46px);
  letter-spacing:-1.5px;
  line-height:1.1;
}

.lead{
  max-width:760px;
  color:var(--muted);
  margin-top:15px;
}

/* =========================
   ABOUT
========================= */

.about-grid{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:55px;
}

.about-copy p{
  color:var(--muted);
  margin-bottom:18px;
}

.about-copy strong{
  color:#E2E8F0;
}

.fact-card{
  border:1px solid var(--line);
  background:linear-gradient(
    145deg,
    var(--surface2),
    var(--surface)
  );
  padding:28px;
  box-shadow:0 20px 60px #0005;
}

.fact{
  padding:17px 0;
  border-bottom:1px solid var(--line);
}

.fact:last-child{
  border-bottom:0;
}

.fact b{
  display:block;
  color:#E2E8F0;
  font-size:13px;
  margin-bottom:3px;
}

.fact span{
  color:var(--muted);
  font-size:13px;
}

/* =========================
   RESULTS
========================= */

.results{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
}

.result{
  border:1px solid var(--line);
  background:linear-gradient(
    145deg,
    #111827,
    #0D1420
  );
  padding:28px;
  min-height:170px;
  transition:.3s;
}

.result:hover{
  transform:translateY(-5px);
  border-color:#38bdf866;
  box-shadow:0 15px 45px #0006;
}

.result-number{
  font-size:40px;
  font-weight:800;
  color:var(--cyan);
  letter-spacing:-2px;
}

.result-title{
  margin-top:6px;
  color:#CBD5E1;
  font-size:13px;
}

/* =========================
   PROJECTS
========================= */

.projects{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:18px;
}

.project{
  border:1px solid var(--line);
  background:linear-gradient(
    145deg,
    #111827,
    #0D1420
  );
  padding:30px;
  position:relative;
  overflow:hidden;
  transition:.3s;
}

.project:before{
  content:"";
  position:absolute;
  left:0;
  top:0;
  width:100%;
  height:2px;
  background:linear-gradient(
    90deg,
    var(--blue),
    var(--cyan),
    transparent
  );
}

.project:hover{
  transform:translateY(-5px);
  border-color:#38bdf866;
}

.project-number{
  font-size:12px;
  color:var(--cyan);
  letter-spacing:3px;
}

.project h3{
  font-size:24px;
  margin:10px 0;
}

.project p{
  color:var(--muted);
  font-size:14px;
}

.tags{
  display:flex;
  flex-wrap:wrap;
  gap:7px;
  margin-top:20px;
}

.tag{
  font-size:11px;
  color:#BAE6FD;
  border:1px solid #38bdf844;
  background:#0EA5E91a;
  padding:5px 9px;
  border-radius:999px;
}

.project-link{
  display:inline-block;
  margin-top:20px;
  color:var(--cyan);
  font-size:13px;
  font-weight:700;
}

/* =========================
   WORKFLOW
========================= */

.workflow{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:12px;
}

.step{
  border:1px solid var(--line);
  background:var(--surface);
  padding:22px;
  position:relative;
}

.step-number{
  font-size:11px;
  color:var(--cyan);
  letter-spacing:2px;
}

.step h3{
  font-size:16px;
  margin:12px 0 6px;
}

.step p{
  font-size:12px;
  color:var(--muted);
}

/* =========================
   TECHNOLOGY STACK
========================= */

.stack{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.stack .tag{
  padding:9px 13px;
  font-size:12px;
}

/* =========================
   ROADMAP
========================= */

.roadmap{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:14px;
}

.road{
  border-left:2px solid var(--line);
  padding:20px 20px 20px 24px;
  background:linear-gradient(
    145deg,
    #111827,
    #0D1420
  );
}

.road-status{
  color:var(--cyan);
  font-size:11px;
  font-weight:800;
  letter-spacing:2px;
  text-transform:uppercase;
}

.road h3{
  margin:8px 0;
}

.road p{
  font-size:13px;
  color:var(--muted);
}

/* =========================
   CONTACT
========================= */

.contact{
  display:grid;
  grid-template-columns:1fr .8fr;
  gap:30px;
  align-items:center;
}

.cta{
  border:1px solid #38bdf866;
  background:linear-gradient(
    135deg,
    #0C2534,
    #101827
  );
  padding:38px;
}

.cta h3{
  font-size:30px;
}

.cta p{
  color:var(--muted);
  margin:10px 0 20px;
}

.cta a{
  display:inline-block;
  background:linear-gradient(
    90deg,
    var(--blue),
    var(--cyan)
  );
  color:#061018;
  padding:12px 18px;
  font-weight:800;
  border-radius:6px;
  transition:.25s;
}

.cta a:hover{
  transform:translateY(-2px);
  box-shadow:0 10px 30px #22d3ee33;
}

/* =========================
   FOOTER
========================= */

footer{
  padding:28px 0;
  color:var(--dim);
  font-size:12px;
}

.footer-inner{
  display:flex;
  justify-content:space-between;
  gap:20px;
  flex-wrap:wrap;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width:900px){

  .about-grid,
  .contact{
    grid-template-columns:1fr;
  }

  .results{
    grid-template-columns:repeat(2,1fr);
  }

  .workflow{
    grid-template-columns:repeat(2,1fr);
  }

  .roadmap{
    grid-template-columns:repeat(2,1fr);
  }
}

@media(max-width:650px){

  .nav-inner{
    padding:12px 0;
    align-items:flex-start;
    gap:12px;
  }

  .nav-links{
    gap:10px;
    flex-wrap:wrap;
    justify-content:flex-end;
  }

  .nav-links a{
    font-size:11px;
  }

  .hero{
    min-height:520px;
  }

  .chart{
    left:2%;
    transform:scale(.75);
    transform-origin:left bottom;
  }

  .ring{
    right:2%;
    transform:scale(.75);
    transform-origin:right top;
  }

  section{
    padding:65px 0;
  }

  .results,
  .projects,
  .workflow,
  .roadmap{
    grid-template-columns:1fr;
  }

  .hero h1{
    letter-spacing:-2px;
  }

  .hero-content{
    padding:80px 16px;
  }
}

@media(prefers-reduced-motion:reduce){

  html{
    scroll-behavior:auto;
  }

  .hero-glow,
  .hero-line:after,
  .bar{
    animation:none;
  }

  .result,
  .project,
  .cta a{
    transition:none;
  }
}
</style>
</head>

<body>

<header class="hero" id="home">

  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-wave"></div>

  <div class="chart" aria-hidden="true">
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
  </div>

  <div class="ring" aria-hidden="true"></div>

  <div class="hero-content">

    <div class="eyebrow">
      Data • AI • Business Analytics
    </div>

    <h1>
      Nur A <span>Alam</span>
    </h1>

    <div class="hero-line"></div>

    <p class="hero-role">
      <strong>Data Scientist</strong> • Machine Learning • Business Intelligence
    </p>

    <div class="hero-meta">
      <span>Data Strategy</span>
      <span>AI Solutions</span>
      <span>Business Analytics</span>
    </div>

  </div>
</header>

<nav>
  <div class="container nav-inner">

    <a href="#home" class="brand">
      NUR A <span>ALAM</span>
    </a>

    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#results">Results</a>
      <a href="#projects">Projects</a>
      <a href="#workflow">Workflow</a>
      <a href="#stack">Technology</a>
      <a href="#roadmap">Roadmap</a>
      <a href="#contact">Contact</a>
    </div>

  </div>
</nav>

<main>

<section id="about">
  <div class="container">

    <div class="section-head">
      <div class="kicker">01 — Profile</div>
      <h2>Data with purpose.<br>Intelligence with impact.</h2>
      <p class="lead">
        Transforming complex data into practical intelligence,
        scalable analytics systems and measurable business outcomes.
      </p>
    </div>

    <div class="about-grid">

      <div class="about-copy">

        <p>
          I work at the intersection of
          <strong>data science, artificial intelligence,
          machine learning and business strategy</strong>.
        </p>

        <p>
          My focus is not simply building models.
          I design analytical solutions that connect
          data, technology and decision-making.
        </p>

        <p>
          From data preparation and exploratory analysis
          to predictive modelling, visualization and
          strategic insight, every solution is designed
          around a clear business objective.
        </p>

      </div>

      <div class="fact-card">

        <div class="fact">
          <b>Core Focus</b>
          <span>Data Science &amp; AI</span>
        </div>

        <div class="fact">
          <b>Specialization</b>
          <span>Machine Learning &amp; Analytics</span>
        </div>

        <div class="fact">
          <b>Business Value</b>
          <span>Decision Intelligence</span>
        </div>

        <div class="fact">
          <b>Approach</b>
          <span>Evidence-driven &amp; scalable</span>
        </div>

      </div>

    </div>

  </div>
</section>

<section id="results">
  <div class="container">

    <div class="section-head">
      <div class="kicker">02 — Results</div>
      <h2>Turning information<br>into decisions.</h2>
      <p class="lead">
        A practical approach focused on measurable value,
        analytical clarity and business outcomes.
      </p>
    </div>

    <div class="results">

      <div class="result">
        <div class="result-number">01</div>
        <div class="result-title">
          Data-driven strategic insights
        </div>
      </div>

      <div class="result">
        <div class="result-number">02</div>
        <div class="result-title">
          Predictive analytical solutions
        </div>
      </div>

      <div class="result">
        <div class="result-number">03</div>
        <div class="result-title">
          Automated intelligence workflows
        </div>
      </div>

      <div class="result">
        <div class="result-number">04</div>
        <div class="result-title">
          Executive-ready reporting
        </div>
      </div>

    </div>

  </div>
</section>

<section id="projects">
  <div class="container">

    <div class="section-head">
      <div class="kicker">03 — Selected Work</div>
      <h2>Projects built around<br>real-world problems.</h2>
    </div>

    <div class="projects">

      <article class="project">

        <div class="project-number">PROJECT 01</div>

        <h3>Business Intelligence</h3>

        <p>
          Analytical dashboards and reporting systems
          designed to transform operational data into
          clear executive-level insights.
        </p>

        <div class="tags">
          <span class="tag">Power BI</span>
          <span class="tag">SQL</span>
          <span class="tag">Data Analytics</span>
          <span class="tag">Dashboarding</span>
        </div>

        <a class="project-link" href="#contact">
          Explore project →
        </a>

      </article>

      <article class="project">

        <div class="project-number">PROJECT 02</div>

        <h3>Predictive Analytics</h3>

        <p>
          Machine learning workflows designed to identify
          patterns, predict outcomes and support
          data-informed decisions.
        </p>

        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">Machine Learning</span>
          <span class="tag">Statistics</span>
          <span class="tag">Predictive Modeling</span>
        </div>

        <a class="project-link" href="#contact">
          Explore project →
        </a>

      </article>

      <article class="project">

        <div class="project-number">PROJECT 03</div>

        <h3>AI &amp; Automation</h3>

        <p>
          Intelligent workflows combining automation,
          artificial intelligence and structured data
          processes to improve efficiency.
        </p>

        <div class="tags">
          <span class="tag">AI</span>
          <span class="tag">Automation</span>
          <span class="tag">Python</span>
          <span class="tag">APIs</span>
        </div>

        <a class="project-link" href="#contact">
          Explore project →
        </a>

      </article>

      <article class="project">

        <div class="project-number">PROJECT 04</div>

        <h3>Strategic Analytics</h3>

        <p>
          Data-driven frameworks that connect analytical
          findings with strategic planning, performance
          measurement and organizational priorities.
        </p>

        <div class="tags">
          <span class="tag">Strategy</span>
          <span class="tag">Analytics</span>
          <span class="tag">KPIs</span>
          <span class="tag">Decision Support</span>
        </div>

        <a class="project-link" href="#contact">
          Explore project →
        </a>

      </article>

    </div>

  </div>
</section>

<section id="workflow">
  <div class="container">

    <div class="section-head">
      <div class="kicker">04 — Workflow</div>
      <h2>From raw data<br>to business value.</h2>
    </div>

    <div class="workflow">

      <div class="step">
        <div class="step-number">01</div>
        <h3>Discover</h3>
        <p>
          Understand the business problem,
          objectives and available data.
        </p>
      </div>

      <div class="step">
        <div class="step-number">02</div>
        <h3>Prepare</h3>
        <p>
          Clean, structure and transform data
          into analysis-ready information.
        </p>
      </div>

      <div class="step">
        <div class="step-number">03</div>
        <h3>Analyze</h3>
        <p>
          Identify patterns, trends,
          relationships and opportunities.
        </p>
      </div>

      <div class="step">
        <div class="step-number">04</div>
        <h3>Model</h3>
        <p>
          Develop analytical and machine
          learning solutions where appropriate.
        </p>
      </div>

      <div class="step">
        <div class="step-number">05</div>
        <h3>Deliver</h3>
        <p>
          Communicate insights through
          dashboards, reports and decisions.
        </p>
      </div>

    </div>

  </div>
</section>

<section id="stack">
  <div class="container">

    <div class="section-head">
      <div class="kicker">05 — Technology</div>
      <h2>Technology stack.</h2>
      <p class="lead">
        A flexible toolkit for analytics, artificial
        intelligence, visualization and business intelligence.
      </p>
    </div>

    <div class="stack">

      <span class="tag">Python</span>
      <span class="tag">SQL</span>
      <span class="tag">Pandas</span>
      <span class="tag">NumPy</span>
      <span class="tag">Scikit-Learn</span>
      <span class="tag">Machine Learning</span>
      <span class="tag">Artificial Intelligence</span>
      <span class="tag">Power BI</span>
      <span class="tag">Data Visualization</span>
      <span class="tag">Statistics</span>
      <span class="tag">Business Analytics</span>
      <span class="tag">Data Strategy</span>

    </div>

  </div>
</section>

<section id="roadmap">
  <div class="container">

    <div class="section-head">
      <div class="kicker">06 — Roadmap</div>
      <h2>Building toward<br>intelligent organizations.</h2>
    </div>

    <div class="roadmap">

      <div class="road">
        <div class="road-status">Phase 01</div>
        <h3>Data Foundation</h3>
        <p>
          Establish reliable data structures,
          analytical processes and reporting foundations.
        </p>
      </div>

      <div class="road">
        <div class="road-status">Phase 02</div>
        <h3>Advanced Analytics</h3>
        <p>
          Introduce predictive analytics,
          machine learning and deeper insights.
        </p>
      </div>

      <div class="road">
        <div class="road-status">Phase 03</div>
        <h3>AI Integration</h3>
        <p>
          Connect artificial intelligence with
          workflows, decision systems and automation.
        </p>
      </div>

      <div class="road">
        <div class="road-status">Phase 04</div>
        <h3>Decision Intelligence</h3>
        <p>
          Build integrated analytical systems
          that support strategic organizational decisions.
        </p>
      </div>

    </div>

  </div>
</section>

<section id="contact">
  <div class="container">

    <div class="section-head">
      <div class="kicker">07 — Contact</div>
      <h2>Let's turn data<br>into direction.</h2>
    </div>

    <div class="contact">

      <div>
        <p class="lead">
          Whether the challenge involves analytics,
          artificial intelligence, business intelligence
          or data strategy, the goal is simple:
          create solutions that deliver meaningful value.
        </p>
      </div>

      <div class="cta">

        <h3>Start a conversation.</h3>

        <p>
          Let's explore how data and AI can create
          measurable impact.
        </p>

        <a href="mailto:your-email@example.com">
          Get in touch →
        </a>

      </div>

    </div>

  </div>
</section>

</main>

<footer>
  <div class="container footer-inner">

    <div>
      © 2026 Nur A Alam. All rights reserved.
    </div>

    <div>
      Data Science • AI • Business Analytics
    </div>

  </div>
</footer>

</body>
</html>
```
