import random, math, os
os.makedirs('assets', exist_ok=True)
os.chdir('assets')
random.seed(7)
FONT = "'Fira Code', Consolas, 'Courier New', monospace"

# ---------- 1. HERO: neural network ----------
W,H = 1000,300
layers_x = [560, 690, 820, 940]
layers_y = [[80,150,220],[50,100,150,200,250],[50,100,150,200,250],[110,190]]
nodes = [[(layers_x[i],y) for y in ys] for i,ys in enumerate(layers_y)]
s = f'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 {W} {H}" width="100%" role="img" aria-label="Nur-A-Alam, Data Scientist">
<defs>
<linearGradient id="bg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#0b1220"/><stop offset="1" stop-color="#10224a"/></linearGradient>
<pattern id="dots" width="24" height="24" patternUnits="userSpaceOnUse"><circle cx="2" cy="2" r="1" fill="#38bdf8" opacity="0.12"/></pattern>
<filter id="glow"><feGaussianBlur stdDeviation="3" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
</defs>
<rect width="{W}" height="{H}" rx="16" fill="url(#bg)"/>
<rect width="{W}" height="{H}" rx="16" fill="url(#dots)"/>
<text x="40" y="115" font-family="{FONT}" font-size="46" font-weight="700" fill="#ffffff">Nur-A-Alam</text>
<text x="42" y="158" font-family="{FONT}" font-size="18" fill="#38bdf8">Data Scientist · Machine Learning</text>
<text x="42" y="188" font-family="{FONT}" font-size="14" fill="#94a3b8">Forecasting · Fraud · NLP · Business Analytics</text>
<text x="42" y="248" font-family="{FONT}" font-size="15" fill="#22c55e">&gt;&gt;&gt; model.fit(X_train, y_train)<tspan fill="#22c55e">_<animate attributeName="opacity" values="1;1;0;0" keyTimes="0;0.5;0.5;1" dur="1s" repeatCount="indefinite"/></tspan></text>
<g stroke="#38bdf8" stroke-width="1" opacity="0.18">
'''
for i in range(3):
    for (x1,y1) in nodes[i]:
        for (x2,y2) in nodes[i+1]:
            s += f'<line x1="{x1}" y1="{y1}" x2="{x2}" y2="{y2}"/>\n'
s += '</g>\n'
# pulses (forward pass)
for i in range(3):
    for (x1,y1) in nodes[i]:
        for (x2,y2) in nodes[i+1]:
            s += (f'<circle r="2.6" fill="#7dd3fc" filter="url(#glow)" opacity="0">'
                  f'<animateMotion path="M{x1},{y1} L{x2},{y2}" dur="2.4s" begin="{i*0.6}s" repeatCount="indefinite" keyPoints="0;1;1" keyTimes="0;0.25;1" calcMode="linear"/>'
                  f'<animate attributeName="opacity" values="0;1;1;0;0" keyTimes="0;0.02;0.23;0.25;1" dur="2.4s" begin="{i*0.6}s" repeatCount="indefinite"/></circle>\n')
# nodes
for i,layer in enumerate(nodes):
    for (x,y) in layer:
        col = "#f97316" if i==3 else "#38bdf8"
        s += (f'<circle cx="{x}" cy="{y}" r="9" fill="#0f172a" stroke="{col}" stroke-width="2">'
              f'<animate attributeName="fill" values="#0f172a;{col};#0f172a;#0f172a" keyTimes="0;0.1;0.4;1" dur="2.4s" begin="{max(i*0.6-0.05,0)}s" repeatCount="indefinite"/></circle>\n')
for x,t in zip(layers_x,["input","hidden","hidden","output"]):
    s += f'<text x="{x}" y="285" text-anchor="middle" font-family="{FONT}" font-size="11" fill="#64748b">{t}</text>\n'
s += '</svg>'
open('hero-neural.svg','w').write(s)

# ---------- 2. TRAINING CURVE ----------
W,H = 1000,320
L,R,T,B = 70,950,50,260
N=60
def X(i): return L + (R-L)*i/(N-1)
loss=[];acc=[]
for i in range(N):
    l = 0.08 + 0.85*math.exp(-i/11) + random.uniform(-0.025,0.025)*math.exp(-i/40)*3
    a = 0.93 - 0.5*math.exp(-i/13) + random.uniform(-0.02,0.02)*math.exp(-i/40)*3
    loss.append(l); acc.append(a)
def path(vals): 
    return "M" + " L".join(f"{X(i):.1f},{B-(B-T)*v:.1f}" for i,v in enumerate(vals))
pl, pa = path(loss), path(acc)
dur="7s"; kt="0;0.75;1"
def dash(p,color):
    return (f'<path d="{p}" fill="none" stroke="{color}" stroke-width="3" stroke-linejoin="round" stroke-linecap="round" pathLength="1" stroke-dasharray="1" stroke-dashoffset="1" filter="url(#glow)">'
            f'<animate attributeName="stroke-dashoffset" values="1;0;0" keyTimes="{kt}" dur="{dur}" repeatCount="indefinite"/></path>')
def dot(p,color):
    return (f'<circle r="5" fill="{color}" filter="url(#glow)"><animateMotion path="{p}" dur="{dur}" repeatCount="indefinite" keyPoints="0;1;1" keyTimes="{kt}" calcMode="linear"/></circle>')
s = f'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 {W} {H}" width="100%" role="img" aria-label="Animated model training curves">
<defs><linearGradient id="bg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#0b1220"/><stop offset="1" stop-color="#10224a"/></linearGradient>
<filter id="glow"><feGaussianBlur stdDeviation="2.5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter></defs>
<rect width="{W}" height="{H}" rx="16" fill="url(#bg)"/>
<text x="40" y="32" font-family="{FONT}" font-size="15" fill="#e2e8f0">training.log</text>
<circle cx="152" cy="27" r="4" fill="#22c55e"><animate attributeName="opacity" values="1;0.2;1" dur="1.2s" repeatCount="indefinite"/></circle>
<g stroke="#334155" stroke-width="1" stroke-dasharray="3 5">
'''
for k in range(5):
    y = T + (B-T)*k/4
    s += f'<line x1="{L}" y1="{y:.0f}" x2="{R}" y2="{y:.0f}"/>\n'
s += f'</g>\n<line x1="{L}" y1="{T}" x2="{L}" y2="{B}" stroke="#64748b"/><line x1="{L}" y1="{B}" x2="{R}" y2="{B}" stroke="#64748b"/>\n'
s += f'<text x="{L}" y="{B+24}" font-family="{FONT}" font-size="12" fill="#64748b">epoch 0</text><text x="{R}" y="{B+24}" text-anchor="end" font-family="{FONT}" font-size="12" fill="#64748b">epoch 60 →</text>\n'
s += f'<g><line x1="{L}" y1="{T}" x2="{L}" y2="{B}" stroke="#38bdf8" stroke-opacity="0.35"><animateTransform attributeName="transform" type="translate" values="0 0;{R-L} 0;{R-L} 0" keyTimes="{kt}" dur="{dur}" repeatCount="indefinite"/></line></g>\n'
s += dash(pl,"#f97316") + "\n" + dash(pa,"#38bdf8") + "\n" + dot(pl,"#f97316") + "\n" + dot(pa,"#38bdf8") + "\n"
s += f'''<g font-family="{FONT}" font-size="13"><rect x="{R-250}" y="20" width="12" height="12" rx="3" fill="#f97316"/><text x="{R-232}" y="31" fill="#cbd5e1">loss ↓</text><rect x="{R-150}" y="20" width="12" height="12" rx="3" fill="#38bdf8"/><text x="{R-132}" y="31" fill="#cbd5e1">validation score ↑</text></g>
<text x="{W/2}" y="305" text-anchor="middle" font-family="{FONT}" font-size="13" fill="#94a3b8">baseline → model → better model · measured, not assumed</text>
</svg>'''
open('training-curve.svg','w').write(s)

# ---------- 3. PIPELINE ----------
W,H=1000,190
xs=[30,225,420,615,810]
labels=[("01","Data","SQL · CSV · APIs"),("02","Features","leakage-safe"),("03","Model","XGBoost · RF · LR"),("04","Evaluate","vs. baseline"),("05","Deploy","Streamlit · Docker")]
s=f'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 {W} {H}" width="100%" role="img" aria-label="Animated data science pipeline">
<defs><linearGradient id="bg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#0b1220"/><stop offset="1" stop-color="#10224a"/></linearGradient>
<filter id="glow"><feGaussianBlur stdDeviation="3" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter></defs>
<rect width="{W}" height="{H}" rx="16" fill="url(#bg)"/>
'''
for i in range(4):
    x1=xs[i]+150; x2=xs[i+1]
    s+=f'<line x1="{x1}" y1="100" x2="{x2}" y2="100" stroke="#38bdf8" stroke-width="2" stroke-dasharray="6 6" opacity="0.7"><animate attributeName="stroke-dashoffset" values="24;0" dur="1s" repeatCount="indefinite"/></line>\n'
for i,(x,(n,t,sub)) in enumerate(zip(xs,labels)):
    s+=(f'<rect x="{x}" y="60" width="150" height="80" rx="12" fill="#0f172a" stroke="#334155" stroke-width="2">'
        f'<animate attributeName="stroke" values="#334155;#38bdf8;#334155;#334155" keyTimes="0;0.1;0.3;1" dur="4.2s" begin="{i*0.84}s" repeatCount="indefinite"/></rect>\n'
        f'<text x="{x+14}" y="50" font-family="{FONT}" font-size="12" fill="#64748b">{n}</text>\n'
        f'<text x="{x+75}" y="96" text-anchor="middle" font-family="{FONT}" font-size="20" font-weight="700" fill="#ffffff">{t}</text>\n'
        f'<text x="{x+75}" y="120" text-anchor="middle" font-family="{FONT}" font-size="11" fill="#94a3b8">{sub}</text>\n')
for k in range(3):
    s+=(f'<circle r="6" fill="#7dd3fc" filter="url(#glow)"><animateMotion path="M30,100 L960,100" dur="4.2s" begin="{k*1.4}s" repeatCount="indefinite"/></circle>\n')
s+=f'<text x="{W/2}" y="175" text-anchor="middle" font-family="{FONT}" font-size="13" fill="#94a3b8">Data → Insight → Model → Evaluation → Deployment → Business Impact</text>\n</svg>'
open('pipeline.svg','w').write(s)

os.chdir('..')
README = r'''<p align="center">
  <img src="assets/hero-neural.svg" alt="Nur-A-Alam - Data Scientist" width="100%"/>
</p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&pause=1000&color=38BDF8&center=true&vCenter=true&width=760&lines=I+turn+messy+data+into+business+decisions;Churn+%7C+Fraud+%7C+Forecasting+%7C+NLP;Every+model+is+benchmarked+against+a+baseline;Open+to+remote+ML+%26+data+science+work" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=NurMithu&label=Profile%20Views&color=2563EB&style=for-the-badge" alt="Profile Views"/>
  <img src="https://img.shields.io/github/followers/NurMithu?style=for-the-badge&color=2563EB" alt="Followers"/>
  <img src="https://img.shields.io/badge/Open%20to-Remote%20Work-38BDF8?style=for-the-badge" alt="Open to remote"/>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/nur-a-alam-b8935a215/"><img src="https://img.shields.io/badge/LinkedIn-Connect-1E77B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="#-featured-projects"><img src="https://img.shields.io/badge/Jump%20to-Projects-2563EB?style=for-the-badge"/></a>
</p>

---

## 👋 Hi, I'm Nur

I'm a **Data Scientist** (Postgraduate Diploma in Data Science candidate) who builds **end-to-end, production-style ML projects** — from raw data and statistical analysis to modeling, evaluation, and deployed apps.

> **My rule:** a high score means nothing without a baseline, a business interpretation, and honest limitations.

```python
class NurAAlam:
    role      = "Data Scientist | ML | Business Analytics"
    stack     = ["Python", "SQL", "pandas", "scikit-learn", "XGBoost", "statsmodels", "PyTorch"]
    ships     = ["Streamlit apps", "Dockerized models", "MLflow-tracked experiments"]
    principle = "Baseline first. Business impact always."
    exploring = ["MLOps", "RAG", "LLM apps", "AI agents"]
    available = "Remote data science / ML projects"
```

---

## 📊 Results at a Glance

<p align="center">
  <img src="assets/training-curve.svg" alt="Animated training curves" width="100%"/>
</p>

| Project | Headline result | Why it matters |
|---|---|---|
| 📉 **Churn & CLV** | **ROC AUC 0.789** | Threshold tuned for early-warning retention outreach |
| 📈 **Sales Forecasting** | **R² 0.926** · **~40% RMSPE cut** vs linear baseline | 1,115+ stores; **~39% avg sales lift** linked to promotions |
| 🛡️ **Fraud Detection** | **85% precision @ 85% recall** | Fraud is <1% of data, so accuracy is meaningless |
| 💬 **Sentiment Analysis** | **Macro F1 0.714** (**~39% over** 0.513 baseline) | Finds *why* customers are unhappy |

---

## 🚀 Featured Projects

### 📉 Customer Churn & Lifetime Value
Predicts churn and estimates lifetime value for a subscription retail business, covering data quality, EDA, statistical testing, feature engineering, and business recommendations.

- Logistic Regression (churn) and Multiple Linear Regression (CLV)
- Business-oriented threshold optimization instead of the default 0.5
- **Tech:** `Python` `pandas` `scikit-learn` `statsmodels`

📂 [Repository](https://github.com/NurMithu/Zephyr_Retail_Churn_CLV_Analysis)

---

### 📈 Retail Sales Forecasting & Promotion Impact
Compares Linear Regression, Random Forest, and XGBoost on a **time-based holdout** to avoid leakage, then translates results into promotion and store-level insights.

- **XGBoost R² = 0.926**, about **40% lower RMSPE** than the linear baseline
- **Tech:** `Python` `XGBoost` `Random Forest` `Streamlit`

📂 [Repository](https://github.com/NurMithu/sales-forecasting-rossmann) · 🚀 [Live Demo](https://sales-forecasting-rossmann-2vkhappr8sgdidmbvkorvl.streamlit.app/)

---

### 🛡️ Credit Card Fraud Detection
Imbalanced classification plus unsupervised anomaly detection, focused on precision, recall, and threshold calibration.

- **85% precision at 85% recall** with a business-calibrated Random Forest
- **81% of fraud caught** by an autoencoder trained with *no* fraud labels
- **Tech:** `scikit-learn` `XGBoost` `SMOTE` `Autoencoders` `Streamlit`

📂 [Repository](https://github.com/NurMithu/fraud-detection) · 🚀 [Live Demo](https://fraud-detection-ywooiuryujcxw7q2ss5hsy.streamlit.app/)

---

### 💬 Customer Sentiment Analysis
Rule-based baseline vs. TF-IDF + trained classifiers, followed by brand benchmarking and complaint root-cause analysis.

- **Macro F1 = 0.714**, about **39% better** than the rule-based baseline (0.513)
- **Tech:** `NLTK` `TF-IDF` `scikit-learn` `Streamlit`

📂 [Repository](https://github.com/NurMithu/sentiment-analysis) · 🚀 [Live Demo](https://sentiment-analysis-ytcvdn7yhftrexed7yoczj.streamlit.app/)

---

## 🗺️ Portfolio Roadmap

| Status | Project |
|:--:|---|
| ✅ | Churn Prediction · Sales Forecasting · Fraud Detection · NLP Sentiment |
| 🔨 | Recommendation System · Loan Default Prediction · Demand Forecasting |
| 🔜 | RAG Application · MLOps Pipeline (MLflow + Docker + CI/CD) · Real-Time Dashboard |

---

## 🧠 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,sql,bash,pytorch,tensorflow,sklearn,docker,git,githubactions,postgres,mongodb&perline=12" alt="Tech Stack"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/XGBoost-FF6600?style=flat-square&logo=xgboost&logoColor=white"/>
  <img src="https://img.shields.io/badge/Statsmodels-3B5B92?style=flat-square"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white"/>
</p>

| Area | Tools |
|---|---|
| **Data & Stats** | pandas, NumPy, statsmodels, hypothesis testing |
| **Machine Learning** | scikit-learn, XGBoost, Random Forest, SMOTE |
| **Deep Learning** | PyTorch, TensorFlow, CNN, LSTM, Autoencoders |
| **Engineering** | Git, GitHub Actions, Docker, PostgreSQL, MongoDB |
| **Deployment** | Streamlit Cloud, MLflow, Model APIs |
| **Exploring** | MLOps, LLMs, RAG, AI Agents |

---

## 🎯 How I Work

<p align="center">
  <img src="assets/pipeline.svg" alt="Animated data science pipeline" width="100%"/>
</p>

**Data → Exploration → Feature Engineering → Modeling → Evaluation → Interpretation → Deployment → Limitations**

1. **Baseline first** — every model must beat something simple.
2. **Right metric** — precision/recall, macro F1, RMSPE, not accuracy by default.
3. **No leakage** — time-based splits and careful feature design.
4. **Business language** — results end as recommendations, not just numbers.
5. **Honest limitations** — assumptions, bias, and failure modes documented.

---

## 📈 GitHub Stats

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=NurMithu&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" alt="GitHub Stats"/>
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=NurMithu&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=NurMithu&theme=tokyonight&hide_border=true" alt="GitHub Streak"/>
</p>

<div align="center">
  <img src="https://github.com/NurMithu/NurMithu/blob/output/github-snake-dark.svg" alt="snake animation"/>
</div>

---

## 🤝 Let's Work Together

I'm open to **remote data science, analytics, and ML projects** — churn and customer analytics, forecasting, fraud detection, NLP, and deployed ML apps.

<p align="center">
  <a href="https://www.linkedin.com/in/nur-a-alam-b8935a215/"><img src="https://img.shields.io/badge/Message%20me%20on%20LinkedIn-1E77B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
</p>

<div align="center">

### ⭐ Building practical machine learning systems, one project at a time.
*Every result is evaluated against a baseline.*

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1220,50:2563eb,100:38bdf8&height=100&section=footer"/>
'''
open('README.md','w',encoding='utf-8').write(README)
print('Done! Created README.md and assets/ (3 animated SVGs). Now: git add . && git commit -m "profile" && git push')
