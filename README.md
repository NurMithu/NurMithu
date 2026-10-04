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
  --navy:#0F172A;
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
    radial-gradient(
      circle at 15% 25%,
      rgba(56,189,248,.18) 0,
      transparent 28%
    ),
    radial-gradient(
      circle at 85% 70%,
      rgba(34,211,238,.13) 0,
      transparent 30%
    ),
    radial-gradient(
      circle at 52% 45%,
      rgba(30,64,175,.12) 0,
      transparent 35%
    ),
    linear-gradient(
      125deg,
      #080C12,
      #0F172A 52%,
      #111827
    );

  border-bottom:1px solid var(--line);
}

.hero-grid{
  position:absolute;
  inset:0;
  opacity:.16;

  background-image:
    linear-gradient(
      rgba(56,189,248,.20) 1px,
      transparent 1px
    ),
    linear-gradient(
      90deg,
      rgba(56,189,248,.20) 1px,
      transparent 1px
    );

  background-size:46px 46px;

  -webkit-mask-image:
    linear-gradient(
      90deg,
      transparent,
      #000 20%,
      #000 80%,
      transparent
    );

  mask-image:
    linear-gradient(
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

  background:
    linear-gradient(
      90deg,
      transparent,
      rgba(56,189,248,.25),
      rgba(34,211,238,.18),
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
    opacity:.6;
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

  border-top:1px solid rgba(56,189,248,.25);
  border-radius:50%;

  background:
    linear-gradient(
      rgba(56,189,248,.06),
      transparent
    );

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

  text-shadow:
    0 0 35px rgba(56,189,248,.12);
}

.hero h1 span{
  color:var(--blue);
}

.hero-line{
  width:210px;
  height:2px;
  margin:22px auto;

  background:
    linear-gradient(
      90deg,
      transparent,
      var(--cyan),
      var(--blue),
      transparent
    );

  position:relative;
  overflow:hidden;

  box-shadow:
    0 0 14px rgba(34,211,238,.45);
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
  color:#F8FAFC;
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
   HERO DATA MOTIFS
========================= */

.chart,
.ring{
  position:absolute;
  z-index:2;
  opacity:.45;
  pointer-events:none;
}

.chart{
  left:6%;
  bottom:20%;

  width:150px;
  height:90px;

  border-left:1px solid rgba(56,189,248,.55);
  border-bottom:1px solid rgba(56,189,248,.55);
}

.bar{
  position:absolute;
  bottom:0;
  width:14px;

  background:
    linear-gradient(
      var(--cyan),
      rgba(30,64,175,.45)
    );

  box-shadow:
    0 0 12px rgba(34,211,238,.2);

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

  border:1px solid rgba(56,189,248,.6);
  border-radius:50%;

  box-shadow:
    0 0 28px rgba(56,189,248,.08);
}

.ring:before,
.ring:after{
  content:"";
  position:absolute;

  border:1px solid rgba(34,211,238,.45);
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

  background:
    rgba(11,15,20,.90);

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
  color:#E2E8F0;
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
  color:var(--blue);

  text-shadow:
    0 0 12px rgba(56,189,248,.35);
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

  background:
    linear-gradient(
      145deg,
      rgba(23,32,51,.95),
      rgba(13,20,32,.95)
    );

  padding:28px;

  box-shadow:
    0 15px 40px rgba(0,0,0,.18);
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
  gap:14px;
}

.result{
  min-height:175px;
  padding:24px;

  background:
    linear-gradient(
      145deg,
      #111827,
      #0D1522
    );

  border:1px solid var(--line);

  transition:.25s;

  position:relative;
  overflow:hidden;
}

.result:before{
  content:"";

  position:absolute;
  left:0;
  top:0;

  width:100%;
  height:2px;

  background:
    linear-gradient(
      90deg,
      var(--blue),
      var(--cyan),
      transparent
    );

  opacity:.65;
}

.result:hover{
  transform:translateY(-5px);

  border-color:
    rgba(56,189,248,.55);

  box-shadow:
    0 14px 35px rgba(8,145,178,.12);
}

.result-number{
  font-size:32px;
  font-weight:800;
  letter-spacing:-1px;
  color:var(--blue);
}

.result-title{
  font-weight:700;
  margin:8px 0;
  color:#E2E8F0;
}

.result p{
  font-size:13px;
  color:var(--muted);
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
  background:
    linear-gradient(
      145deg,
      #111827,
      #0C1420
    );

  border:1px solid var(--line);

  padding:30px;

  transition:.25s;

  position:relative;
  overflow:hidden;
}

.project:after{
  content:"";

  position:absolute;

  width:120px;
  height:120px;

  right:-70px;
  top:-70px;

  border-radius:50%;

  background:
    rgba(34,211,238,.08);

  filter:blur(5px);
}

.project:hover{
  transform:translateY(-5px);

  border-color:
    rgba(56,189,248,.55);

  box-shadow:
    0 16px 40px rgba(8,145,178,.10);
}

.project-number{
  color:var(--blue);

  font-size:12px;
  letter-spacing:2px;
}

.project h3{
  font-size:22px;
  margin:10px 0;
  color:#F8FAFC;
}

.project p{
  color:var(--muted);
  font-size:14px;
  margin-bottom:18px;
}

.tags{
  display:flex;
  flex-wrap:wrap;
  gap:7px;
  margin-bottom:20px;
}

.tag{
  padding:5px 9px;

  border:1px solid #2B3A50;

  background:#0E1726;

  color:#AFC4D8;

  font-size:11px;

  border-radius:3px;
}

.tag:hover{
  border-color:
    rgba(56,189,248,.6);

  color:var(--cyan);
}

.project-link{
  font-size:12px;
  font-weight:700;

  color:var(--blue);

  letter-spacing:1px;

  transition:.2s;
}

.project-link:hover{
  color:var(--cyan);
}


/* =========================
   WORKFLOW
========================= */

.workflow{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:1px;

  background:var(--line);

  border:1px solid var(--line);
}

.step{
  background:#101927;
  padding:25px;

  transition:.25s;
}

.step:hover{
  background:#132238;

  box-shadow:
    inset 0 0 0 1px
    rgba(56,189,248,.25);
}

.step-number{
  color:var(--cyan);

  font-size:11px;
  letter-spacing:2px;
}

.step h3{
  margin:8px 0;

  font-size:17px;

  color:#E2E8F0;
}

.step p{
  color:var(--muted);
  font-size:13px;
}


/* =========================
   TECHNOLOGY STACK
========================= */

.stack{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.stack span{
  padding:10px 14px;

  border:1px solid #2B3A50;

  background:#101927;

  color:#B8C7D8;

  font-size:13px;

  transition:.2s;
}

.stack span:hover{
  border-color:
    rgba(56,189,248,.55);

  color:var(--cyan);

  transform:translateY(-2px);
}


/* =========================
   ROADMAP
========================= */

.roadmap{
  display:grid;
  gap:10px;
  max-width:800px;
}

.road{
  display:flex;

  gap:18px;

  align-items:center;

  padding:17px 20px;

  background:#101927;

  border:1px solid var(--line);

  transition:.2s;
}

.road:hover{
  border-color:
    rgba(56,189,248,.45);

  transform:translateX(3px);
}

.road-status{
  width:70px;

  color:var(--cyan);

  font-size:11px;
  font-weight:700;
  letter-spacing:1px;
}

.road strong{
  font-size:14px;
  color:#E2E8F0;
}

.road span{
  color:var(--muted);
  font-size:13px;
}


/* =========================
   CONTACT
========================= */

.contact{
  text-align:center;

  padding:100px 20px;

  background:
    radial-gradient(
      circle at 50% 0%,
      rgba(56,189,248,.13),
      transparent 35%
    ),
    linear-gradient(
      145deg,
      #111827,
      #070B11
    );
}

.contact h2{
  margin-bottom:15px;
}

.contact p{
  color:var(--muted);

  max-width:650px;

  margin:
    0 auto 28px;
}

.cta{
  display:inline-flex;

  padding:13px 21px;

  border:
    1px solid
    rgba(56,189,248,.65);

  color:#E0F2FE;

  background:
    rgba(14,165,233,.07);

  font-size:12px;
  font-weight:700;

  letter-spacing:1px;

  transition:.25s;
}

.cta:hover{
  background:var(--blue);

  border-color:var(--blue);

  color:#07111C;

  box-shadow:
    0 0 25px
    rgba(56,189,248,.28);
}


/* =========================
   FOOTER
========================= */

footer{
  padding:28px 0;

  color:#64748B;

  font-size:12px;
}

.footer-inner{
  display:flex;

  justify-content:space-between;

  gap:20px;
}


/* =========================
   RESPONSIVE
========================= */

@media(max-width:900px){

  .about-grid,
  .projects{
    grid-template-columns:1fr;
  }

  .results{
    grid-template-columns:repeat(2,1fr);
  }

  .workflow{
    grid-template-columns:repeat(2,1fr);
  }

  .chart{
    left:2%;
    opacity:.5;
  }

  .ring{
    right:2%;
    opacity:.5;
  }
}

@media(max-width:620px){

  .nav-links{
    display:none;
  }

  section{
    padding:60px 0;
  }

  .results,
  .workflow{
    grid-template-columns:1fr;
  }

  .hero{
    min-height:430px;
  }

  .hero h1{
    letter-spacing:-2px;
  }

  .hero-meta{
    display:none;
  }

  .chart,
  .ring{
    display:none;
  }

  .footer-inner{
    flex-direction:column;
  }
}

@media(prefers-reduced-motion:reduce){

  *,
  *:before,
  *:after{
    animation:none!important;
    scroll-behavior:auto!important;
    transition:none!important;
  }
}
</style>
</head>

<body>

<!-- =========================
     HERO
========================= -->

<header class="hero" id="top">

  <div class="hero-grid"></div>

  <div class="hero-glow"></div>

  <div class="hero-wave"></div>

  <div class="chart" aria-hidden="true">
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
    <div class="bar"></div>
  </div>

  <div class="ring" aria-hidden="true"></div>

  <div class="hero-content">

    <div class="eyebrow">
      Data • Intelligence • Strategy
    </div>

    <h1>
      Nur-A-<span>Alam</span>
    </h1>

    <div class="hero-line"></div>

    <div class="hero-role">
      <strong>Data Scientist</strong>
      ·
      <strong>Machine Learning</strong>
      ·
      <strong>Business Analytics</strong>
    </div>

    <div class="hero-meta">
      <span>Python & SQL</span>
      <span>Production ML</span>
      <span>Business Impact</span>
      <span>Remote Projects</span>
    </div>

  </div>

</header>


<!-- =========================
     NAVIGATION
========================= -->

<nav>

  <div class="container nav-inner">

    <a class="brand" href="#top">
      NUR A ALAM
    </a>

    <div class="nav-links">

      <a href="#about">
        About
      </a>

      <a href="#results">
        Results
      </a>

      <a href="#projects">
        Projects
      </a>

      <a href="#workflow">
        How I Work
      </a>

      <a href="#contact">
        Contact
      </a>

    </div>

  </div>

</nav>


<!-- =========================
     MAIN
========================= -->

<main>


<!-- =========================
     ABOUT
========================= -->

<section id="about">

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        01 / Profile
      </div>

      <h2>
        Data science built around<br>
        real business decisions.
      </h2>

      <p class="lead">
        I build end-to-end, production-style machine learning and analytics projects—from raw data and statistical analysis to modeling, evaluation, interpretation and deployment.
      </p>

    </div>


    <div class="about-grid">

      <div class="about-copy">

        <p>
          I’m a
          <strong>Data Scientist</strong>
          focused on turning complex datasets into practical, measurable outcomes.
        </p>

        <p>
          My approach is deliberately pragmatic:
          <strong>
            baseline first, choose the right metric, avoid leakage, translate results into business language, and document limitations.
          </strong>
        </p>

        <p>
          I’m particularly interested in machine learning, business analytics, MLOps, RAG applications and AI-driven decision systems.
        </p>

      </div>


      <aside class="fact-card">

        <div class="fact">
          <b>Role</b>
          <span>
            Data Scientist · ML · Business Analytics
          </span>
        </div>

        <div class="fact">
          <b>Core Stack</b>
          <span>
            Python · SQL · pandas · scikit-learn · XGBoost
          </span>
        </div>

        <div class="fact">
          <b>Ships</b>
          <span>
            Streamlit apps · Dockerized models · MLflow experiments
          </span>
        </div>

        <div class="fact">
          <b>Principle</b>
          <span>
            Baseline first. Business impact always.
          </span>
        </div>

        <div class="fact">
          <b>Exploring</b>
          <span>
            MLOps · RAG · LLM apps · AI agents
          </span>
        </div>

      </aside>

    </div>

  </div>

</section>


<!-- =========================
     RESULTS
========================= -->

<section id="results">

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        02 / Results
      </div>

      <h2>
        Evidence over buzzwords.
      </h2>

      <p class="lead">
        Selected project outcomes from the portfolio.
      </p>

    </div>


    <div class="results">

      <article class="result">

        <div class="result-number">
          0.789
        </div>

        <div class="result-title">
          Churn ROC AUC
        </div>

        <p>
          Threshold tuned for early-warning retention outreach.
        </p>

      </article>


      <article class="result">

        <div class="result-number">
          0.926
        </div>

        <div class="result-title">
          Forecasting R²
        </div>

        <p>
          XGBoost performance on a time-based retail holdout.
        </p>

      </article>


      <article class="result">

        <div class="result-number">
          85%
        </div>

        <div class="result-title">
          Fraud Precision
        </div>

        <p>
          85% precision at 85% recall on an imbalanced dataset.
        </p>

      </article>


      <article class="result">

        <div class="result-number">
          0.714
        </div>

        <div class="result-title">
          Sentiment Macro F1
        </div>

        <p>
          Approximately 39% above the stated rule-based baseline.
        </p>

      </article>

    </div>

  </div>

</section>


<!-- =========================
     PROJECTS
========================= -->

<section id="projects">

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        03 / Selected Work
      </div>

      <h2>
        Projects with a business reason.
      </h2>

    </div>


    <div class="projects">


      <!-- PROJECT 01 -->

      <article class="project">

        <div class="project-number">
          PROJECT 01
        </div>

        <h3>
          Customer Churn & Lifetime Value
        </h3>

        <p>
          Predicts churn and estimates customer lifetime value for a subscription retail business, with business-oriented threshold optimization.
        </p>

        <div class="tags">

          <span class="tag">
            Python
          </span>

          <span class="tag">
            pandas
          </span>

          <span class="tag">
            scikit-learn
          </span>

          <span class="tag">
            statsmodels
          </span>

        </div>

        <a
          class="project-link"
          href="https://github.com/NurMithu/Zephyr_Retail_Churn_CLV_Analysis"
          target="_blank"
          rel="noopener noreferrer"
        >
          VIEW REPOSITORY →
        </a>

      </article>


      <!-- PROJECT 02 -->

      <article class="project">

        <div class="project-number">
          PROJECT 02
        </div>

        <h3>
          Retail Sales Forecasting
        </h3>

        <p>
          Compared Linear Regression, Random Forest and XGBoost using a time-based holdout, with promotion-impact analysis.
        </p>

        <div class="tags">

          <span class="tag">
            Python
          </span>

          <span class="tag">
            XGBoost
          </span>

          <span class="tag">
            Random Forest
          </span>

          <span class="tag">
            Streamlit
          </span>

        </div>

        <a
          class="project-link"
          href="https://github.com/NurMithu/sales-forecasting-rossmann"
          target="_blank"
          rel="noopener noreferrer"
        >
          VIEW REPOSITORY →
        </a>

      </article>


      <!-- PROJECT 03 -->

      <article class="project">

        <div class="project-number">
          PROJECT 03
        </div>

        <h3>
          Credit Card Fraud Detection
        </h3>

        <p>
          Imbalanced classification and unsupervised anomaly detection, calibrated around precision and recall rather than accuracy.
        </p>

        <div class="tags">

          <span class="tag">
            scikit-learn
          </span>

          <span class="tag">
            XGBoost
          </span>

          <span class="tag">
            SMOTE
          </span>

          <span class="tag">
            Autoencoders
          </span>

        </div>

        <a
          class="project-link"
          href="https://github.com/NurMithu/fraud-detection"
          target="_blank"
          rel="noopener noreferrer"
        >
          VIEW REPOSITORY →
        </a>

      </article>


      <!-- PROJECT 04 -->

      <article class="project">

        <div class="project-number">
          PROJECT 04
        </div>

        <h3>
          Customer Sentiment Analysis
        </h3>

        <p>
          Rule-based baseline versus TF-IDF and trained classifiers, combined with complaint root-cause analysis.
        </p>

        <div class="tags">

          <span class="tag">
            NLTK
          </span>

          <span class="tag">
            TF-IDF
          </span>

          <span class="tag">
            scikit-learn
          </span>

          <span class="tag">
            Streamlit
          </span>

        </div>

        <a
          class="project-link"
          href="https://github.com/NurMithu/sentiment-analysis"
          target="_blank"
          rel="noopener noreferrer"
        >
          VIEW REPOSITORY →
        </a>

      </article>

    </div>

  </div>

</section>


<!-- =========================
     WORKFLOW
========================= -->

<section id="workflow">

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        04 / Method
      </div>

      <h2>
        A disciplined path from data to decision.
      </h2>

      <p class="lead">
        Technical rigor and business interpretation stay connected.
      </p>

    </div>


    <div class="workflow">


      <article class="step">

        <div class="step-number">
          01
        </div>

        <h3>
          Understand
        </h3>

        <p>
          Define the business question, data and success criteria.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          02
        </div>

        <h3>
          Explore
        </h3>

        <p>
          Profile data, identify patterns, quality issues and leakage.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          03
        </div>

        <h3>
          Model
        </h3>

        <p>
          Establish a baseline before testing more sophisticated models.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          04
        </div>

        <h3>
          Evaluate
        </h3>

        <p>
          Use metrics that reflect the actual cost of business errors.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          05
        </div>

        <h3>
          Interpret
        </h3>

        <p>
          Translate model outputs into clear business recommendations.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          06
        </div>

        <h3>
          Deploy
        </h3>

        <p>
          Package useful models and analytics into practical applications.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          07
        </div>

        <h3>
          Monitor
        </h3>

        <p>
          Track assumptions, limitations, performance and failure modes.
        </p>

      </article>


      <article class="step">

        <div class="step-number">
          08
        </div>

        <h3>
          Improve
        </h3>

        <p>
          Iterate based on evidence, user needs and measurable impact.
        </p>

      </article>

    </div>

  </div>

</section>


<!-- =========================
     TECHNOLOGY
========================= -->

<section>

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        05 / Technology
      </div>

      <h2>
        Tools I work with.
      </h2>

    </div>


    <div class="stack">

      <span>Python</span>
      <span>SQL</span>
      <span>pandas</span>
      <span>NumPy</span>
      <span>scikit-learn</span>
      <span>XGBoost</span>
      <span>statsmodels</span>
      <span>PyTorch</span>
      <span>TensorFlow</span>
      <span>NLTK</span>
      <span>Streamlit</span>
      <span>Docker</span>
      <span>MLflow</span>
      <span>PostgreSQL</span>
      <span>MongoDB</span>
      <span>Git</span>
      <span>GitHub Actions</span>

    </div>

  </div>

</section>


<!-- =========================
     ROADMAP
========================= -->

<section>

  <div class="container">

    <div class="section-head">

      <div class="kicker">
        06 / Roadmap
      </div>

      <h2>
        What’s next.
      </h2>

    </div>


    <div class="roadmap">


      <div class="road">

        <div class="road-status">
          DONE
        </div>

        <div>

          <strong>
            Churn · Sales Forecasting · Fraud · NLP
          </strong>

          <br>

          <span>
            Core portfolio projects
          </span>

        </div>

      </div>


      <div class="road">

        <div class="road-status">
          BUILDING
        </div>

        <div>

          <strong>
            Recommendation System · Loan Default · Demand Forecasting
          </strong>

          <br>

          <span>
            Expanding applied ML portfolio
          </span>

        </div>

      </div>


      <div class="road">

        <div class="road-status">
          NEXT
        </div>

        <div>

          <strong>
            RAG Application · MLOps Pipeline · Real-Time Dashboard
          </strong>

          <br>

          <span>
            Production-focused systems
          </span>

        </div>

      </div>

    </div>

  </div>

</section>


<!-- =========================
     CONTACT
========================= -->

<section class="contact" id="contact">

  <div class="container">

    <div class="kicker">
      07 / Collaboration
    </div>

    <h2>
      Let’s build something useful.
    </h2>

    <p>
      I’m open to remote data science, analytics and machine learning projects where rigorous analysis can translate into meaningful business outcomes.
    </p>

    <a
      class="cta"
      href="https://www.linkedin.com/"
      target="_blank"
      rel="noopener noreferrer"
    >
      CONNECT ON LINKEDIN →
    </a>

  </div>

</section>

</main>


<!-- =========================
     FOOTER
========================= -->

<footer>

  <div class="container footer-inner">

    <span>
      © 2026 Nur A Alam
    </span>

    <span>
      Data Science · Machine Learning · Business Analytics
    </span>

  </div>

</footer>

</body>
</html>
