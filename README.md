<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Hassan Ali — Full-Stack Engineer</title>
<meta name="description" content="Full-stack engineer. Schema to Nginx config, same person. Rails, NestJS, Next.js, Python, Laravel.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --paper:#FBFBF9;
  --paper-2:#F3F2EE;
  --ink:#0B0B0C;
  --ink-60:#5A5A5E;
  --ink-35:#9A9A9E;
  --rule:#E2E1DC;
  --accent:#D6432B;
  --accent-soft:#FBEAE6;
  --blue:#1D4ED8;
  --ease:cubic-bezier(.16,1,.3,1);
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-font-smoothing:antialiased}
body{
  background:var(--paper);color:var(--ink);
  font-family:'Inter',-apple-system,sans-serif;
  font-size:16px;line-height:1.65;overflow-x:hidden;
}
::selection{background:var(--accent);color:#fff}

/* ---------- grain ---------- */
body::after{
  content:'';position:fixed;inset:0;pointer-events:none;z-index:9999;opacity:.035;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='3'/%3E%3C/filter%3E%3Crect width='200' height='200' filter='url(%23n)'/%3E%3C/svg%3E");
}

/* ---------- progress ---------- */
#progress{position:fixed;top:0;left:0;height:2px;width:0;background:var(--accent);z-index:200;transition:width .1s linear}

/* ---------- cursor glow ---------- */
#glow{position:fixed;width:420px;height:420px;border-radius:50%;pointer-events:none;z-index:0;
  background:radial-gradient(circle,rgba(214,67,43,.055),transparent 62%);
  transform:translate(-50%,-50%);transition:opacity .4s;opacity:0}
@media (hover:none){#glow{display:none}}

/* ---------- layout ---------- */
.wrap{max-width:1180px;margin:0 auto;padding:0 32px;position:relative;z-index:1}
section{padding:120px 0;position:relative}

.eyebrow{
  font-family:'JetBrains Mono',monospace;font-size:11px;letter-spacing:.22em;
  text-transform:uppercase;color:var(--ink-35);display:flex;align-items:center;gap:14px;margin-bottom:44px
}
.eyebrow::after{content:'';flex:1;height:1px;background:var(--rule);
  transform:scaleX(0);transform-origin:left;transition:transform 1.1s var(--ease)}
.in-view .eyebrow::after{transform:scaleX(1)}

h2.display{font-family:'Instrument Serif',Georgia,serif;font-weight:400;
  font-size:clamp(38px,5.4vw,68px);line-height:1.02;letter-spacing:-.02em;margin-bottom:26px}
h2.display em{font-style:italic;color:var(--accent)}

/* ---------- nav ---------- */
nav{position:fixed;top:0;left:0;right:0;z-index:150;
  backdrop-filter:blur(14px);background:rgba(251,251,249,.72);
  border-bottom:1px solid transparent;transition:border-color .35s,padding .35s}
nav.stuck{border-color:var(--rule)}
.nav-in{max-width:1180px;margin:0 auto;padding:18px 32px;display:flex;justify-content:space-between;align-items:center}
.logo{font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:500;letter-spacing:.04em;text-decoration:none;color:var(--ink)}
.logo span{color:var(--accent)}
.nav-links{display:flex;gap:30px;align-items:center}
.nav-links a{font-size:13px;color:var(--ink-60);text-decoration:none;position:relative;transition:color .25s}
.nav-links a::after{content:'';position:absolute;left:0;bottom:-4px;width:100%;height:1px;background:var(--ink);
  transform:scaleX(0);transform-origin:right;transition:transform .4s var(--ease)}
.nav-links a:hover{color:var(--ink)}
.nav-links a:hover::after{transform:scaleX(1);transform-origin:left}
@media(max-width:720px){.nav-links a:not(.pill){display:none}}
.pill{border:1px solid var(--ink);border-radius:100px;padding:8px 18px !important;color:var(--ink) !important;font-weight:500;transition:all .3s var(--ease)}
.pill::after{display:none}
.pill:hover{background:var(--ink);color:var(--paper) !important}

/* ---------- hero ---------- */
#hero{padding-top:180px;padding-bottom:80px;min-height:100vh;display:flex;flex-direction:column;justify-content:center}
.status{display:inline-flex;align-items:center;gap:9px;font-family:'JetBrains Mono',monospace;
  font-size:11px;letter-spacing:.16em;text-transform:uppercase;color:var(--ink-60);
  border:1px solid var(--rule);border-radius:100px;padding:7px 15px;margin-bottom:34px;background:#fff}
.dot{width:6px;height:6px;border-radius:50%;background:#16A34A;animation:ping 2s ease-in-out infinite}
@keyframes ping{0%,100%{box-shadow:0 0 0 0 rgba(22,163,74,.5)}50%{box-shadow:0 0 0 6px rgba(22,163,74,0)}}

.hero-name{font-family:'Instrument Serif',Georgia,serif;font-weight:400;
  font-size:clamp(60px,12.5vw,168px);line-height:.88;letter-spacing:-.035em;margin-bottom:34px}
.hero-name .ln{display:block;overflow:hidden}
.hero-name .ln>span{display:block;transform:translateY(105%);
  animation:maskUp 1.15s var(--ease) forwards}
.hero-name .ln:nth-child(2)>span{animation-delay:.11s}
@keyframes maskUp{to{transform:translateY(0)}}
.hero-name i{font-style:italic;color:var(--accent)}

.hero-grid{display:grid;grid-template-columns:1.35fr 1fr;gap:60px;align-items:end;margin-top:20px}
@media(max-width:860px){.hero-grid{grid-template-columns:1fr;gap:38px}}
.lead{font-size:clamp(17px,2vw,21px);line-height:1.55;color:var(--ink-60);max-width:600px}
.lead b{color:var(--ink);font-weight:600}

.rotator{font-family:'JetBrains Mono',monospace;font-size:12.5px;color:var(--ink-60);
  height:22px;overflow:hidden;position:relative}
.rotator ul{list-style:none;animation:roll 12s steps(4) infinite}
.rotator li{height:22px;line-height:22px;white-space:nowrap}
@keyframes roll{to{transform:translateY(-88px)}}

.hero-meta{border-left:1px solid var(--rule);padding-left:26px}
.hero-meta div{font-family:'JetBrains Mono',monospace;font-size:11.5px;color:var(--ink-35);
  display:flex;justify-content:space-between;padding:9px 0;border-bottom:1px solid var(--rule)}
.hero-meta div b{color:var(--ink);font-weight:500}
.hero-meta div:last-child{border:none}

/* ---------- marquee ---------- */
.marquee{border-top:1px solid var(--rule);border-bottom:1px solid var(--rule);
  padding:20px 0;overflow:hidden;white-space:nowrap;background:var(--paper-2)}
.marquee-track{display:inline-flex;gap:0;animation:slide 42s linear infinite}
.marquee:hover .marquee-track{animation-play-state:paused}
@keyframes slide{to{transform:translateX(-50%)}}
.marquee-track span{font-family:'JetBrains Mono',monospace;font-size:13px;color:var(--ink-60);padding:0 26px;position:relative}
.marquee-track span::after{content:'—';position:absolute;right:-6px;color:var(--accent);opacity:.45}

/* ---------- reveal ---------- */
.rv{opacity:0;transform:translateY(26px);transition:opacity .9s var(--ease),transform .9s var(--ease)}
.in-view .rv,.rv.in-view{opacity:1;transform:none}
.in-view .rv:nth-child(1){transition-delay:.03s}
.in-view .rv:nth-child(2){transition-delay:.09s}
.in-view .rv:nth-child(3){transition-delay:.15s}
.in-view .rv:nth-child(4){transition-delay:.21s}
.in-view .rv:nth-child(5){transition-delay:.27s}
.in-view .rv:nth-child(6){transition-delay:.33s}

/* ---------- capability cards ---------- */
.caps{display:grid;grid-template-columns:repeat(2,1fr);gap:0;border-top:1px solid var(--rule)}
@media(max-width:820px){.caps{grid-template-columns:1fr}}
.cap{padding:38px 34px 38px 0;border-bottom:1px solid var(--rule);position:relative;transition:padding-left .45s var(--ease)}
.caps .cap:nth-child(odd){padding-right:48px}
.caps .cap:nth-child(even){padding-left:48px;border-left:1px solid var(--rule)}
@media(max-width:820px){.caps .cap:nth-child(even){padding-left:0;border-left:none}}
.cap::before{content:'';position:absolute;left:0;top:-1px;height:1px;width:0;background:var(--accent);transition:width .6s var(--ease)}
.cap:hover::before{width:100%}
.cap .num{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--accent);letter-spacing:.15em;display:block;margin-bottom:14px}
.cap h3{font-size:20px;font-weight:600;letter-spacing:-.01em;margin-bottom:10px}
.cap p{font-size:15px;color:var(--ink-60);line-height:1.6}

/* ---------- architecture ---------- */
.arch{background:#fff;border:1px solid var(--rule);border-radius:14px;padding:28px 20px;overflow:hidden}
.arch svg{width:100%;height:auto;display:block}
.wire{fill:none;stroke-width:1.5;stroke-dasharray:4 8;animation:flow 1.6s linear infinite}
@keyframes flow{to{stroke-dashoffset:-24}}
.nodeCircle{transition:transform .3s var(--ease);transform-origin:center}
.node:hover .nodeCircle{transform:scale(1.14)}
.halo{animation:breathe 3.4s ease-in-out infinite;transform-origin:center}
.hb{animation-delay:.5s}.hc{animation-delay:1s}.hd{animation-delay:1.5s}
@keyframes breathe{0%,100%{opacity:.10}50%{opacity:.26}}

/* ---------- work ---------- */
.work-item{border-top:1px solid var(--rule);padding:34px 0;display:grid;
  grid-template-columns:60px 1fr 300px;gap:30px;align-items:start;
  transition:background .4s var(--ease),padding-left .4s var(--ease)}
@media(max-width:900px){.work-item{grid-template-columns:44px 1fr;gap:18px}}
.work-item:hover{background:var(--paper-2);padding-left:16px}
.work-item:last-child{border-bottom:1px solid var(--rule)}
.work-item .idx{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--ink-35);padding-top:6px}
.work-item h3{font-family:'Instrument Serif',Georgia,serif;font-size:29px;font-weight:400;letter-spacing:-.01em;line-height:1.2;margin-bottom:8px}
.work-item p{font-size:15px;color:var(--ink-60);max-width:620px}
.chips{display:flex;flex-wrap:wrap;gap:6px;padding-top:6px}
@media(max-width:900px){.chips{grid-column:2}}
.chip{font-family:'JetBrains Mono',monospace;font-size:10.5px;color:var(--ink-60);
  border:1px solid var(--rule);border-radius:100px;padding:3px 10px;background:#fff;white-space:nowrap}

/* ---------- stack ---------- */
.stack-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--rule);border:1px solid var(--rule)}
@media(max-width:900px){.stack-grid{grid-template-columns:1fr}}
.stack-cell{background:var(--paper);padding:30px 26px;transition:background .35s}
.stack-cell:hover{background:#fff}
.stack-cell h4{font-family:'JetBrains Mono',monospace;font-size:11px;letter-spacing:.18em;
  text-transform:uppercase;color:var(--accent);margin-bottom:18px}
.stack-cell ul{list-style:none;display:flex;flex-wrap:wrap;gap:7px}
.stack-cell li{font-size:13.5px;color:var(--ink-60);border-bottom:1px solid transparent;
  transition:color .22s,border-color .22s;cursor:default}
.stack-cell li:hover{color:var(--ink);border-color:var(--accent)}
.stack-cell li:not(:last-child)::after{content:'·';color:var(--ink-35);margin-left:7px}

/* ---------- quote ---------- */
.quote{border-left:2px solid var(--accent);padding:6px 0 6px 26px;
  font-family:'Instrument Serif',Georgia,serif;font-size:clamp(20px,2.6vw,30px);
  line-height:1.35;font-style:italic;color:var(--ink);max-width:800px}

/* ---------- contact ---------- */
#contact{background:var(--ink);color:var(--paper);padding:130px 0 70px}
#contact .eyebrow{color:rgba(251,251,249,.4)}
#contact .eyebrow::after{background:rgba(251,251,249,.16)}
#contact h2{font-family:'Instrument Serif',Georgia,serif;font-weight:400;
  font-size:clamp(42px,8vw,110px);line-height:.94;letter-spacing:-.03em;margin-bottom:44px}
#contact h2 em{font-style:italic;color:var(--accent)}
.contact-links{display:flex;flex-wrap:wrap;gap:14px;margin-bottom:80px}
.clink{display:inline-flex;align-items:center;gap:11px;text-decoration:none;color:var(--paper);
  border:1px solid rgba(251,251,249,.22);border-radius:100px;padding:13px 26px;font-size:14.5px;
  position:relative;overflow:hidden;transition:color .35s var(--ease),border-color .35s}
.clink span{position:relative;z-index:1}
.clink::before{content:'';position:absolute;inset:0;background:var(--paper);
  transform:translateY(101%);transition:transform .45s var(--ease)}
.clink:hover{color:var(--ink);border-color:var(--paper)}
.clink:hover::before{transform:translateY(0)}
.foot{border-top:1px solid rgba(251,251,249,.14);padding-top:26px;display:flex;
  justify-content:space-between;flex-wrap:wrap;gap:12px;
  font-family:'JetBrains Mono',monospace;font-size:11px;color:rgba(251,251,249,.42)}
</style>
</head>
<body>

<div id="progress"></div>
<div id="glow"></div>

<nav id="nav">
  <div class="nav-in">
    <a href="#hero" class="logo">hassan<span>.</span>ali</a>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#system">System</a>
      <a href="#work">Work</a>
      <a href="#stack">Stack</a>
      <a href="#contact" class="pill">Get in touch</a>
    </div>
  </div>
</nav>

<!-- ============ HERO ============ -->
<section id="hero">
  <div class="wrap">
    <div class="status"><span class="dot"></span> Open to full-stack roles</div>

    <h1 class="hero-name">
      <span class="ln"><span>Hassan</span></span>
      <span class="ln"><span><i>Ali</i></span></span>
    </h1>

    <div class="hero-grid">
      <div>
        <p class="lead">
          Full-stack engineer who owns features <b>from the database to production</b>.
          I don't hand off at the API boundary — I write the schema, build the services,
          ship the frontend, then deploy and operate it on AWS behind Nginx.
        </p>
        <br>
        <div class="rotator">
          <ul>
            <li>&gt; typescript · ruby · python · php</li>
            <li>&gt; rails · nestjs · next.js · laravel · flask</li>
            <li>&gt; postgres · redis · sidekiq · prisma</li>
            <li>&gt; aws ec2 · nginx · ubuntu · s3</li>
          </ul>
        </div>
      </div>
      <div class="hero-meta">
        <div><span>Role</span><b>Full-Stack Engineer</b></div>
        <div><span>Languages</span><b>4 in production</b></div>
        <div><span>Scope</span><b>Schema → on-call</b></div>
        <div><span>Infra</span><b>Self-operated</b></div>
      </div>
    </div>
  </div>
</section>

<div class="marquee">
  <div class="marquee-track">
    <span>TypeScript</span><span>Ruby on Rails</span><span>Next.js</span><span>NestJS</span><span>Python</span><span>PostgreSQL</span><span>Redis</span><span>AWS</span><span>React Native</span><span>Laravel</span><span>Nginx</span><span>Sidekiq</span><span>Prisma</span><span>WebSockets</span><span>OpenAI</span><span>Stripe</span>
    <span>TypeScript</span><span>Ruby on Rails</span><span>Next.js</span><span>NestJS</span><span>Python</span><span>PostgreSQL</span><span>Redis</span><span>AWS</span><span>React Native</span><span>Laravel</span><span>Nginx</span><span>Sidekiq</span><span>Prisma</span><span>WebSockets</span><span>OpenAI</span><span>Stripe</span>
  </div>
</div>

<!-- ============ ABOUT ============ -->
<section id="about" class="reveal">
  <div class="wrap">
    <div class="eyebrow">01 — About</div>
    <h2 class="display rv">I build across stacks, and I <em>run what I build.</em></h2>
    <p class="lead rv" style="max-width:760px;margin-bottom:64px">
      Realtime microservice architectures, e-commerce platforms, POS systems, AI services.
      Four languages in production, picked per service rather than forced across all of them.
    </p>

    <div class="caps">
      <div class="cap rv">
        <span class="num">/ 01</span>
        <h3>Microservice architecture</h3>
        <p>A Rails API, NestJS services, a Python AI service, and a Next.js frontend — wired together over WebSockets and ActionCable so state moves live instead of on refresh.</p>
      </div>
      <div class="cap rv">
        <span class="num">/ 02</span>
        <h3>Security &amp; compliance</h3>
        <p>Role-based access control, JWT auth, rate limiting, and field-level encryption for sensitive data at rest. HIPAA-style PHI handling — written for audit, not for the demo.</p>
      </div>
      <div class="cap rv">
        <span class="num">/ 03</span>
        <h3>Infrastructure I operate</h3>
        <p>Next.js, NestJS and Rails apps deployed to AWS EC2 behind an Nginx reverse proxy on Ubuntu Linux, with Redis and background job queues. No throwing it over the wall.</p>
      </div>
      <div class="cap rv">
        <span class="num">/ 04</span>
        <h3>Commerce &amp; mobile</h3>
        <p>Deep work in e-commerce, POS, ERP and CMS products — including offline-first POS on IndexedDB and headless CMS builds. Cross-platform mobile with React Native.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ SYSTEM ============ -->
<section id="system" class="reveal">
  <div class="wrap">
    <div class="eyebrow">02 — The system</div>
    <h2 class="display rv">One platform, <em>four runtimes.</em></h2>
    <p class="lead rv" style="max-width:700px;margin-bottom:48px">
      This is the shape of the realtime platform I architect and maintain. Traffic is live.
    </p>

    <div class="arch rv">
      <svg viewBox="0 0 1000 380" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <path id="p1" d="M190 90 C 330 90, 380 190, 470 190"/>
          <path id="p2" d="M810 90 C 670 90, 620 190, 530 190"/>
          <path id="p3" d="M190 292 C 330 292, 380 190, 470 190"/>
          <path id="p4" d="M810 292 C 670 292, 620 190, 530 190"/>
        </defs>

        <use href="#p1" class="wire" stroke="#D6432B"/>
        <use href="#p2" class="wire" stroke="#1D4ED8"/>
        <use href="#p3" class="wire" stroke="#7C3AED"/>
        <use href="#p4" class="wire" stroke="#16A34A"/>

        <circle r="3.5" fill="#D6432B"><animateMotion dur="2.2s" repeatCount="indefinite"><mpath href="#p1"/></animateMotion></circle>
        <circle r="3.5" fill="#1D4ED8"><animateMotion dur="2.7s" begin=".6s" repeatCount="indefinite"><mpath href="#p2"/></animateMotion></circle>
        <circle r="3.5" fill="#7C3AED"><animateMotion dur="2s" begin="1s" repeatCount="indefinite"><mpath href="#p3"/></animateMotion></circle>
        <circle r="3.5" fill="#16A34A"><animateMotion dur="2.5s" begin="1.4s" repeatCount="indefinite"><mpath href="#p4"/></animateMotion></circle>

        <g class="node">
          <circle cx="190" cy="90" r="34" fill="#D6432B" class="halo"/>
          <circle cx="190" cy="90" r="24" fill="#fff" stroke="#D6432B" stroke-width="1.6" class="nodeCircle"/>
          <text x="190" y="95" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="11" fill="#D6432B">RB</text>
          <text x="190" y="136" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="10.5" fill="#5A5A5E">RAILS 7 API</text>
        </g>
        <g class="node">
          <circle cx="810" cy="90" r="34" fill="#1D4ED8" class="halo hb"/>
          <circle cx="810" cy="90" r="24" fill="#fff" stroke="#1D4ED8" stroke-width="1.6" class="nodeCircle"/>
          <text x="810" y="95" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="11" fill="#1D4ED8">TS</text>
          <text x="810" y="136" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="10.5" fill="#5A5A5E">NESTJS SERVICES</text>
        </g>
        <g class="node">
          <circle cx="190" cy="292" r="34" fill="#7C3AED" class="halo hc"/>
          <circle cx="190" cy="292" r="24" fill="#fff" stroke="#7C3AED" stroke-width="1.6" class="nodeCircle"/>
          <text x="190" y="297" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="11" fill="#7C3AED">PY</text>
          <text x="190" y="338" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="10.5" fill="#5A5A5E">AI MICROSERVICE</text>
        </g>
        <g class="node">
          <circle cx="810" cy="292" r="34" fill="#16A34A" class="halo hd"/>
          <circle cx="810" cy="292" r="24" fill="#fff" stroke="#16A34A" stroke-width="1.6" class="nodeCircle"/>
          <text x="810" y="297" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="11" fill="#16A34A">NX</text>
          <text x="810" y="338" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="10.5" fill="#5A5A5E">NEXT.JS / REACT 19</text>
        </g>

        <rect x="455" y="166" width="90" height="48" rx="10" fill="#fff" stroke="#0B0B0C" stroke-width="1.6"/>
        <text x="500" y="196" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="11" fill="#0B0B0C">WS / ⚡</text>
        <text x="500" y="238" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="10.5" fill="#5A5A5E">REALTIME BUS · REDIS · SIDEKIQ</text>
      </svg>
    </div>
  </div>
</section>

<!-- ============ WORK ============ -->
<section id="work" class="reveal">
  <div class="wrap">
    <div class="eyebrow">03 — Selected work</div>
    <h2 class="display rv">Described by <em>capability,</em> not by name.</h2>
    <p class="lead rv" style="max-width:700px;margin-bottom:54px">
      Most recent work lives in private team and client repositories. Happy to walk through
      architecture, code and decisions on request.
    </p>

    <div class="rv">
      <div class="work-item">
        <div class="idx">001</div>
        <div>
          <h3>Realtime microservices platform</h3>
          <p>Multi-service system combining a Rails 7 API, NestJS services, a Python AI microservice and a Next.js / React 19 frontend, connected over WebSockets and ActionCable for live updates. RBAC, background job processing, rate limiting, and field-level encryption of sensitive data at rest.</p>
        </div>
        <div class="chips"><span class="chip">Rails 7</span><span class="chip">NestJS</span><span class="chip">Python</span><span class="chip">React 19</span><span class="chip">Sidekiq</span><span class="chip">ActionCable</span></div>
      </div>

      <div class="work-item">
        <div class="idx">002</div>
        <div>
          <h3>Offline-first Point of Sale</h3>
          <p>Full POS on Laravel + Inertia + React with IndexedDB sync, barcode scanning, thermal-print support and sales analytics. Keeps taking payments when the connection drops, then reconciles.</p>
        </div>
        <div class="chips"><span class="chip">Laravel</span><span class="chip">Inertia</span><span class="chip">React</span><span class="chip">IndexedDB</span></div>
      </div>

      <div class="work-item">
        <div class="idx">003</div>
        <div>
          <h3>E-commerce platforms</h3>
          <p>Production storefronts on Next.js 16 + Prisma + PostgreSQL with NextAuth, plus React + Express + Prisma builds. Checkout, catalog, auth and admin owned end to end.</p>
        </div>
        <div class="chips"><span class="chip">Next.js 16</span><span class="chip">Prisma</span><span class="chip">PostgreSQL</span><span class="chip">NextAuth</span><span class="chip">Stripe</span></div>
      </div>

      <div class="work-item">
        <div class="idx">004</div>
        <div>
          <h3>AI-powered applications</h3>
          <p>Chat and automation products integrating the OpenAI API into Next.js and Flask services — streaming responses, queued jobs, and rate-limited endpoints.</p>
        </div>
        <div class="chips"><span class="chip">OpenAI API</span><span class="chip">Next.js</span><span class="chip">Flask</span></div>
      </div>

      <div class="work-item">
        <div class="idx">005</div>
        <div>
          <h3>Headless CMS &amp; business systems</h3>
          <p>Content platforms on Laravel 12 + Livewire, plus ERP, accounting and internal admin tooling. The unglamorous systems that a business actually runs on.</p>
        </div>
        <div class="chips"><span class="chip">Laravel 12</span><span class="chip">Livewire</span><span class="chip">MySQL</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ STACK ============ -->
<section id="stack" class="reveal">
  <div class="wrap">
    <div class="eyebrow">04 — The stack</div>
    <h2 class="display rv">Right tool per service. <em>Not one forced everywhere.</em></h2>
    <div style="height:44px"></div>

    <div class="stack-grid rv">
      <div class="stack-cell"><h4>Languages</h4><ul><li>TypeScript</li><li>JavaScript</li><li>Ruby</li><li>Python</li><li>PHP</li></ul></div>
      <div class="stack-cell"><h4>Frontend</h4><ul><li>Next.js</li><li>React</li><li>React Native</li><li>Vite</li><li>Tailwind</li><li>Zustand</li><li>Inertia</li><li>Livewire</li></ul></div>
      <div class="stack-cell"><h4>Backend</h4><ul><li>NestJS</li><li>Node.js</li><li>Rails</li><li>Laravel</li><li>Flask</li><li>Express</li></ul></div>
      <div class="stack-cell"><h4>Data &amp; messaging</h4><ul><li>PostgreSQL</li><li>MongoDB</li><li>Redis</li><li>Sidekiq</li><li>Prisma</li></ul></div>
      <div class="stack-cell"><h4>Realtime &amp; AI</h4><ul><li>WebSockets</li><li>Socket.IO</li><li>ActionCable</li><li>OpenAI API</li><li>Firebase</li><li>Stripe</li></ul></div>
      <div class="stack-cell"><h4>Cloud &amp; infra</h4><ul><li>AWS EC2</li><li>AWS S3</li><li>Nginx</li><li>Ubuntu</li><li>Linux</li><li>Git</li></ul></div>
    </div>

    <div style="height:70px"></div>
    <div class="quote rv">
      RBAC · JWT auth · rate limiting · field-level encryption · background jobs · offline-first.
      Practices, not buzzwords — each one shipped in something that has users.
    </div>
  </div>
</section>

<!-- ============ CONTACT ============ -->
<section id="contact" class="reveal">
  <div class="wrap">
    <div class="eyebrow">05 — Get in touch</div>
    <h2 class="rv">Let's build<br>something that <em>runs.</em></h2>
    <div class="contact-links rv">
      <a class="clink" href="mailto:hassanali.naeem9811@gmail.com"><span>hassanali.naeem9811@gmail.com</span></a>
      <a class="clink" href="https://caffstack.com"><span>caffstack.com ↗</span></a>
    </div>
    <div class="foot">
      <span>© 2026 Hassan Ali</span>
      <span>Open to full-stack roles — build the product, run the infrastructure.</span>
    </div>
  </div>
</section>

<script>
// scroll progress
const bar = document.getElementById('progress');
const nav = document.getElementById('nav');
addEventListener('scroll', () => {
  const h = document.documentElement.scrollHeight - innerHeight;
  bar.style.width = (scrollY / h) * 100 + '%';
  nav.classList.toggle('stuck', scrollY > 40);
}, {passive:true});

// reveal on scroll
const io = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in-view'); io.unobserve(e.target); } });
}, {threshold:0.12, rootMargin:'0px 0px -60px 0px'});
document.querySelectorAll('.reveal, .work-item').forEach(el => io.observe(el));

// cursor glow
const glow = document.getElementById('glow');
addEventListener('mousemove', e => {
  glow.style.opacity = 1;
  glow.style.left = e.clientX + 'px';
  glow.style.top = e.clientY + 'px';
}, {passive:true});
</script>
</body>
</html>
