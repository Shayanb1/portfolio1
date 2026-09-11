---
layout: post 
title: Portfolio Home 
hide: true
show_reading_time: false
---

<style>
  :root {
    --term-green: #4ade80;
    --term-cyan: #22d3ee;
    --term-bg: #0d1117;
    --term-border: #30363d;
    --term-muted: #8b949e;
  }

  .term-box {
    background: var(--term-bg);
    border: 1px solid var(--term-border);
    border-radius: 8px;
    padding: 24px 28px;
    font-family: 'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
    margin-bottom: 2rem;
  }

  .term-bar {
    display: flex;
    align-items: center;
    gap: 6px;
    margin-bottom: 16px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--term-border);
  }

  .term-dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
  }
  .term-dot.red   { background: #ff5f57; }
  .term-dot.yellow{ background: #febc2e; }
  .term-dot.green { background: #28c840; }

  .term-title-text {
    font-family: monospace;
    font-size: 0.75rem;
    color: var(--term-muted);
    margin-left: 8px;
  }

  .term-prompt {
    color: var(--term-green);
    font-weight: 700;
    margin-right: 8px;
  }

  .term-line {
    display: flex;
    align-items: baseline;
    gap: 6px;
    line-height: 1.9;
    font-family: monospace;
    font-size: 0.95rem;
  }

  .term-cmd { color: var(--term-cyan); }
  .term-str { color: #f97316; }
  .term-muted-txt { color: var(--term-muted); }

  .cursor {
    display: inline-block;
    width: 8px;
    height: 1em;
    background: var(--term-green);
    vertical-align: text-bottom;
    animation: blink 1s step-end infinite;
  }
  @keyframes blink { 50% { opacity: 0; } }

  .section-label {
    font-family: monospace;
    font-size: 0.8rem;
    color: var(--term-muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 0.4rem;
    display: block;
  }

  .section-heading {
    font-family: monospace;
    font-size: 1rem;
    color: var(--term-green);
    margin: 0 0 0.25rem 0;
  }

  .section-desc {
    font-family: monospace;
    font-size: 0.82rem;
    color: var(--term-muted);
    margin-bottom: 1rem;
  }

  .link-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 2rem;
  }

  .code-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 16px;
    background: #161b22;
    border: 1px solid var(--term-border);
    border-radius: 6px;
    font-family: monospace;
    font-size: 0.85rem;
    color: #e6edf3;
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s, background 0.2s;
  }

  .code-btn::before {
    content: '$';
    color: var(--term-green);
    font-weight: 700;
  }

  .code-btn:hover {
    border-color: var(--term-green);
    color: var(--term-green);
    background: #0d1117;
    text-decoration: none;
  }

  .code-btn .btn-icon {
    opacity: 0.6;
    font-size: 0.8rem;
  }

  .tag-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 7px 14px;
    background: #161b22;
    border: 1px solid var(--term-border);
    border-radius: 4px;
    font-family: monospace;
    font-size: 0.82rem;
    color: var(--term-cyan);
    text-decoration: none;
    transition: border-color 0.2s, background 0.2s;
  }

  .tag-btn::before {
    content: '#';
    color: var(--term-muted);
  }

  .tag-btn:hover {
    border-color: var(--term-cyan);
    background: #0d1117;
    text-decoration: none;
  }

  .divider {
    border: none;
    border-top: 1px solid var(--term-border);
    margin: 1.8rem 0;
  }
</style>

<div class="term-box">
  <div class="term-bar">
    <span class="term-dot red"></span>
    <span class="term-dot yellow"></span>
    <span class="term-dot green"></span>
    <span class="term-title-text">portfolio — zsh</span>
  </div>
  <div class="term-line">
    <span class="term-prompt">~$</span>
    <span class="term-cmd">whoami</span>
  </div>
  <div class="term-line" style="margin-left: 1.6rem;">
    <span class="term-str">Shayan Bhatti</span>
  </div>
  <div class="term-line" style="margin-top: 8px;">
    <span class="term-prompt">~$</span>
    <span class="term-cmd">cat</span>
    <span style="color: #e6edf3;">about.txt</span>
  </div>
  <div class="term-line" style="margin-left: 1.6rem;">
    <span class="term-muted-txt">// student developer · CS enthusiast · builder of things</span>
  </div>
  <div class="term-line" style="margin-top: 8px;">
    <span class="term-prompt">~$</span>
    <span class="cursor"></span>
  </div>
</div>

<hr class="divider">

<span class="section-label">// dev environment</span>
<p class="section-desc">&gt; Tools and workflows — click to explore.</p>

<div class="link-grid">
  <a href="https://opencodingsociety.com" class="code-btn">
    <span class="btn-icon">🔗</span> open-coding-society
  </a>
  <a href="https://github.com/Open-Coding-Society/portfolio" class="code-btn">
    <span class="btn-icon">
      <svg style="width:14px;height:14px;fill:currentColor;vertical-align:middle" viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
    </span> github/portfolio
  </a>
  <a href="https://vscode.dev/" class="code-btn">
    <span class="btn-icon">
      <svg style="width:14px;height:14px;fill:#007ACC;vertical-align:middle" viewBox="0 0 16 16"><path d="M11.34 0L5.66 5.39l-2.4-1.8L1.19 4.82v6.36l2.07 1.23 2.4-1.8L11.34 16 15 14.23V1.77L11.34 0zm.59 11.57l-3.86-3.54 3.86-3.54v7.08z"/></svg>
    </span> vscode.dev
  </a>
</div>

<hr class="divider">

<span class="section-label">// lessons</span>
<p class="section-desc">&gt; Foundational topics I've built and documented.</p>

<div class="link-grid">
  <a href="{{site.baseurl}}/code/javascript" class="tag-btn">js-basics</a>
  <a href="{{site.baseurl}}/game/essentials/variables" class="tag-btn">js-variables</a>
  <a href="{{site.baseurl}}/gamerunner" class="tag-btn">gamerunner</a>
  <a href="{{site.baseurl}}/network/stack" class="tag-btn">networking</a>
</div>

<hr class="divider">

<span class="section-label">// class progress</span>
<p class="section-desc">&gt; Games and projects built through the course.</p>

<div class="link-grid">
  <a href="{{site.baseurl}}/snake" class="tag-btn">snake</a>
  <a href="{{site.baseurl}}/gamify/parallax" class="tag-btn">fish-game</a>
  <a href="{{site.baseurl}}/gamify" class="tag-btn">gamify</a>
  <a href="{{site.baseurl}}/cs-pathway" class="tag-btn">cs-pathway</a>
</div>
