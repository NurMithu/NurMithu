<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Nur A Alam | Data Scientist</title>
<meta name="description" content="Nur A Alam is a data scientist working on machine learning, analytics and business intelligence.">
<meta property="og:title" content="Nur A Alam | Data Scientist">
<meta property="og:description" content="Machine learning, analytics and business intelligence.">
<meta name="color-scheme" content="dark">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='12' fill='%230B0F15'/%3E%3Ctext x='32' y='43' font-family='Arial' font-weight='700' font-size='30' text-anchor='middle' fill='%235BC8E8'%3ENA%3C/text%3E%3C/svg%3E">
<style>
:root{
  --bg:#0B0F15; --panel:#10161F; --line:#1F2937;
  --text:#F1F5F9; --muted:#94A3B8;
  --cyan:#5BC8E8; --amber:#E8A857;
  --serif:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
  --sans:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
  --mono:ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;scroll-padding-top:70px}
body{background:var(--bg);color:var(--text);font-family:var(--sans);line-height:1.65;-webkit-font-smoothing:antialiased}
a{color:inherit;text-decoration:none}
:focus-visible{outline:2px solid var(--cyan);outline-offset:3px;border-radius:4px}
.wrap{width:min(1080px,100% - 40px);margin-inline:auto}
.skip{position:absolute;left:-999px;top:8px;background:var(--cyan);color:#041018;padding:8px 14px;border-radius:6px;z-index:50}
.skip:focus{left:8px}

/* nav */
header.nav{position:sticky;top:0;z-index:20;background:rgba(10,14,20,.88);backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;gap:16px;min-height:56px;flex-wrap:wrap;padding-block:6px}
.logo{font-size:17px;font-weight:700;letter-spacing:-.01em}
.nav ul{display:flex;gap:24px;list-style:none;flex-wrap:wrap}
.nav-right{display:flex;align-items:center;gap:24px;flex-wrap:wrap}
.nav-cta{font-size:14px;font-weight:600;padding:7px 14px;border:1px solid var(--line);border-radius:6px;transition:border-color .2s,color .2s}
.nav-cta:hover{border-color:var(--cyan);color:var(--cyan)}
.nav ul a{font-size:14px;color:var(--muted);transition:color .2s}
.nav ul a:hover{color:var(--cyan)}

/* hero */
.hero{padding:clamp(48px,9vw,110px) 0 clamp(40px,7vw,90px);border-bottom:1px solid var(--line);background:var(--bg)}
.hero .wrap{display:grid;grid-template-columns:1.1fr .9fr;gap:48px;align-items:center}
.hero h1{font-weight:700;font-size:clamp(42px,6.5vw,76px);line-height:1.04;letter-spacing:-.035em}
.hero .role{margin-top:20px;font-size:clamp(17px,2vw,20px);color:var(--muted);max-width:30em}
.focus{list-style:none;display:flex;gap:0;margin-top:28px;flex-wrap:wrap}
.focus li{padding:0 20px;border-left:1px solid var(--line);font-size:14px;color:var(--muted)}
.focus li:first-child{padding-left:0;border-left:0}
.hero .role b{color:var(--text);font-weight:600}
.actions{margin-top:32px;display:flex;gap:12px;flex-wrap:wrap}
.btn{display:inline-block;padding:11px 22px;border-radius:6px;font-weight:600;font-size:15px;border:1px solid var(--line);transition:transform .2s,border-color .2s,background .2s}
.btn:hover{transform:translateY(-2px);border-color:var(--cyan)}
.btn.primary{background:var(--cyan);color:#041018;border-color:var(--cyan)}
.btn.primary:hover{background:#86d6ee}

/* hero neural network */
.plot{background:var(--panel);border:1px solid var(--line);border-radius:8px;padding:18px 18px 10px}
.plot-head{display:flex;justify-content:space-between;gap:12px;align-items:baseline}
.plot-head strong{font-size:20px}
.plot-head span{font-size:14px;color:var(--muted)}
.plot-sub{font-family:var(--mono);font-size:13px;color:var(--muted);margin-top:4px}
.plot canvas{display:block;width:100%;aspect-ratio:4/3}

/* sections */
section{padding:clamp(56px,8vw,96px) 0;border-bottom:1px solid var(--line)}
h2{font-size:clamp(26px,3.6vw,38px);line-height:1.18;letter-spacing:-.025em;font-weight:700;max-width:20em}
.lead{color:var(--muted);margin-top:14px;max-width:38em}
.head{margin-bottom:40px}

.about{display:grid;grid-template-columns:1.2fr .8fr;gap:48px}
.about p{color:var(--muted);margin-bottom:16px;max-width:40em}
.about p strong{color:var(--text);font-weight:600}
.facts{border:1px solid var(--line);border-radius:8px;background:var(--panel);padding:8px 24px;align-self:start}
.facts div{padding:16px 0;border-bottom:1px solid var(--line)}
.facts div:last-child{border-bottom:0}
.facts dt{font-size:13px;color:var(--muted)}
.facts dd{font-weight:600;margin-top:2px}

/* projects */
.proj{list-style:none;border-top:1px solid var(--line)}
.proj li{transition:background .2s;display:grid;grid-template-columns:.9fr 1.6fr auto;gap:28px;align-items:start;padding:28px 0;border-bottom:1px solid var(--line)}
.proj h3{font-size:21px;line-height:1.25;letter-spacing:-.015em}
.proj p{color:var(--muted);font-size:15px}
.tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:14px;list-style:none}
.tags li{display:block;padding:3px 10px;border:1px solid var(--line);border-radius:999px;font-size:12px;color:#BFE9F5;background:rgba(91,200,232,.06)}
.proj li:hover{background:rgba(255,255,255,.015)}
.proj .go{font-size:14px;font-weight:600;color:var(--cyan);white-space:nowrap;padding-top:6px}
.proj .go:hover{text-decoration:underline;text-underline-offset:4px}

/* process */
.steps{list-style:none;counter-reset:s;display:grid;grid-template-columns:repeat(5,1fr);gap:0;border:1px solid var(--line);border-radius:8px;overflow:hidden}
.steps li{counter-increment:s;padding:24px 20px;background:var(--panel);border-right:1px solid var(--line)}
.steps li:last-child{border-right:0}
.steps li:before{content:counter(s);display:block;font-family:var(--mono);color:var(--amber);font-size:13px;margin-bottom:12px}
.steps h3{font-size:17px;margin-bottom:6px}
.steps p{font-size:14px;color:var(--muted)}

/* toolkit */
.kit{display:grid;grid-template-columns:repeat(3,1fr);gap:28px}
.kit h3{font-size:15px;color:var(--amber);font-weight:600;margin-bottom:12px}
.kit ul{list-style:none;display:flex;flex-wrap:wrap;gap:8px}
.kit li{padding:6px 12px;border:1px solid var(--line);border-radius:8px;background:var(--panel);font-size:14px}

/* contact */
.contact{display:grid;grid-template-columns:1fr 1fr;gap:48px;align-items:center}
.links{list-style:none;border:1px solid var(--line);border-radius:8px;background:var(--panel)}
.links li{border-bottom:1px solid var(--line)}
.links li:last-child{border-bottom:0}
.links a{display:flex;justify-content:space-between;gap:12px;padding:18px 24px;transition:color .2s,background .2s}
.links a:hover{color:var(--cyan);background:rgba(91,200,232,.05)}
.links span{color:var(--muted);font-size:14px;overflow-wrap:anywhere;text-align:right}

footer{padding:28px 0;color:var(--muted);font-size:13px}
footer .wrap{display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap}

@media(max-width:900px){
  .hero .wrap,.about,.contact{grid-template-columns:1fr;gap:32px}
  .proj li{grid-template-columns:1fr;gap:12px}
  .steps{grid-template-columns:1fr 1fr}
  .steps li{border-bottom:1px solid var(--line)}
  .kit{grid-template-columns:1fr}
}
@media(max-width:560px){
  .nav ul{gap:14px}
  .steps{grid-template-columns:1fr}
  .steps li{border-right:0}
}
@media(prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  .btn{transition:none}
}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>

<header class="nav">
  <div class="wrap">
    <a class="logo" href="#top">Nur A Alam</a>
    <div class="nav-right">
      <nav aria-label="Main">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#projects">Work</a></li>
          <li><a href="#process">Process</a></li>
          <li><a href="#toolkit">Toolkit</a></li>
        </ul>
      </nav>
      <a class="nav-cta" href="#contact">Contact</a>
    </div>
  </div>
</header>

<main id="main">
<div class="hero" id="top">
  <div class="wrap">
    <div>
      <h1>Nur A Alam</h1>
      <p class="role"><b>Data scientist.</b> I build machine learning models and analytics that help teams make better decisions.</p>
      <ul class="focus" aria-label="Focus areas"><li>Machine learning</li><li>Business analytics</li><li>Data visualization</li></ul>
      <div class="actions">
        <a class="btn primary" href="#projects">See my work</a>
        <a class="btn" href="#contact">Contact me</a>
      </div>
    </div>

    <figure class="plot">
      <div class="plot-head"><strong>Neural network</strong><span>Training run</span></div>
      <p class="plot-sub" id="stat">epoch 0 · loss 1.000</p>
      <canvas id="cloud" role="img" aria-label="Animated neural network. Signals pass forward through four layers while a loss curve below falls as training epochs advance."></canvas>
    </figure>
  </div>
</div>

<section id="about">
  <div class="wrap">
    <div class="head">
      <h2>Analysis that leads to a decision.</h2>
    </div>
    <div class="about">
      <div>
        <p>I work across <strong>data science, machine learning and business analytics</strong>. I start with the question the business needs answered, then choose the simplest method that answers it well.</p>
        <p>That covers data preparation, exploratory analysis, predictive modelling and clear reporting, so the people who act on the results can trust and understand them.</p>
      </div>
      <dl class="facts">
        <div><dt>Focus</dt><dd>Data science and machine learning</dd></div>
        <div><dt>Specialty</dt><dd>Predictive and business analytics</dd></div>
        <div><dt>Output</dt><dd>Models, dashboards and clear recommendations</dd></div>
      </dl>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="head">
      <h2>Selected work</h2>
      <p class="lead">Four areas of practice, each linked to the related repositories on GitHub.</p>
    </div>
    <ul class="proj">
      <li>
        <h3>Business intelligence</h3>
        <div>
          <p>Dashboards and reporting that turn operational data into a clear view of performance for managers and executives.</p>
          <ul class="tags"><li>Power BI</li><li>SQL</li><li>Dashboards</li></ul>
        </div>
        <a class="go" href="https://github.com/YOUR-USERNAME?tab=repositories" target="_blank" rel="noopener">View repositories</a>
      </li>
      <li>
        <h3>Predictive analytics</h3>
        <div>
          <p>Machine learning workflows that find patterns, forecast outcomes and show how reliable each prediction is.</p>
          <ul class="tags"><li>Python</li><li>Scikit-learn</li><li>Statistics</li></ul>
        </div>
        <a class="go" href="https://github.com/YOUR-USERNAME?tab=repositories" target="_blank" rel="noopener">View repositories</a>
      </li>
      <li>
        <h3>AI and automation</h3>
        <div>
          <p>Automated data workflows that combine APIs and AI models to remove repetitive manual work.</p>
          <ul class="tags"><li>Python</li><li>APIs</li><li>Automation</li></ul>
        </div>
        <a class="go" href="https://github.com/YOUR-USERNAME?tab=repositories" target="_blank" rel="noopener">View repositories</a>
      </li>
      <li>
        <h3>Strategic analytics</h3>
        <div>
          <p>KPI frameworks that connect analysis to planning, so teams can measure progress against their priorities.</p>
          <ul class="tags"><li>KPIs</li><li>Analysis</li><li>Decision support</li></ul>
        </div>
        <a class="go" href="https://github.com/YOUR-USERNAME?tab=repositories" target="_blank" rel="noopener">View repositories</a>
      </li>
    </ul>
  </div>
</section>

<section id="process">
  <div class="wrap">
    <div class="head">
      <h2>How I work</h2>
    </div>
    <ol class="steps">
      <li><h3>Discover</h3><p>Define the business question and check what data exists.</p></li>
      <li><h3>Prepare</h3><p>Clean and structure the data for analysis.</p></li>
      <li><h3>Analyze</h3><p>Find patterns, trends and relationships.</p></li>
      <li><h3>Model</h3><p>Build and validate a model when one is needed.</p></li>
      <li><h3>Deliver</h3><p>Share findings in a report or dashboard people can act on.</p></li>
    </ol>
  </div>
</section>

<section id="toolkit">
  <div class="wrap">
    <div class="head">
      <h2>Toolkit</h2>
    </div>
    <div class="kit">
      <div><h3>Programming and data</h3><ul><li>Python</li><li>SQL</li><li>Pandas</li><li>NumPy</li></ul></div>
      <div><h3>Modelling</h3><ul><li>Scikit-learn</li><li>Machine learning</li><li>Statistics</li></ul></div>
      <div><h3>Communication</h3><ul><li>Power BI</li><li>Data visualization</li><li>Business analytics</li></ul></div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap contact">
    <div>
      <h2>Let’s discuss your data challenge.</h2>
      <p class="lead">Send a short description of the question and the data available, and I will reply with a suggested approach.</p>
    </div>
    <ul class="links">
      <li><a href="mailto:your-email@example.com">Email <span>your-email@example.com</span></a></li>
      <li><a href="https://github.com/YOUR-USERNAME" target="_blank" rel="noopener">GitHub <span>github.com/YOUR-USERNAME</span></a></li>
      <li><a href="https://www.linkedin.com/in/YOUR-PROFILE" target="_blank" rel="noopener">LinkedIn <span>linkedin.com/in/YOUR-PROFILE</span></a></li>
    </ul>
  </div>
</section>
</main>

<footer>
  <div class="wrap">
    <span>© 2026 Nur A Alam</span>
    <span>Data science, machine learning and analytics</span>
  </div>
</footer>

<script>
(function () {
  var cv = document.getElementById("cloud");
  if (!cv || !cv.getContext) return;
  var ctx = cv.getContext("2d"), W = 0, H = 0, lastEpoch = -1;
  var reduce = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  var layers = [4, 6, 6, 3], PERIOD = 1200, EPOCHS = 40;
  var seed = 5;
  function rnd() { seed = (seed * 16807) % 2147483647; return seed / 2147483647; }

  var edges = [], li, a, b;
  for (li = 0; li < layers.length - 1; li++)
    for (a = 0; a < layers[li]; a++)
      for (b = 0; b < layers[li + 1]; b++)
        edges.push({ l: li, a: a, b: b, w: rnd() });

  var loss = [];
  for (var e = 0; e <= EPOCHS; e++)
    loss.push(0.12 + 0.88 * Math.exp(-e / 9) + 0.025 * Math.sin(e * 1.7) * Math.exp(-e / 25));

  function node(l, i) {
    var top = H * 0.1, bot = H * 0.62, n = layers[l];
    return { x: W * (0.12 + 0.76 * l / (layers.length - 1)), y: n === 1 ? (top + bot) / 2 : top + (bot - top) * i / (n - 1) };
  }

  function size() {
    var r = cv.getBoundingClientRect(), d = Math.min(window.devicePixelRatio || 1, 2);
    W = r.width; H = r.height;
    cv.width = Math.round(W * d); cv.height = Math.round(H * d);
    ctx.setTransform(d, 0, 0, d, 0, 0);
  }

  function draw(wave, epoch) {
    var i, j, p, q, ed, loc, act, x0 = W * 0.12, x1 = W * 0.88, y0 = H * 0.76, y1 = H * 0.95;
    ctx.clearRect(0, 0, W, H);

    for (i = 0; i < edges.length; i++) {
      ed = edges[i]; p = node(ed.l, ed.a); q = node(ed.l + 1, ed.b);
      ctx.strokeStyle = "rgba(148,163,184," + (0.05 + 0.13 * ed.w).toFixed(3) + ")";
      ctx.lineWidth = 1;
      ctx.beginPath(); ctx.moveTo(p.x, p.y); ctx.lineTo(q.x, q.y); ctx.stroke();
      loc = wave - ed.l;
      if (wave >= 0 && loc > 0 && loc < 1 && ed.w > 0.4) {
        ctx.fillStyle = "rgba(91,200,232," + (0.35 + 0.6 * ed.w).toFixed(2) + ")";
        ctx.beginPath(); ctx.arc(p.x + (q.x - p.x) * loc, p.y + (q.y - p.y) * loc, 2.2, 0, 6.2832); ctx.fill();
      }
    }

    for (j = 0; j < layers.length; j++) {
      act = wave < 0 ? 0 : Math.max(0, 1 - Math.abs(wave - j) * 1.4);
      for (i = 0; i < layers[j]; i++) {
        p = node(j, i);
        if (act > 0) {
          ctx.fillStyle = "rgba(91,200,232," + (0.18 * act).toFixed(3) + ")";
          ctx.beginPath(); ctx.arc(p.x, p.y, 13, 0, 6.2832); ctx.fill();
        }
        ctx.fillStyle = "#10161F";
        ctx.strokeStyle = act > 0.15 ? "rgba(91,200,232," + (0.5 + 0.5 * act).toFixed(2) + ")" : "rgba(148,163,184,.55)";
        ctx.lineWidth = 1.6;
        ctx.beginPath(); ctx.arc(p.x, p.y, 6, 0, 6.2832); ctx.fill(); ctx.stroke();
      }
    }

    ctx.strokeStyle = "#1F2937"; ctx.lineWidth = 1;
    ctx.beginPath(); ctx.moveTo(x0, y0); ctx.lineTo(x0, y1); ctx.lineTo(x1, y1); ctx.stroke();
    ctx.strokeStyle = "rgba(232,168,87,.95)"; ctx.lineWidth = 2; ctx.lineJoin = "round";
    ctx.beginPath();
    for (i = 0; i <= epoch; i++) {
      p = x0 + (x1 - x0) * i / EPOCHS; q = y1 - (y1 - y0) * Math.min(1, (loss[i] - 0.1) / 0.95);
      if (i === 0) ctx.moveTo(p, q); else ctx.lineTo(p, q);
    }
    ctx.stroke();
    ctx.fillStyle = "#E8A857";
    ctx.beginPath(); ctx.arc(p, q, 3.5, 0, 6.2832); ctx.fill();
    ctx.fillStyle = "#94A3B8"; ctx.font = "11px ui-monospace,Menlo,Consolas,monospace";
    ctx.fillText("loss", x0 + 6, y0 + 10);
    ctx.fillText("epoch", x1 - 36, y1 - 6);
  }

  var stat = document.getElementById("stat");
  function label(epoch) {
    if (stat && epoch !== lastEpoch) { lastEpoch = epoch; stat.textContent = "epoch " + epoch + " · loss " + loss[epoch].toFixed(3); }
  }

  function frame(ts) {
    var cycle = ts / PERIOD, epoch = Math.floor(cycle) % (EPOCHS + 1);
    var wave = (cycle - Math.floor(cycle)) * 4.2 - 0.3;
    draw(wave, epoch); label(epoch);
    requestAnimationFrame(frame);
  }

  function still() { draw(-1, EPOCHS); label(EPOCHS); }
  size();
  window.addEventListener("resize", function () { size(); if (reduce) still(); });
  if (reduce) still(); else requestAnimationFrame(frame);
})();
</script>
</body>
</html>
