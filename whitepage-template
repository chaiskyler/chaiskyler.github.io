<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Whitepaper Title — Author / Organization</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400..800;1,400..800&family=Playfair+Display:ital,wght@0,400..900;1,400..900&display=swap" rel="stylesheet">

  <style>
    /* ── Tokens ───────────────────────────────────────────────── */
    :root {
      --bg:            #FAFAF8;
      --surface:       #F2F0EB;
      --border:        #D8D4CC;
      --text-primary:  #1A1916;
      --text-secondary:#5A5852;
      --text-muted:    #8A8780;
      --accent:        #385DFF;
      --link:          #385DFF;
      --toggle-bg:     #D8D4CC;
      --toggle-knob:   #FAFAF8;
      --code-bg:       #EEE;
      --garamond:         'EB Garamond', Garamond;
      --playfair:          'Playfair Display';
      --max-width:     950px;
      --gutter:        clamp(1.25rem, 5vw, 3rem);
    }

    [data-theme="dark"] {
      --bg:            #131310;
      --surface:       #1E1D1A;
      --border:        #333028;
      --text-primary:  #EDEAE4;
      --text-secondary:#A09C94;
      --text-muted:    #6A6660;
      --accent:        #385DFF;
      --link:          #385DFF;
      --toggle-bg:     #333028;
      --toggle-knob:   #EDEAE4;
      --code-bg:       #252420;
    }

    /* ── Reset ───────────────────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text-primary);
      font-family: var(--garamond);
      font-size: 18px;
      line-height: 1.25;
      transition: background 0.2s, color 0.2s;
      -webkit-font-smoothing: antialiased;
    }

    /* ── Layout ──────────────────────────────────────────────── */
    .page {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 2rem var(--gutter) 2rem;
    }

    /* ── Topbar ──────────────────────────────────────────────── */
    .topbar {
      display: flex;
      justify-content: flex-end;
      align-items: right;
      margin-bottom: 3rem;
      padding-bottom: 1.25rem;
      border-bottom: 1px solid var(--border);
    }

    /* ── Toggle ──────────────────────────────────────────────── */
    .toggle-wrap {
      display: flex;
      align-items: right;
      gap: 10px;
      cursor: pointer;
      user-select: none;
    }

    .toggle-label {
      font-family: var(--playfair);
      font-size: 12px;
      align: right;
      color: var(--text-muted);
      letter-spacing: 0.05em;
    }

    .toggle {
      position: relative;
      width: 40px;
      height: 22px;
      background: var(--toggle-bg);
      border-radius: 11px;
      transition: background 0.2s;
      flex-shrink: 0;
    }

    .toggle::after {
      content: '';
      position: absolute;
      top: 3px;
      left: 3px;
      width: 16px;
      height: 16px;
      background: var(--toggle-knob);
      border-radius: 50%;
      transition: transform 0.2s, background 0.2s;
    }

    [data-theme="dark"] .toggle {
      background: var(--accent);
    }

    [data-theme="dark"] .toggle::after {
      transform: translateX(18px);
    }

    /* ── Cover ───────────────────────────────────────────────── */
    .cover {
      margin-bottom: 3.5rem;
    }

    h1 {
      font-family: var(--playfair);
      font-size: clamp(1.8rem, 4vw, 2.6rem);
      font-weight: 700;
      line-height: 1.25;
      color: var(--text-primary);
      margin-bottom: 1rem;
    }

    .cover-subtitle {
      font-family: var(--garamond);
      font-size: 17px;
      font-weight: 300;
      color: var(--text-secondary);
      margin-bottom: 2rem;
      line-height: 1.6;
    }

    .cover-meta {
      display: grid; 
      grid-template-columns: auto 1fr;
      gap: 1.25rem 2rem;
      font-family: var(--garamond);
      font-size: 13px;
      color: var(--text-muted);
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
      border-top: 1px solid var(--border);
    }

    .cover-meta-item strong {
      display: block;
      font-weight: 500;
      color: var(--text-secondary);
      margin-bottom: 2px;
      padding-bottom: 0.75rem;
    }
    
    .cover-meta-item:last-child {
    text-align: right;	
  	}

    /* ── TOC ─────────────────────────────────────────────────── */
    .toc {
      margin-bottom: 3.5rem;
      padding: 1.5rem;
      background: var(--surface);
      border-radius: 3px;
      border: 1px solid var(--border);
    }

    .toc-title {
      font-family: var(--playfair);
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .toc ol {
      list-style: none;
      counter-reset: toc;
    }

    .toc ol li {
      counter-increment: toc;
      display: flex;
      align-items: baseline;
      gap: 0.75rem;
      font-family: var(--playfair);
      font-size: 14px;
      color: var(--text-secondary);
      padding: 3px 0;
    }

    .toc ol li::before {
      content: counter(toc);
      font-size: 11px;
      font-weight: 500;
      color: var(--text-muted);
      min-width: 16px;
    }

    .toc ol li a {
      color: var(--link);
      text-decoration: none;
    }

    .toc ol li a:hover {
      text-decoration: underline;
    }

    /* ── Body content ────────────────────────────────────────── */
    .section {
      margin-bottom: 3rem;
    }

    h2 {
      font-family: var(--playfair);
      font-size: 1.4rem;
      font-weight: 700;
      line-height: 1.3;
      color: var(--text-primary);
      margin-bottom: 1rem;
      margin-top: 2.5rem;
      padding-top: 2rem;
      border-top: 1px solid var(--border);
    }

    h2:first-child { margin-top: 0; border-top: none; padding-top: 0; }

    h3 {
      font-family: var(--playfair);
      font-size: 1rem;
      font-weight: 500;
      letter-spacing: 0.02em;
      color: var(--text-secondary);
      margin-top: 1.75rem;
      margin-bottom: 0.5rem;
      text-transform: uppercase;
      font-size: 12px;
      letter-spacing: 0.08em;
    }

    p { margin-bottom: 1.2rem; }

    a {
      color: var(--link);
      text-decoration: underline;
      text-decoration-color: color-mix(in srgb, var(--link) 35%, transparent);
      text-underline-offset: 3px;
    }

    a:hover { color: red; }
    .toc ol li a:hover { color: red; }
    .fn-ref a:hover { color: red; }

    /* ── Callout ─────────────────────────────────────────────── */
    .callout {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 6px;
      padding: 1.25rem 1.5rem;
      margin: 1.75rem 0;
      font-size: 16px;
    }

    .callout-label {
      font-family: var(--playfair);
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 0.5rem;
    }

    /* ── Blockquote ──────────────────────────────────────────── */
    blockquote {
      border-left: 3px solid var(--border);
      margin: 1.75rem 0;
      padding: 0.25rem 1.5rem;
      color: var(--text-secondary);
      font-style: italic;
    }

    blockquote cite {
      display: block;
      font-style: normal;
      font-family: var(--garamond);
      font-size: 13px;
      color: var(--text-muted);
      margin-top: 0.5rem;
    }

    /* ── Code ────────────────────────────────────────────────── */
    code {
      font-family: 'Courier New', monospace;
      font-size: 0.85em;
      background: var(--code-bg);
      padding: 1px 5px;
      border-radius: 3px;
      color: var(--text-secondary);
    }

    pre {
      background: var(--code-bg);
      padding: 1.25rem;
      border-radius: 6px;
      overflow-x: auto;
      margin: 1.5rem 0;
      font-size: 14px;
      line-height: 1.6;
      border: 1px solid var(--border);
    }

    pre code { background: none; padding: 0; }

    /* ── Footnotes ───────────────────────────────────────────── */
    .footnotes {
      margin-top: 4rem;
      padding-top: 1.5rem;
      border-top: 1px solid var(--border);
      font-family: var(--garamond);
      font-size: 13px;
      color: var(--text-muted);
      line-height: 1.6;
    }

    .footnotes-label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    .footnotes ol {
      padding-left: 1.5rem;
    }

    .footnotes li {
      margin-bottom: 0.5rem;
    }



    /* ── Footnote tooltip ────────────────────────────────────── */
    .fn-ref {
      position: relative;
      display: inline-block;
    }

    .fn-ref a {
      font-family: var(--garamond);
      font-size: 11px;
      color: var(--accent);
      text-decoration: none;
      cursor: default;
    }

    .fn-tooltip {
      display: none;
      position: absolute;
      bottom: calc(100% + 6px);
      left: 50%;
      transform: translateX(-50%);
      width: 260px;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 5px;
      padding: 0.6rem 0.85rem;
      font-family: var(--garamond);
      font-size: 12px;
      line-height: 1.55;
      color: var(--text-secondary);
      z-index: 100;
      pointer-events: none;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }

    .fn-tooltip::after {
      content: '';
      position: absolute;
      top: 100%;
      left: 50%;
      transform: translateX(-50%);
      border: 5px solid transparent;
      border-top-color: var(--border);
    }

    .fn-tooltip::before {
      content: '';
      position: absolute;
      top: calc(100% - 1px);
      left: 50%;
      transform: translateX(-50%);
      border: 5px solid transparent;
      border-top-color: var(--surface);
      z-index: 1;
    }

    .fn-ref:hover .fn-tooltip,
    .fn-ref:focus-within .fn-tooltip {
      display: block;
    }

    .fn-ref.tip-left .fn-tooltip  { left: 0;    transform: none; }
    .fn-ref.tip-left .fn-tooltip::after,
    .fn-ref.tip-left .fn-tooltip::before { left: 20px; transform: none; }

    .fn-ref.tip-right .fn-tooltip  { left: auto; right: 0; transform: none; }
    .fn-ref.tip-right .fn-tooltip::after,
    .fn-ref.tip-right .fn-tooltip::before { left: auto; right: 20px; transform: none; }

    /* ── PDF dropdown ────────────────────────────────────────── */
    .pdf-toggle {
      font-family: var(--playfair);
      font-size: 13px;
      color: var(--accent);
      cursor: pointer;
      user-select: none;
      background: none;
      border: none;
      padding: 0;
      display: flex;
      align-items: center;
      gap: 4px;
      letter-spacing: 0.01em;
    }

    .pdf-toggle:hover { color: red; }

    .pdf-toggle .pdf-caret {
      display: inline-block;
      font-style: normal;
      transition: transform 0.18s;
      font-size: 10px;
    }

    .pdf-toggle[aria-expanded="true"] .pdf-caret {
      transform: rotate(90deg);
    }

    .pdf-links {
      display: none;
      margin-top: 8px;
      gap: 8px;
      flex-wrap: wrap;
    }

    .pdf-links.open { display: flex; }

    .pdf-btn {
      font-family: var(--playfair);
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--text-muted);
      text-decoration: none;
      border: 1px solid var(--border);
      border-radius: 3px;
      padding: 3px 10px;
      transition: color 0.15s, border-color 0.15s;
    }

    .pdf-btn:hover {
      color: red;
      border-color: red;
    }

    /* ── Print ───────────────────────────────────────────────── */
    @media print {
      [data-theme="dark"] {
        --bg: #fff;
        --text-primary: #000;
        --text-secondary: #333;
      }
      .topbar, .toggle-wrap { display: none; }
    }
  </style>
</head>

<body>
<div class="page">

  <!-- Topbar -->
  <div class="topbar">
    <div class="toggle-wrap" onclick="toggleTheme()" role="button" aria-label="Toggle dark mode" tabindex="0">
      <span class="toggle-label" id="toggle-label">Light</span>
      <div class="toggle" id="toggle" aria-hidden="true"></div>
    </div>
  </div>

  <!-- Cover -->
  <div class="cover">
    <h1>The Title of Your Whitepaper Goes Here Across Multiple Lines If Needed</h1>
    <p class="cover-subtitle">A concise subtitle that clarifies scope, method, or central argument — one or two lines at most.</p>
    <div class="cover-meta">
      <div class="cover-meta-item">
        <strong>Chai Skyler</strong>
        <div style="margin-top: 6px;">
        <button class="pdf-toggle" id="pdf-toggle" aria-expanded="false" onclick="togglePdf()">
            <i class="pdf-caret">›</i> pdf
          </button>
          <div class="pdf-links" id="pdf-links">
            <a class="pdf-btn" href="whitepaper-light.pdf" download>light</a>
            <a class="pdf-btn" href="whitepaper-dark.pdf" download>dark</a>
        </div>
          </div>
      </div>
      <div class="cover-meta-item">
        <strong>Month Year</strong>
    </div>
  </div>

  <!-- Table of Contents -->
  <div class="toc">
    <div class="toc-title">Contents</div>
    <ol>
      <li><a href="#introduction">Introduction</a></li>
      <li><a href="#background">Background and Context</a></li>
      <li><a href="#argument">Central Argument</a></li>
      <li><a href="#implications">Implications</a></li>
      <li><a href="#conclusion">Conclusion</a></li>
    </ol>
  </div>

  <!-- Body -->
  <div class="section" id="introduction">
    <h2>1. Introduction</h2>
    <p>Begin with the problem or question that motivates the paper. Establish why it matters and to whom. A strong opening paragraph earns the reader's attention before asking for their patience with the argument that follows.</p>
    <p>Lay out the structure of the paper in a brief roadmap. Readers of whitepapers are often busy; tell them what they will find and where.</p>
  </div>

  <div class="section" id="background">
    <h2>2. Background and Context</h2>
    <p>Provide the minimum necessary context for the reader to follow the argument. This is not a literature review — it is orientation. Assume an intelligent reader who may not share your specialization.</p>

    <h3>2.1 Sub-topic</h3>
    <p>Use third-level headings sparingly and only when a section genuinely requires subdivision. Avoid hierarchical nesting for its own sake.</p>

    <blockquote>
      A quotation relevant to the argument can anchor a section, introduce a counterpoint, or crystallize a concept in borrowed language.
      <cite>— Source, Year</cite>
    </blockquote>

    <div class="callout">
      <div class="callout-label">Key Definition</div>
      <p style="margin: 0;">Use callout boxes for definitions, important caveats, or standalone facts that readers may want to locate quickly when skimming.</p>
    </div>
  </div>

  <div class="section" id="argument">
    <h2>3. Central Argument</h2>
    <p>State your argument plainly before elaborating. Avoid burying the claim in qualification. Readers should be able to identify your thesis within the first paragraph of this section.</p>
    <p>Develop the argument in prose. Resist the temptation to use bullet lists as a substitute for reasoning — connected prose forces you to articulate the relationships between ideas. Reserve lists for genuinely enumerable items without internal logic dependencies.</p>
    <p>Engage with the strongest counterargument available. A paper that ignores obvious objections is unconvincing. Steel-man the opposing view before rebutting it.<sup class="fn-ref" id="ref1"><a href="#fn1">1</a><span class="fn-tooltip">This is a footnote. Use footnotes for citations, tangential elaborations, or methodological caveats that would interrupt the prose flow.</span></sup></p>
  </div>

  <div class="section" id="implications">
    <h2>4. Implications</h2>
    <p>What follows if the argument is correct? Be specific about who is affected and how. Avoid vague gestures toward "further research" as a substitute for actual implications.</p>
    <p>Distinguish between near-term practical implications and longer-term or more speculative ones. Be honest about which is which.</p>
  </div>

  <div class="section" id="conclusion">
    <h2>5. Conclusion</h2>
    <p>Restate the central claim concisely — not a summary of every section, but a crystallization of what you argued and why it matters. A good conclusion leaves the reader with a single clear thought, not a list.</p>
    <p>End with a sentence or two that places the work in a larger frame, or gestures at what remains open. Resist the impulse to end with exhortation.</p>
  </div>

  <!-- Footnotes -->
  <div class="footnotes">
    <div class="footnotes-label">Notes</div>
    <ol>
      <li id="fn1">This is a footnote. Use footnotes for citations, tangential elaborations, or methodological caveats that would interrupt the prose flow. <a href="#ref1" aria-label="Return to text">↑</a></li>
    </ol>
  </div>


</div>

<script>
  const html = document.documentElement;
  const label = document.getElementById('toggle-label');

  const saved = localStorage.getItem('theme');
  if (saved) { html.setAttribute('data-theme', saved); updateLabel(); }
  else if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
    html.setAttribute('data-theme', 'dark'); updateLabel();
  }

  function toggleTheme() {
    const next = html.getAttribute('data-theme') === 'dark' ? 'light' : 'dark';
    html.setAttribute('data-theme', next);
    localStorage.setItem('theme', next);
    updateLabel();
  }

  function updateLabel() {
    label.textContent = html.getAttribute('data-theme') === 'dark' ? 'Dark' : 'Light';
  }

  document.getElementById('toggle').parentElement.addEventListener('keydown', e => {
    if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); toggleTheme(); }
  });

  function togglePdf() {
    const btn = document.getElementById('pdf-toggle');
    const links = document.getElementById('pdf-links');
    const open = links.classList.toggle('open');
    btn.setAttribute('aria-expanded', open);
  }

  /* Footnote tooltip edge detection — nudge left/right if near viewport edge */
  document.querySelectorAll('.fn-ref').forEach(ref => {
    ref.addEventListener('mouseenter', () => {
      const tip = ref.querySelector('.fn-tooltip');
      if (!tip) return;
      ref.classList.remove('tip-left', 'tip-right');
      const r = ref.getBoundingClientRect();
      const tw = 260;
      const vw = window.innerWidth;
      if (r.left + r.width / 2 - tw / 2 < 8) ref.classList.add('tip-left');
      else if (r.left + r.width / 2 + tw / 2 > vw - 8) ref.classList.add('tip-right');
    });
  });
</script>
</body>
</html>
