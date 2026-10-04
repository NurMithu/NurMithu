<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Nur-A-Alam | Executive Profile Banner</title>

<style>
* {
    box-sizing: border-box;
}

html,
body {
    margin: 0;
    background: #111;
    font-family: Inter, "Segoe UI", Arial, sans-serif;
}

/* =========================================================
   MAIN BANNER
   LinkedIn-style ratio: 1584 × 396
========================================================= */

.banner {
    width: 1584px;
    height: 396px;

    position: relative;
    overflow: hidden;

    color: #f5f5f5;

    background:
        radial-gradient(
            circle at 12% 20%,
            rgba(255,255,255,.08),
            transparent 25%
        ),
        radial-gradient(
            circle at 88% 80%,
            rgba(255,255,255,.05),
            transparent 28%
        ),
        linear-gradient(
            115deg,
            #080808 0%,
            #171717 46%,
            #303030 100%
        );
}


/* =========================================================
   SUBTLE GRID
========================================================= */

.grid {
    position: absolute;
    inset: 0;

    opacity: .16;

    background-image:
        linear-gradient(
            rgba(255,255,255,.09) 1px,
            transparent 1px
        ),
        linear-gradient(
            90deg,
            rgba(255,255,255,.09) 1px,
            transparent 1px
        );

    background-size: 48px 48px;

    mask-image:
        linear-gradient(
            to right,
            transparent,
            black 18%,
            black 82%,
            transparent
        );
}


/* =========================================================
   ANIMATED LIGHT SWEEP
========================================================= */

.light {
    position: absolute;

    width: 480px;
    height: 900px;

    top: -250px;
    left: -600px;

    transform: rotate(18deg);

    background:
        linear-gradient(
            90deg,
            transparent,
            rgba(255,255,255,.035),
            rgba(255,255,255,.13),
            rgba(255,255,255,.035),
            transparent
        );

    filter: blur(10px);

    animation:
        sweep 7s ease-in-out infinite;
}

@keyframes sweep {

    0%,
    20% {
        left: -650px;
        opacity: 0;
    }

    35% {
        opacity: 1;
    }

    70% {
        left: 1700px;
        opacity: .75;
    }

    100% {
        left: 1800px;
        opacity: 0;
    }
}


/* =========================================================
   BOTTOM ARCHITECTURAL WAVE
========================================================= */

.wave {
    position: absolute;

    left: -5%;
    bottom: -88px;

    width: 110%;
    height: 165px;

    border-top:
        1px solid rgba(255,255,255,.22);

    border-radius:
        50% 50% 0 0;

    background:
        linear-gradient(
            180deg,
            rgba(255,255,255,.08),
            rgba(255,255,255,.015)
        );

    transform: rotate(-1.5deg);
}


/* =========================================================
   CONTENT
========================================================= */

.content {
    position: absolute;

    inset: 0;

    display: flex;
    align-items: center;
    justify-content: center;

    text-align: center;

    z-index: 5;
}

.inner {
    transform: translateY(-5px);
}


/* =========================================================
   SMALL EXECUTIVE LABEL
========================================================= */

.eyebrow {

    letter-spacing: 5px;

    text-transform: uppercase;

    font-size: 13px;

    font-weight: 600;

    color: #a8a8a8;

    margin-bottom: 12px;
}


/* =========================================================
   NAME
========================================================= */

h1 {

    margin: 0;

    font-size: 66px;

    line-height: .98;

    letter-spacing: -2.5px;

    font-weight: 750;

    color: #fafafa;

    text-shadow:
        0 4px 28px rgba(0,0,0,.45);
}

h1 span {
    color: #9d9d9d;
}


/* =========================================================
   ANIMATED DIVIDER
========================================================= */

.rule {

    width: 210px;

    height: 2px;

    margin:
        17px auto 15px;

    background:
        linear-gradient(
            90deg,
            transparent,
            #d7d7d7,
            #666,
            transparent
        );

    position: relative;

    overflow: hidden;
}

.rule::after {

    content: "";

    position: absolute;

    top: 0;
    left: -35%;

    width: 35%;
    height: 100%;

    background: #fff;

    filter: blur(1px);

    animation:
        ruleMove 3.5s linear infinite;
}

@keyframes ruleMove {

    to {
        left: 135%;
    }
}


/* =========================================================
   PROFESSIONAL TAGLINE
========================================================= */

.tagline {

    font-size: 20px;

    font-weight: 500;

    letter-spacing: 1.8px;

    color: #d0d0d0;
}

.tagline b {

    color: #f1f1f1;

    font-weight: 650;
}

.dot {

    margin: 0 13px;

    color: #777;
}


/* =========================================================
   DATA VISUALIZATION MOTIFS
========================================================= */

.motif {

    position: absolute;

    z-index: 3;

    color:
        rgba(255,255,255,.35);
}


/* LEFT GRAPH */

.left {

    left: 95px;

    top: 105px;
}


/* RIGHT GRAPH */

.right {

    right: 95px;

    top: 103px;
}


/* =========================================================
   BAR CHART
========================================================= */

.chart {

    width: 190px;

    height: 110px;

    border-left:
        1px solid rgba(255,255,255,.28);

    border-bottom:
        1px solid rgba(255,255,255,.28);

    position: relative;
}


/* BAR */

.bar {

    position: absolute;

    bottom: 0;

    width: 18px;

    background:
        linear-gradient(
            #bdbdbd,
            #444
        );

    border:
        1px solid rgba(255,255,255,.18);
}


/* Individual bars */

.b1 {

    left: 25px;

    height: 32px;
}

.b2 {

    left: 58px;

    height: 54px;
}

.b3 {

    left: 91px;

    height: 76px;
}

.b4 {

    left: 124px;

    height: 92px;
}

.b5 {

    left: 157px;

    height: 66px;
}


/* Trend line */

.line {

    position: absolute;

    left: 20px;

    bottom: 18px;

    width: 155px;

    height: 65px;

    border-top:
        2px solid rgba(245,245,245,.58);

    transform:
        skewY(-20deg)
        rotate(-2deg);

    opacity: .65;
}


/* =========================================================
   DATA RING
========================================================= */

.data-ring {

    width: 105px;

    height: 105px;

    border:
        1px solid rgba(255,255,255,.28);

    border-radius: 50%;

    position: relative;
}


.data-ring::before,
.data-ring::after {

    content: "";

    position: absolute;

    inset: 15px;

    border:
        1px solid rgba(255,255,255,.18);

    border-radius: 50%;
}


.data-ring::after {

    inset: 31px;

    border-color:
        rgba(255,255,255,.32);
}


/* Ring diagonal */

.ring-line {

    position: absolute;

    width: 140px;

    height: 1px;

    top: 51px;

    left: -18px;

    background:
        rgba(255,255,255,.25);

    transform:
        rotate(35deg);
}


/* =========================================================
   FOOTER LABEL
========================================================= */

.signature {

    position: absolute;

    left: 48px;

    bottom: 30px;

    font-size: 11px;

    letter-spacing: 2px;

    color: #777;

    text-transform: uppercase;
}


/* =========================================================
   STATUS INDICATOR
========================================================= */

.status {

    position: absolute;

    right: 48px;

    bottom: 30px;

    display: flex;

    align-items: center;

    gap: 8px;

    font-size: 11px;

    letter-spacing: 1.5px;

    color: #858585;

    text-transform: uppercase;
}


.status i {

    width: 7px;

    height: 7px;

    border-radius: 50%;

    background: #cfcfcf;

    box-shadow:
        0 0 12px rgba(255,255,255,.55);

    animation:
        pulse 2s ease-in-out infinite;
}


@keyframes pulse {

    50% {
        opacity: .35;
        transform: scale(.75);
    }
}


/* =========================================================
   RESPONSIVE
========================================================= */

@media (max-width: 900px) {

    .banner {
        transform-origin: top left;
    }

    .motif {
        opacity: .35;
    }

    h1 {
        font-size: 50px;
    }

    .tagline {
        font-size: 16px;
    }
}
</style>
</head>


<body>

<div class="banner">

    <!-- Background grid -->
    <div class="grid"></div>


    <!-- Animated light -->
    <div class="light"></div>


    <!-- Bottom wave -->
    <div class="wave"></div>


    <!-- =====================================================
         LEFT DATA VISUAL
    ====================================================== -->

    <div class="motif left">

        <div class="chart">

            <div class="bar b1"></div>

            <div class="bar b2"></div>

            <div class="bar b3"></div>

            <div class="bar b4"></div>

            <div class="bar b5"></div>

            <div class="line"></div>

        </div>

    </div>


    <!-- =====================================================
         RIGHT DATA VISUAL
    ====================================================== -->

    <div class="motif right">

        <div class="data-ring">

            <div class="ring-line"></div>

        </div>

    </div>


    <!-- =====================================================
         MAIN CONTENT
    ====================================================== -->

    <main class="content">

        <div class="inner">

            <div class="eyebrow">

                Data • Intelligence • Strategy

            </div>


            <h1>

                Nur-A-<span>Alam</span>

            </h1>


            <div class="rule"></div>


            <div class="tagline">

                <b>Data Scientist</b>

                <span class="dot">•</span>

                <b>Machine Learning</b>

                <span class="dot">•</span>

                <b>Business Analytics</b>

            </div>

        </div>

    </main>


    <!-- Bottom-left label -->

    <div class="signature">

        NUR A ALAM / PROFESSIONAL PROFILE

    </div>


    <!-- Bottom-right status -->

    <div class="status">

        <i></i>

        Data-driven professional

    </div>

</div>

</body>
</html>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=NurMithu&label=Profile%20Views&color=0a1f5c&style=for-the-badge"/>
  <img src="https://img.shields.io/github/followers/NurMithu?style=for-the-badge&color=2A52BE"/>
  <img src="https://img.shields.io/badge/Open%20to-Remote%20Work-F5C451?style=for-the-badge&labelColor=0a1f5c"/>
</p>

<p align="center">
  <a href="https://><img src="https://img.shields.io/badge/LinkedIn-Connect-2A52BE?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://github.com/NurMithu"><img src="https://img.shields.io/badge/GitHub-0a1f5c?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 👋 Hi, I'm Nur

I'm a **Data Scientist** (Postgraduate Diploma in Data Science candidate) who builds **end-to-end, production-style ML projects** — from raw data and statistical analysis to modeling, evaluation, and deployed apps.

> **My rule:** a high score means nothing without a baseline, a business interpretation, and honest limitations.

<table align="center">
<tr><td><b>🎯 Role</b></td><td>Data Scientist · ML · Business Analytics</td></tr>
<tr><td><b>🛠️ Stack</b></td><td>Python · SQL · pandas · scikit-learn · XGBoost · statsmodels · PyTorch</td></tr>
<tr><td><b>🚀 Ships</b></td><td>Streamlit apps · Dockerized models · MLflow-tracked experiments</td></tr>
<tr><td><b>💡 Principle</b></td><td>Baseline first. Business impact always.</td></tr>
<tr><td><b>🔭 Exploring</b></td><td>MLOps · RAG · LLM apps · AI agents</td></tr>
<tr><td><b>🌍 Available</b></td><td>Remote data science / ML projects</td></tr>
</table>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 📊 Results at a Glance

| Project | Headline result | Why it matters |
|---|---|---|
| 📉 **Churn & CLV** | **ROC AUC 0.789** | Threshold tuned for early-warning retention outreach |
| 📈 **Sales Forecasting** | **R² 0.926** · **~40% RMSPE cut** vs linear baseline | 1,115+ stores; **~39% avg sales lift** linked to promotions |
| 🛡️ **Fraud Detection** | **85% precision @ 85% recall** | Fraud is <1% of data, so accuracy is meaningless |
| 💬 **Sentiment Analysis** | **Macro F1 0.714** (**~39% over** 0.513 baseline) | Finds *why* customers are unhappy |

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 🚀 Featured Projects

### 📉 Customer Churn & Lifetime Value
Predicts churn and estimates lifetime value for a subscription retail business.
- Logistic Regression (churn) and Multiple Linear Regression (CLV)
- Business-oriented threshold optimization instead of the default 0.5
- **Tech:** `Python` `pandas` `scikit-learn` `statsmodels`

📂 [Repository](https://github.com/NurMithu/Zephyr_Retail_Churn_CLV_Analysis)

### 📈 Retail Sales Forecasting & Promotion Impact
Linear Regression vs Random Forest vs XGBoost on a **time-based holdout**.
- **XGBoost R² = 0.926**, ~40% lower RMSPE than the linear baseline
- **Tech:** `Python` `XGBoost` `Random Forest` `Streamlit`

📂 [Repository](https://github.com/NurMithu/sales-forecasting-rossmann) · 🚀 [Live Demo](https://sales-forecasting-rossmann-2vkhappr8sgdidmbvkorvl.streamlit.app/)

### 🛡️ Credit Card Fraud Detection
Imbalanced classification plus unsupervised anomaly detection.
- **85% precision at 85% recall** with a business-calibrated Random Forest
- **81% of fraud caught** by an autoencoder trained with no fraud labels
- **Tech:** `scikit-learn` `XGBoost` `SMOTE` `Autoencoders` `Streamlit`

📂 [Repository](https://github.com/NurMithu/fraud-detection) · 🚀 [Live Demo](https://fraud-detection-ywooiuryujcxw7q2ss5hsy.streamlit.app/)

### 💬 Customer Sentiment Analysis
Rule-based baseline vs TF-IDF + trained classifiers, plus complaint root-cause analysis.
- **Macro F1 = 0.714**, ~39% better than the rule-based baseline (0.513)
- **Tech:** `NLTK` `TF-IDF` `scikit-learn` `Streamlit`

📂 [Repository](https://github.com/NurMithu/sentiment-analysis) · 🚀 [Live Demo](https://sentiment-analysis-ytcvdn7yhftrexed7yoczj.streamlit.app/)

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 🗺️ Portfolio Roadmap

| Status | Project |
|:--:|---|
| ✅ | Churn Prediction · Sales Forecasting · Fraud Detection · NLP Sentiment |
| 🔨 | Recommendation System · Loan Default Prediction · Demand Forecasting |
| 🔜 | RAG Application · MLOps Pipeline · Real-Time Dashboard |

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 🧠 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,sql,bash,pytorch,tensorflow,sklearn,docker,git,githubactions,postgres,mongodb&perline=12"/>
</p>

## 🎯 How I Work

**Data → Exploration → Feature Engineering → Modeling → Evaluation → Interpretation → Deployment → Limitations**

1. **Baseline first** — every model must beat something simple.
2. **Right metric** — precision/recall, macro F1, RMSPE, not accuracy by default.
3. **No leakage** — time-based splits and careful feature design.
4. **Business language** — results end as recommendations, not just numbers.
5. **Honest limitations** — assumptions, bias, and failure modes documented.

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 📈 GitHub Activity

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=NurMithu&show_icons=true&bg_color=0a1530&title_color=f5c451&icon_color=7aa2ff&text_color=dbe6ff&border_color=2a52be&rank_icon=github"/>
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=NurMithu&layout=compact&bg_color=0a1530&title_color=f5c451&text_color=dbe6ff&border_color=2a52be"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=NurMithu&bg_color=0a1530&color=7aa2ff&line=2a52be&point=f5c451&area=true&area_color=2a52be&hide_border=true" width="100%"/>
</p>

<div align="center">
  <img src="https://github.com/NurMithu/NurMithu/blob/output/github-snake-dark.svg" alt="snake animation"/>
</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:020718,50:2a52be,100:020718&height=3"/>

## 🤝 Let's Work Together

I'm open to **remote data science, analytics, and ML projects**.

<p align="center">
  <a href=""><img src="https://img.shields.io/badge/Message%20me%20on%20LinkedIn-2A52BE?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:020718,50:071a52,100:2a52be&height=110&section=footer"/>
