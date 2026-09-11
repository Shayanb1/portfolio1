---
layout: post 
title: Portfolio Home 
hide: true
show_reading_time: false
---

<style>
/* ── Reset for this page's content area ── */
.post-content { overflow: visible; }

/* ── HERO ── */
.hero {
  position: relative;
  padding: 3rem 0 2.5rem;
  text-align: center;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 80% 60% at 50% 0%, rgba(74,222,128,.10) 0%, transparent 70%),
    radial-gradient(ellipse 50% 40% at 80% 100%, rgba(34,211,238,.08) 0%, transparent 60%);
  pointer-events: none;
}

.hero-greeting {
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  font-size: .82rem;
  color: #4ade80;
  letter-spacing: .15em;
  text-transform: uppercase;
  margin-bottom: .6rem;
}

.hero-name {
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  font-size: clamp(2rem, 6vw, 3.6rem);
  font-weight: 800;
  line-height: 1.1;
  background: linear-gradient(135deg, #4ade80 0%, #22d3ee 45%, #818cf8 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0 0 .5rem;
}

.hero-sub {
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  font-size: .9rem;
  color: #8b949e;
  margin-bottom: 1.4rem;
}

.hero-sub .accent { color: #22d3ee; }

.hero-tags {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
  margin-bottom: 2rem;
}

.hero-tag {
  padding: 4px 12px;
  border-radius: 999px;
  font-family: monospace;
  font-size: .75rem;
  letter-spacing: .05em;
  border: 1px solid;
}
.hero-tag.green  { border-color: #4ade80; color: #4ade80; background: rgba(74,222,128,.08); }
.hero-tag.cyan   { border-color: #22d3ee; color: #22d3ee; background: rgba(34,211,238,.08); }
.hero-tag.purple { border-color: #a78bfa; color: #a78bfa; background: rgba(167,139,250,.08); }

/* ── TERMINAL BLOCK ── */
.term-card {
  background: #0d1117;
  border: 1px solid #21262d;
  border-radius: 12px;
  overflow: hidden;
  margin: 0 auto 2.5rem;
  max-width: 680px;
  box-shadow: 0 0 0 1px #30363d, 0 8px 32px rgba(0,0,0,.6), 0 0 48px rgba(74,222,128,.06);
}

.term-titlebar {
  background: #161b22;
  padding: 10px 16px;
  display: flex;
  align-items: center;
  gap: 6px;
  border-bottom: 1px solid #21262d;
}

.dot { width: 12px; height: 12px; border-radius: 50%; }
.dot.r { background: #ff5f57; }
.dot.y { background: #febc2e; }
.dot.g { background: #28c840; }
.term-fname { font-family: monospace; font-size: .72rem; color: #484f58; margin-left: 8px; }

.term-body {
  padding: 18px 22px;
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  font-size: .86rem;
  line-height: 2;
}

.t-prompt { color: #4ade80; }
.t-cmd    { color: #22d3ee; }
.t-arg    { color: #e6edf3; }
.t-out    { color: #8b949e; padding-left: 1.4rem; }
.t-str    { color: #f97316; }
.t-comment{ color: #484f58; }

.cursor {
  display: inline-block;
  width: 8px; height: 1em;
  background: #4ade80;
  vertical-align: text-bottom;
  animation: blink 1s step-end infinite;
}
@keyframes blink { 50% { opacity: 0; } }

/* ── SECTION HEADERS ── */
.sec-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin: 2.5rem 0 1.2rem;
}

.sec-header::after {
  content: '';
  flex: 1;
  height: 1px;
  background: linear-gradient(90deg, #21262d, transparent);
}

.sec-label {
  font-family: monospace;
  font-size: .78rem;
  letter-spacing: .12em;
  text-transform: uppercase;
  color: #4ade80;
}

.sec-num {
  font-family: monospace;
  font-size: .7rem;
  color: #484f58;
}

/* ── DEVENV BUTTONS ── */
.devenv-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-bottom: .5rem;
}

.dev-btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 12px 20px;
  border-radius: 8px;
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  font-size: .84rem;
  font-weight: 600;
  text-decoration: none;
  border: 1px solid transparent;
  transition: transform .18s, box-shadow .18s, border-color .18s;
  position: relative;
  overflow: hidden;
}

.dev-btn::before {
  content: '';
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity .18s;
}

.dev-btn:hover { transform: translateY(-2px); text-decoration: none; }
.dev-btn:hover::before { opacity: 1; }

.dev-btn .prefix {
  font-family: monospace;
  font-size: .7rem;
  opacity: .6;
}

.btn-ocs {
  background: linear-gradient(135deg, #1a1a2e, #16213e);
  border-color: #FA8072;
  color: #FA8072;
  box-shadow: 0 0 0 0 rgba(250,128,114,0);
}
.btn-ocs:hover {
  border-color: #FA8072;
  box-shadow: 0 4px 20px rgba(250,128,114,.3), 0 0 0 1px rgba(250,128,114,.2);
  color: #FA8072;
}

.btn-gh {
  background: linear-gradient(135deg, #161b22, #0d1117);
  border-color: #30363d;
  color: #e6edf3;
  box-shadow: 0 0 0 0 rgba(255,255,255,0);
}
.btn-gh:hover {
  border-color: #58a6ff;
  box-shadow: 0 4px 20px rgba(88,166,255,.25), 0 0 0 1px rgba(88,166,255,.15);
  color: #58a6ff;
}

.btn-vscode {
  background: linear-gradient(135deg, #001d3d, #003566);
  border-color: #007ACC;
  color: #4fc3f7;
  box-shadow: 0 0 0 0 rgba(0,122,204,0);
}
.btn-vscode:hover {
  box-shadow: 0 4px 20px rgba(0,122,204,.35), 0 0 0 1px rgba(79,195,247,.2);
  color: #4fc3f7;
}

/* ── LESSON CARDS ── */
.lesson-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 12px;
  margin-bottom: .5rem;
}

.lesson-card {
  display: flex;
  flex-direction: column;
  padding: 16px;
  border-radius: 10px;
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  text-decoration: none;
  border: 1px solid transparent;
  transition: transform .2s, box-shadow .2s;
  position: relative;
  overflow: hidden;
}

.lesson-card::after {
  content: '→';
  position: absolute;
  bottom: 12px;
  right: 14px;
  font-size: .9rem;
  opacity: 0;
  transform: translateX(-6px);
  transition: opacity .2s, transform .2s;
}

.lesson-card:hover { transform: translateY(-3px); text-decoration: none; }
.lesson-card:hover::after { opacity: 1; transform: translateX(0); }

.lc-tag {
  font-size: .65rem;
  letter-spacing: .1em;
  text-transform: uppercase;
  margin-bottom: 6px;
  opacity: .7;
}

.lc-name {
  font-size: .9rem;
  font-weight: 700;
}

.lc-js {
  background: linear-gradient(135deg, #1a2a1a, #0d1117);
  border-color: #4ade80;
  color: #4ade80;
  box-shadow: inset 0 0 20px rgba(74,222,128,.05);
}
.lc-js:hover { box-shadow: 0 6px 24px rgba(74,222,128,.2), inset 0 0 20px rgba(74,222,128,.08); color: #4ade80; }

.lc-var {
  background: linear-gradient(135deg, #1a1a2e, #0d1117);
  border-color: #818cf8;
  color: #818cf8;
  box-shadow: inset 0 0 20px rgba(129,140,248,.05);
}
.lc-var:hover { box-shadow: 0 6px 24px rgba(129,140,248,.2), inset 0 0 20px rgba(129,140,248,.08); color: #818cf8; }

.lc-game {
  background: linear-gradient(135deg, #2a1a0d, #0d1117);
  border-color: #f97316;
  color: #f97316;
  box-shadow: inset 0 0 20px rgba(249,115,22,.05);
}
.lc-game:hover { box-shadow: 0 6px 24px rgba(249,115,22,.2), inset 0 0 20px rgba(249,115,22,.08); color: #f97316; }

.lc-net {
  background: linear-gradient(135deg, #0d1a2a, #0d1117);
  border-color: #22d3ee;
  color: #22d3ee;
  box-shadow: inset 0 0 20px rgba(34,211,238,.05);
}
.lc-net:hover { box-shadow: 0 6px 24px rgba(34,211,238,.2), inset 0 0 20px rgba(34,211,238,.08); color: #22d3ee; }

/* ── PROGRESS CARDS ── */
.prog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 10px;
  margin-bottom: .5rem;
}

.prog-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 14px 16px;
  border-radius: 8px;
  background: #0d1117;
  border: 1px solid #21262d;
  font-family: monospace;
  font-size: .88rem;
  font-weight: 700;
  text-decoration: none;
  color: #e6edf3;
  transition: border-color .2s, box-shadow .2s, transform .2s;
}

.prog-card:hover {
  transform: translateY(-2px);
  text-decoration: none;
}

.prog-card .pc-arrow {
  opacity: 0;
  font-size: .8rem;
  transition: opacity .2s, transform .2s;
  transform: translateX(-4px);
}

.prog-card:hover .pc-arrow { opacity: 1; transform: translateX(0); }

.pc-snake:hover  { border-color: #4ade80; box-shadow: 0 4px 16px rgba(74,222,128,.2); color: #4ade80; }
.pc-fish:hover   { border-color: #22d3ee; box-shadow: 0 4px 16px rgba(34,211,238,.2); color: #22d3ee; }
.pc-gamify:hover { border-color: #f97316; box-shadow: 0 4px 16px rgba(249,115,22,.2); color: #f97316; }
.pc-cs:hover     { border-color: #a78bfa; box-shadow: 0 4px 16px rgba(167,139,250,.2); color: #a78bfa; }
</style>

<!-- ═══════════════ HERO ═══════════════ -->
<div class="hero">
  <p class="hero-greeting">// welcome to my portfolio</p>
  <h1 class="hero-name">Shayan Bhatti</h1>
  <p class="hero-sub">
    11th grade · <span class="accent">aspiring AI engineer</span>
  </p>
  <div class="hero-tags">
    <span class="hero-tag green">11th Grade</span>
    <span class="hero-tag cyan">AI Research</span>
    <span class="hero-tag purple">Full-Stack Dev</span>
  </div>
</div>

<!-- ═══════════════ TERMINAL BIO ═══════════════ -->
<div class="term-card">
  <div class="term-titlebar">
    <span class="dot r"></span>
    <span class="dot y"></span>
    <span class="dot g"></span>
    <span class="term-fname">~/portfolio — bash</span>
  </div>
  <div class="term-body">
    <div><span class="t-prompt">$</span> <span class="t-cmd">whoami</span></div>
    <div class="t-out"><span class="t-str">shayan_bhatti</span> <span class="t-comment">// 11th grade, Del Norte HS</span></div>
    <div style="margin-top:6px"><span class="t-prompt">$</span> <span class="t-cmd">cat</span> <span class="t-arg">mission.txt</span></div>
    <div class="t-out">I want to develop AI and push it past its current limits.</div>
    <div class="t-out">Not just use it — <span style="color:#4ade80">build it, break it, and rebuild it better.</span></div>
    <div style="margin-top:6px"><span class="t-prompt">$</span> <span class="t-cmd">ls</span> <span class="t-arg">./skills/</span></div>
    <div class="t-out"><span style="color:#22d3ee">python/</span>  <span style="color:#4ade80">javascript/</span>  <span style="color:#818cf8">machine-learning/</span>  <span style="color:#f97316">web-dev/</span></div>
    <div style="margin-top:6px"><span class="t-prompt">$</span> <span class="cursor"></span></div>
  </div>
</div>

<!-- ═══════════════ DEV ENV ═══════════════ -->
<div class="sec-header">
  <span class="sec-num">01</span>
  <span class="sec-label">Development Environment</span>
</div>

<div class="devenv-grid">
  <a href="https://opencodingsociety.com" class="dev-btn btn-ocs">
    <img src="{{ '/favicon.ico' | relative_url }}" style="width:16px;height:16px;" alt="">
    <span>OCS</span>
    <span class="prefix">↗</span>
  </a>
  <a href="https://github.com/Open-Coding-Society/portfolio" class="dev-btn btn-gh">
    <svg style="width:16px;height:16px;fill:currentColor;flex-shrink:0" viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
    <span>GitHub</span>
    <span class="prefix">↗</span>
  </a>
  <a href="https://vscode.dev/" class="dev-btn btn-vscode">
    <svg style="width:16px;height:16px;fill:#4fc3f7;flex-shrink:0" viewBox="0 0 16 16"><path d="M11.34 0L5.66 5.39l-2.4-1.8L1.19 4.82v6.36l2.07 1.23 2.4-1.8L11.34 16 15 14.23V1.77L11.34 0zm.59 11.57l-3.86-3.54 3.86-3.54v7.08z"/></svg>
    <span>VSCode.dev</span>
    <span class="prefix">↗</span>
  </a>
</div>

<!-- ═══════════════ LESSONS ═══════════════ -->
<div class="sec-header">
  <span class="sec-num">02</span>
  <span class="sec-label">My Lessons</span>
</div>

<div class="lesson-grid">
  <a href="{{site.baseurl}}/code/javascript" class="lesson-card lc-js">
    <span class="lc-tag">lang</span>
    <span class="lc-name">JS Basics</span>
  </a>
  <a href="{{site.baseurl}}/game/essentials/variables" class="lesson-card lc-var">
    <span class="lc-tag">lang</span>
    <span class="lc-name">JS Variables</span>
  </a>
  <a href="{{site.baseurl}}/gamerunner" class="lesson-card lc-game">
    <span class="lc-tag">project</span>
    <span class="lc-name">Gamerunner</span>
  </a>
  <a href="{{site.baseurl}}/network/stack" class="lesson-card lc-net">
    <span class="lc-tag">systems</span>
    <span class="lc-name">Networking</span>
  </a>
</div>

<!-- ═══════════════ CLASS PROGRESS ═══════════════ -->
<div class="sec-header">
  <span class="sec-num">03</span>
  <span class="sec-label">Class Progress</span>
</div>

<div class="prog-grid">
  <a href="{{site.baseurl}}/snake" class="prog-card pc-snake">
    <span>Snake</span><span class="pc-arrow">→</span>
  </a>
  <a href="{{site.baseurl}}/gamify/parallax" class="prog-card pc-fish">
    <span>Fish</span><span class="pc-arrow">→</span>
  </a>
  <a href="{{site.baseurl}}/gamify" class="prog-card pc-gamify">
    <span>Gamify</span><span class="pc-arrow">→</span>
  </a>
  <a href="{{site.baseurl}}/cs-pathway" class="prog-card pc-cs">
    <span>CS Pathway</span><span class="pc-arrow">→</span>
  </a>
</div>
