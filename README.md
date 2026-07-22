<div align="center">

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;700&display=swap');

  :root {
    --bg: #0d1117;
    --card: rgba(22, 27, 34, 0.8);
    --border: rgba(48, 54, 61, 0.6);
    --text: #e6edf3;
    --text-muted: #8b949e;
    --accent: #58a6ff;
    --accent2: #bc8cff;
    --accent3: #7ee787;
    --gradient: linear-gradient(135deg, #58a6ff, #bc8cff, #7ee787);
  }

  /* SMOOTH FADE IN */
  .fade-in {
    animation: fadeIn 0.8s ease-out both;
  }
  .fade-in-d1 { animation-delay: 0.1s; }
  .fade-in-d2 { animation-delay: 0.2s; }
  .fade-in-d3 { animation-delay: 0.3s; }
  .fade-in-d4 { animation-delay: 0.4s; }
  .fade-in-d5 { animation-delay: 0.5s; }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* SLIDE IN */
  .slide-left {
    animation: slideInLeft 0.6s ease-out both;
  }
  .slide-right {
    animation: slideInRight 0.6s ease-out both;
  }
  @keyframes slideInLeft {
    from { opacity: 0; transform: translateX(-40px); }
    to { opacity: 1; transform: translateX(0); }
  }
  @keyframes slideInRight {
    from { opacity: 0; transform: translateX(40px); }
    to { opacity: 1; transform: translateX(0); }
  }

  /* SCALE IN */
  .scale-in {
    animation: scaleIn 0.5s ease-out both;
  }
  @keyframes scaleIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  /* GLASS CARD */
  .glass-card {
    background: var(--card);
    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px;
    margin: 16px 0;
    transition: all 0.3s ease;
  }
  .glass-card:hover {
    border-color: rgba(88, 166, 255, 0.3);
    box-shadow: 0 0 20px rgba(88, 166, 255, 0.05);
    transform: translateY(-2px);
  }

  /* GRADIENT BORDER CARD */
  .gradient-border {
    position: relative;
    border-radius: 14px;
    padding: 2px;
    background: var(--gradient);
    background-size: 200% 200%;
    animation: gradientShift 4s ease infinite;
    margin: 16px 0;
  }
  .gradient-border > div {
    background: var(--bg);
    border-radius: 12px;
    padding: 22px;
  }
  @keyframes gradientShift {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }

  /* GLOW DOT */
  .glow-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    display: inline-block;
    margin-right: 6px;
    animation: glowPulse 2s ease-in-out infinite;
  }
  .glow-dot.green { background: #7ee787; box-shadow: 0 0 8px #7ee787; }
  .glow-dot.blue { background: #58a6ff; box-shadow: 0 0 8px #58a6ff; }
  .glow-dot.purple { background: #bc8cff; box-shadow: 0 0 8px #bc8cff; }
  @keyframes glowPulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
  }

  /* HOVER LIFT */
  .hover-lift {
    transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  }
  .hover-lift:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 40px rgba(0, 0, 0, 0.3);
  }

  /* PROGRESS BAR */
  .bar-track {
    width: 100%;
    height: 6px;
    background: rgba(255,255,255,0.05);
    border-radius: 3px;
    overflow: hidden;
    margin: 6px 0 12px;
  }
  .bar-fill {
    height: 100%;
    border-radius: 3px;
    background: var(--gradient);
    background-size: 200% 100%;
    animation: shimmer 2.5s linear infinite;
    transition: width 1s ease;
  }
  @keyframes shimmer {
    0% { background-position: 200% 0; }
    100% { background-position: -200% 0; }
  }

  /* SKILL CHIP */
  .chip {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    margin: 3px;
    border-radius: 20px;
    font-size: 13px;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 500;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--text);
    transition: all 0.25s ease;
  }
  .chip:hover {
    border-color: var(--accent);
    background: rgba(88, 166, 255, 0.08);
    transform: translateY(-2px);
  }

  /* ORBIT RING around avatar */
  .avatar-wrapper {
    position: relative;
    display: inline-block;
  }
  .avatar-wrapper::before {
    content: '';
    position: absolute;
    inset: -6px;
    border-radius: 50%;
    border: 2px solid transparent;
    border-top-color: var(--accent);
    border-right-color: var(--accent2);
    animation: orbitSpin 3s linear infinite;
  }
  .avatar-wrapper::after {
    content: '';
    position: absolute;
    inset: -14px;
    border-radius: 50%;
    border: 1px solid transparent;
    border-bottom-color: var(--accent3);
    border-left-color: var(--accent);
    animation: orbitSpin 5s linear infinite reverse;
    opacity: 0.4;
  }
  @keyframes orbitSpin {
    to { transform: rotate(360deg); }
  }

  /* TYPING CURSOR */
  .cursor-blink::after {
    content: '|';
    animation: blink 0.8s step-end infinite;
    color: var(--accent);
    font-weight: 300;
  }
  @keyframes blink {
    50% { opacity: 0; }
  }

  /* LINK STYLE */
  a { color: var(--accent); text-decoration: none; }
  a:hover { text-decoration: underline; }

  /* CODE */
  code {
    font-family: 'JetBrains Mono', monospace;
    background: rgba(110, 118, 129, 0.2);
    padding: 2px 6px;
    border-radius: 4px;
    font-size: 0.9em;
  }

  /* SUBTLE GRID BG */
  .section-bg {
    background-image:
      radial-gradient(circle at 1px 1px, rgba(88,166,255,0.03) 1px, transparent 0);
    background-size: 32px 32px;
    border-radius: 12px;
    padding: 24px;
  }

  /* STATUS BADGE */
  .status {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    font-family: 'Inter', sans-serif;
  }
  .status.open { background: rgba(126,231,135,0.1); color: #7ee787; border: 1px solid rgba(126,231,135,0.2); }
  .status.wip { background: rgba(88,166,255,0.1); color: #58a6ff; border: 1px solid rgba(88,166,255,0.2); }
  .status.done { background: rgba(188,140,255,0.1); color: #bc8cff; border: 1px solid rgba(188,140,255,0.2); }

  /* DIVIDER */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 40px 0;
    border: none;
  }
</style>

<!-- ══════════ AVATAR ══════════ -->
<div class="fade-in avatar-wrapper">
  <img src="https://avatars.githubusercontent.com/chidvielasparepalli" width="130" height="130" style="border-radius:50%; display:block; border: 3px solid #161b22;" alt="avatar" />
</div>

<!-- ══════════ NAME ══════════ -->
<div class="fade-in fade-in-d1" style="margin-top: 20px;">
  <h1 style="font-family:'Inter',sans-serif; font-weight:800; font-size:2.2em; margin:0; color:var(--text); letter-spacing:-0.5px;">
    Chidviela Sparepalli
  </h1>
  <p style="font-family:'JetBrains Mono',monospace; font-size:0.95em; color:var(--text-muted); margin:8px 0 0;">
    Full Stack Developer <span style="color:var(--accent);">/</span> Building things for the web
  </p>
</div>

<!-- ══════════ TYPING SVG ══════════ -->
<div class="fade-in fade-in-d2" style="margin-top: 16px;">
  <img src="https://readme-typing-svg.demolab.com?font=Inter&size=16&duration=3000&pause=1500&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=550&height=100&lines=Full+Stack+Developer;%26+Open+Source+Enthusiast;%26+Building+Scalable+Applications" alt="typing" />
</div>

<!-- ══════════ BADGES ══════════ -->
<div class="fade-in fade-in-d3" style="display:flex; justify-content:center; gap:8px; flex-wrap:wrap; margin-top:16px;">
  <img src="https://komarev.com/ghpvc/?username=chidvielasparepalli&label=Profile%20Views&color=0d1117&style=flat-square&labelColor=30363d" alt="views" />
  <img src="https://img.shields.io/github/stars/chidvielasparepalli?color=58a6ff&labelColor=0d1117&style=flat-square&label=Stars" alt="stars" />
  <img src="https://img.shields.io/github/followers/chidvielasparepalli?color=bc8cff&labelColor=0d1117&style=flat-square&label=Followers" alt="followers" />
  <img src="https://img.shields.io/badge/Status-<span class="glow-dot green"></span>-0d1117?style=flat-square&labelColor=30363d&color=7ee787" alt="status" />
</div>

<!-- ══════════ ABOUT ══════════ -->
<div class="fade-in fade-in-d4" style="max-width:620px; margin:30px auto 0;">
  <div class="glass-card section-bg" style="text-align:left;">
    <h3 style="font-family:'Inter',sans-serif; font-weight:700; font-size:1em; color:var(--text-muted); margin:0 0 12px; text-transform:uppercase; letter-spacing:1.5px;">
      About
    </h3>
    <p style="font-family:'Inter',sans-serif; font-size:0.95em; color:var(--text); line-height:1.7; margin:0;">
      I architect and build end-to-end web applications with a focus on performance, clean code, and
      delightful user experiences. Passionate about open source, system design, and turning complex problems
      into simple, elegant solutions.
    </p>
    <div style="margin-top:16px; display:flex; gap:8px; flex-wrap:wrap;">
      <span class="chip"><span class="glow-dot blue"></span>Open to Work</span>
      <span class="chip"><span class="glow-dot green"></span>Available for Freelance</span>
      <span class="chip"><span class="glow-dot purple"></span>Open Source</span>
    </div>
  </div>
</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- STATS SECTION -->
<!-- ═══════════════════════════════════ -->
<div align="center">

<h2 style="font-family:'Inter',sans-serif; font-weight:700; color:var(--text); font-size:1.3em; margin-bottom:20px;">
  <span style="color:var(--accent);">—</span> GitHub Analytics <span style="color:var(--accent);">—</span>
</h2>

<table>
<tr>
<td class="slide-left" width="50%">
  <div class="gradient-border">
    <div>
      <img src="https://github-readme-stats.vercel.app/api?username=chidvielasparepalli&show_icons=true&theme=tokyonight&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=bc8cff&text_color=e6edf3&include_all_commits=true&count_private=true" width="100%" alt="stats" />
    </div>
  </div>
</td>
<td class="slide-right" width="50%">
  <div class="gradient-border">
    <div>
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=chidvielasparepalli&theme=tokyonight&background=0d1117&hide_border=true&ring=58a6ff&fire=bc8cff&currStreakLabel=7ee787&sideLabels=e6edf3&stroke=58a6ff" width="100%" alt="streak" />
    </div>
  </div>
</td>
</tr>
</table>

<div class="scale-in" style="max-width:580px; margin:16px auto;">
  <div class="gradient-border">
    <div>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=chidvielasparepalli&layout=compact&theme=tokyonight&bg_color=0d1117&hide_border=true&title_color=58a6ff&text_color=e6edf3&langs_count=8" width="100%" alt="langs" />
    </div>
  </div>
</div>

<!-- Contribution Graph -->
<div class="scale-in" style="max-width:750px; margin:16px auto;">
  <div class="gradient-border">
    <div style="padding:16px;">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=chidvielasparepalli&bg_color=0d1117&color=58a6ff&line=bc8cff&point=7ee787&area=true&area_color=58a6ff&hide_border=true" width="100%" alt="activity" style="border-radius:8px;" />
    </div>
  </div>
</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- TECH STACK -->
<!-- ═══════════════════════════════════ -->
<div align="center">

<h2 style="font-family:'Inter',sans-serif; font-weight:700; color:var(--text); font-size:1.3em; margin-bottom:20px;">
  <span style="color:var(--accent2);">—</span> Tech Stack <span style="color:var(--accent2);">—</span>
</h2>

<div class="slide-left" style="max-width:750px;">

  <div class="glass-card section-bg hover-lift">
    <div style="display:flex; align-items:center; gap:8px; margin-bottom:16px;">
      <span class="glow-dot blue"></span>
      <h3 style="font-family:'Inter',sans-serif; font-weight:600; font-size:0.9em; color:var(--text-muted); margin:0; text-transform:uppercase; letter-spacing:1px;">Frontend</h3>
    </div>

    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>React / Next.js</span><span style="color:var(--accent);">90%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:90%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>TypeScript</span><span style="color:var(--accent2);">85%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:85%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>Tailwind CSS</span><span style="color:var(--accent3);">88%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:88%;"></div></div>
    </div>

    <div style="text-align:left; margin-top:12px;">
      <img class="chip" src="https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB" alt="react" />
      <img class="chip" src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white" alt="next" />
      <img class="chip" src="https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white" alt="ts" />
      <img class="chip" src="https://img.shields.io/badge/Tailwind-38B2AC?style=flat&logo=tailwind-css&logoColor=white" alt="tailwind" />
      <img class="chip" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black" alt="js" />
      <img class="chip" src="https://img.shields.io/badge/Redux-593D88?style=flat&logo=redux&logoColor=white" alt="redux" />
    </div>
  </div>

</div>

<div class="slide-right" style="max-width:750px;">

  <div class="glass-card section-bg hover-lift">
    <div style="display:flex; align-items:center; gap:8px; margin-bottom:16px;">
      <span class="glow-dot purple"></span>
      <h3 style="font-family:'Inter',sans-serif; font-weight:600; font-size:0.9em; color:var(--text-muted); margin:0; text-transform:uppercase; letter-spacing:1px;">Backend</h3>
    </div>

    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>Node.js / Express</span><span style="color:var(--accent2);">88%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:88%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>Python / Django</span><span style="color:var(--accent3);">75%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:75%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>PostgreSQL / MongoDB</span><span style="color:var(--accent);">80%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:80%;"></div></div>
    </div>

    <div style="text-align:left; margin-top:12px;">
      <img class="chip" src="https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white" alt="node" />
      <img class="chip" src="https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white" alt="express" />
      <img class="chip" src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="python" />
      <img class="chip" src="https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white" alt="django" />
      <img class="chip" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white" alt="pg" />
      <img class="chip" src="https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white" alt="mongo" />
      <img class="chip" src="https://img.shields.io/badge/GraphQL-E10098?style=flat&logo=graphql&logoColor=white" alt="gql" />
    </div>
  </div>

</div>

<div class="slide-left" style="max-width:750px;">

  <div class="glass-card section-bg hover-lift">
    <div style="display:flex; align-items:center; gap:8px; margin-bottom:16px;">
      <span class="glow-dot green"></span>
      <h3 style="font-family:'Inter',sans-serif; font-weight:600; font-size:0.9em; color:var(--text-muted); margin:0; text-transform:uppercase; letter-spacing:1px;">DevOps & Tools</h3>
    </div>

    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>Docker / CI/CD</span><span style="color:var(--accent3);">70%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:70%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>AWS / Cloud</span><span style="color:var(--accent);">65%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:65%;"></div></div>
    </div>
    <div style="margin-bottom:12px;">
      <div style="display:flex; justify-content:space-between; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--text-muted);">
        <span>Git / Linux</span><span style="color:var(--accent2);">90%</span>
      </div>
      <div class="bar-track"><div class="bar-fill" style="width:90%;"></div></div>
    </div>

    <div style="text-align:left; margin-top:12px;">
      <img class="chip" src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" alt="docker" />
      <img class="chip" src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white" alt="aws" />
      <img class="chip" src="https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white" alt="vercel" />
      <img class="chip" src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white" alt="git" />
      <img class="chip" src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black" alt="linux" />
      <img class="chip" src="https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black" alt="firebase" />
    </div>
  </div>

</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- PINNED PROJECTS -->
<!-- ═══════════════════════════════════ -->
<div align="center">

<h2 style="font-family:'Inter',sans-serif; font-weight:700; color:var(--text); font-size:1.3em; margin-bottom:20px;">
  <span style="color:var(--accent3);">—</span> Featured Projects <span style="color:var(--accent3);">—</span>
</h2>

<div class="scale-in" style="display:flex; justify-content:center; gap:12px; flex-wrap:wrap; max-width:800px; margin:0 auto;">

  <a href="https://github.com/chidvielasparepalli?tab=repositories&sort=stargazers" style="flex:1; min-width:250px; max-width:380px;">
    <div class="glass-card hover-lift" style="text-align:left; height:100%; padding:20px;">
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="var(--accent)"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9z"/></svg>
        <span style="font-family:'Inter',sans-serif; font-weight:600; color:var(--accent); font-size:0.95em;">Pinned Repos</span>
      </div>
      <p style="font-family:'Inter',sans-serif; font-size:0.85em; color:var(--text-muted); margin:0;">
        Explore my top repositories sorted by stars.
      </p>
    </div>
  </a>

  <a href="#" style="flex:1; min-width:250px; max-width:380px;">
    <div class="glass-card hover-lift" style="text-align:left; height:100%; padding:20px;">
      <div style="display:flex; align-items:center; gap:8px; margin-bottom:8px;">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="var(--accent2)"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
        <span style="font-family:'Inter',sans-serif; font-weight:600; color:var(--accent2); font-size:0.95em;">Open Source</span>
      </div>
      <p style="font-family:'Inter',sans-serif; font-size:0.85em; color:var(--text-muted); margin:0;">
        Contributing to projects that matter.
      </p>
    </div>
  </a>

</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- SNAKE / CONTRIBUTION -->
<!-- ═══════════════════════════════════ -->
<div align="center">

<h2 style="font-family:'Inter',sans-serif; font-weight:700; color:var(--text); font-size:1.3em; margin-bottom:20px;">
  <span style="color:var(--accent);">—</span> Contribution Graph <span style="color:var(--accent);">—</span>
</h2>

<div class="scale-in" style="max-width:800px;">
  <div class="gradient-border">
    <div style="padding:16px;">
      <img src="https://raw.githubusercontent.com/chidvielasparepalli/chidvielasparepalli/output/github-contribution-grid-snake-dark.svg" alt="snake" width="100%" style="border-radius:8px;" />
    </div>
  </div>
</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- CONNECT -->
<!-- ═══════════════════════════════════ -->
<div align="center">

<h2 style="font-family:'Inter',sans-serif; font-weight:700; color:var(--text); font-size:1.3em; margin-bottom:20px;">
  <span style="color:var(--accent2);">—</span> Connect <span style="color:var(--accent2);">—</span>
</h2>

<div class="fade-in" style="display:flex; justify-content:center; gap:10px; flex-wrap:wrap;">

  <a href="https://github.com/chidvielasparepalli" class="hover-lift" style="display:inline-block;">
    <div class="glass-card" style="padding:12px 20px; display:flex; align-items:center; gap:8px;">
      <svg width="20" height="20" viewBox="0 0 16 16" fill="var(--text)"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      <span style="font-family:'Inter',sans-serif; font-weight:500; font-size:0.9em;">GitHub</span>
    </div>
  </a>

  <a href="#" class="hover-lift" style="display:inline-block;">
    <div class="glass-card" style="padding:12px 20px; display:flex; align-items:center; gap:8px;">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="var(--accent)"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      <span style="font-family:'Inter',sans-serif; font-weight:500; font-size:0.9em;">LinkedIn</span>
    </div>
  </a>

  <a href="#" class="hover-lift" style="display:inline-block;">
    <div class="glass-card" style="padding:12px 20px; display:flex; align-items:center; gap:8px;">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="var(--accent3)"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
      <span style="font-family:'Inter',sans-serif; font-weight:500; font-size:0.9em;">Twitter</span>
    </div>
  </a>

  <a href="#" class="hover-lift" style="display:inline-block;">
    <div class="glass-card" style="padding:12px 20px; display:flex; align-items:center; gap:8px;">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="var(--accent2)"><path d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.928 5.493a3 3 0 01-3.144 0L1.5 8.67z"/><path d="M22.5 6.908V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.158l9.714 5.978a1.5 1.5 0 001.572 0L22.5 6.908z"/></svg>
      <span style="font-family:'Inter',sans-serif; font-weight:500; font-size:0.9em;">Email</span>
    </div>
  </a>

</div>

</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════ -->
<!-- FOOTER -->
<!-- ═══════════════════════════════════ -->
<div align="center" style="margin-bottom:30px;">

<div class="glass-card" style="display:inline-block; max-width:500px; padding:20px 30px;">
  <img src="https://raw.githubusercontent.com/Plarameo/animated-github-svg/main/line_animation.svg" width="100%" style="margin-bottom:10px;" />
  <p style="font-family:'Inter',sans-serif; font-size:0.85em; color:var(--text-muted); margin:8px 0 0;">
    Built with care by <strong style="color:var(--text);">Chidviela Sparepalli</strong>
  </p>
  <p style="font-family:'JetBrains Mono',monospace; font-size:0.75em; color:var(--text-muted); margin:4px 0 0; opacity:0.6;">
    "First, solve the problem. Then, write the code."
  </p>
</div>

</div>
