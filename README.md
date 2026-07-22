# Hi there, I'm Chidvielas! 👋

<div align="center">

<!-- ANIMATED CURSOR + GLOW EFFECTS -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&family=Press+Start+2P&display=swap');

  :root {
    --primary: #F72585;
    --secondary: #7209B7;
    --accent: #4361EE;
    --neon: #00F0FF;
    --gold: #FFD700;
    --bg-dark: #0a0a0f;
    --glass: rgba(255, 255, 255, 0.05);
    --glass-border: rgba(255, 255, 255, 0.1);
  }

  * { cursor: url('https://raw.githubusercontent.com/sumit-345/cursor/refs/heads/main/cursor.png'), auto !important; }
  *:hover { cursor: url('https://raw.githubusercontent.com/sumit-345/cursor/refs/heads/main/hover.png'), pointer !important; }

  body {
    background: var(--bg-dark);
    overflow-x: hidden;
    font-family: 'Rajdhani', sans-serif;
  }

  /* ANIMATED BORDER GLOW */
  .glow-border {
    border: 2px solid transparent;
    background: linear-gradient(var(--bg-dark), var(--bg-dark)) padding-box,
                linear-gradient(90deg, var(--primary), var(--secondary), var(--accent), var(--neon), var(--primary)) border-box;
    background-size: 300% 300%;
    animation: borderGlow 4s ease infinite;
    border-radius: 16px;
    padding: 20px;
    margin: 15px 0;
  }

  @keyframes borderGlow {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }

  /* GLASS MORPHISM */
  .glass {
    background: rgba(15, 15, 25, 0.7);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 24px;
    box-shadow: 0 8px 32px rgba(247, 37, 133, 0.15),
                inset 0 0 20px rgba(255, 255, 255, 0.02);
  }

  .glass-blue {
    background: rgba(15, 15, 25, 0.7);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(67, 97, 238, 0.3);
    border-radius: 16px;
    padding: 24px;
    box-shadow: 0 8px 32px rgba(67, 97, 238, 0.15),
                inset 0 0 20px rgba(67, 97, 238, 0.02);
  }

  .glass-purple {
    background: rgba(15, 15, 25, 0.7);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(114, 9, 183, 0.3);
    border-radius: 16px;
    padding: 24px;
    box-shadow: 0 8px 32px rgba(114, 9, 183, 0.15);
  }

  /* NEON TEXT */
  .neon-pink {
    color: var(--primary);
    text-shadow: 0 0 7px var(--primary), 0 0 10px var(--primary),
                 0 0 21px var(--primary), 0 0 42px var(--primary);
    font-family: 'Orbitron', sans-serif;
    font-weight: 900;
  }

  .neon-blue {
    color: var(--neon);
    text-shadow: 0 0 7px var(--neon), 0 0 10px var(--neon),
                 0 0 21px var(--neon), 0 0 42px var(--neon);
    font-family: 'Orbitron', sans-serif;
    font-weight: 900;
  }

  .neon-purple {
    color: var(--secondary);
    text-shadow: 0 0 7px var(--secondary), 0 0 10px var(--secondary),
                 0 0 21px var(--secondary);
    font-family: 'Orbitron', sans-serif;
    font-weight: 900;
  }

  /* FLOATING ANIMATION */
  .float {
    animation: float 3s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
  }

  .float-delay {
    animation: float 3s ease-in-out infinite 0.5s;
  }

  /* PULSE GLOW */
  .pulse-glow {
    animation: pulseGlow 2s ease-in-out infinite;
  }

  @keyframes pulseGlow {
    0%, 100% { box-shadow: 0 0 5px var(--primary), 0 0 10px var(--primary); }
    50% { box-shadow: 0 0 20px var(--primary), 0 0 40px var(--primary), 0 0 60px var(--primary); }
  }

  /* SHAKING ANIMATION */
  .shake {
    animation: shake 0.5s ease-in-out infinite;
  }

  @keyframes shake {
    0%, 100% { transform: rotate(0deg); }
    25% { transform: rotate(-3deg); }
    75% { transform: rotate(3deg); }
  }

  /* SLIDE IN ANIMATIONS */
  .slide-left {
    animation: slideLeft 1s ease-out forwards;
    opacity: 0;
  }

  @keyframes slideLeft {
    from { opacity: 0; transform: translateX(-50px); }
    to { opacity: 1; transform: translateX(0); }
  }

  .slide-right {
    animation: slideRight 1s ease-out forwards;
    opacity: 0;
  }

  @keyframes slideRight {
    from { opacity: 0; transform: translateX(50px); }
    to { opacity: 1; transform: translateX(0); }
  }

  .slide-up {
    animation: slideUp 0.8s ease-out forwards;
    opacity: 0;
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* GLITCH EFFECT */
  .glitch {
    position: relative;
    animation: glitch 2s infinite;
  }

  @keyframes glitch {
    0%, 100% { text-shadow: 2px 0 var(--primary), -2px 0 var(--neon); }
    25% { text-shadow: -2px -2px var(--primary), 2px 2px var(--neon); }
    50% { text-shadow: 2px 2px var(--primary), -2px -2px var(--neon); }
    75% { text-shadow: -2px 0 var(--primary), 2px 0 var(--neon); }
  }

  /* ROTATE ON HOVER */
  .hover-spin:hover {
    animation: spin 0.6s ease;
  }

  @keyframes spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }

  /* SCALE BOUNCE */
  .hover-bounce:hover {
    animation: bounce 0.4s ease;
  }

  @keyframes bounce {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.15); }
  }

  /* AURA EFFECT */
  .aura {
    position: relative;
  }
  .aura::before {
    content: '';
    position: absolute;
    top: -3px; left: -3px; right: -3px; bottom: -3px;
    background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent), var(--neon));
    background-size: 400% 400%;
    animation: auraRotate 3s ease infinite;
    border-radius: 18px;
    z-index: -1;
    filter: blur(8px);
    opacity: 0.6;
  }

  @keyframes auraRotate {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }

  /* PROGRESS BAR */
  .progress-bar {
    width: 100%;
    height: 8px;
    background: rgba(255,255,255,0.05);
    border-radius: 10px;
    overflow: hidden;
    margin: 5px 0;
  }
  .progress-fill {
    height: 100%;
    border-radius: 10px;
    background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
    background-size: 200% 100%;
    animation: shimmer 2s linear infinite;
  }

  @keyframes shimmer {
    0% { background-position: -200% 0; }
    100% { background-position: 200% 0; }
  }

  /* PARTICLE CONTAINER */
  .particles {
    position: relative;
    overflow: hidden;
  }
  .particles::before {
    content: '✦ ✧ ✦ ✧ ✦ ✧ ✦ ✧ ✦ ✧';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    font-size: 14px;
    color: rgba(247, 37, 133, 0.1);
    animation: sparkle 8s linear infinite;
    pointer-events: none;
    word-spacing: 30px;
    line-height: 2.5;
  }

  @keyframes sparkle {
    0% { opacity: 0; transform: translateY(0); }
    50% { opacity: 1; }
    100% { opacity: 0; transform: translateY(-20px); }
  }

  /* WAVE DIVIDER */
  .wave-divider {
    width: 100%;
    height: 60px;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 60"><path d="M0,30 Q150,0 300,30 T600,30 T900,30 T1200,30 V60 H0 Z" fill="%23F7258520"/></svg') repeat-x;
    background-size: 1200px 60px;
    animation: wave 6s linear infinite;
  }

  @keyframes wave {
    0% { background-position: 0 0; }
    100% { background-position: 1200px 0; }
  }

  /* SKILL CARD */
  .skill-card {
    display: inline-block;
    padding: 8px 16px;
    margin: 4px;
    border-radius: 12px;
    font-weight: 700;
    font-size: 14px;
    font-family: 'Rajdhani', sans-serif;
    transition: all 0.3s ease;
    border: 1px solid rgba(255,255,255,0.1);
    background: rgba(255,255,255,0.03);
  }
  .skill-card:hover {
    transform: translateY(-3px) scale(1.05);
    box-shadow: 0 10px 30px rgba(247, 37, 133, 0.3);
  }
</style>

<!-- LOADING SCREEN -->
<img src="https://img.shields.io/badge/-ARISE__-F72585?style=for-the-badge&labelColor=0a0a0f&animation=slide-up" alt="loading" width="0" height="0">

<!-- ANIMATED AVATAR WITH AURA -->
<div class="aura" style="display:inline-block; border-radius:50%; padding:3px; margin-bottom:15px;">
  <img src="https://avatars.githubusercontent.com/chidvielasparepalli" width="160" height="160" style="border-radius:50%; display:block;" alt="Avatar" />
</div>

<!-- NAME WITH GLITCH -->
<h1 class="glitch" style="font-family:'Orbitron',sans-serif; font-size:2.5em; margin:10px 0; color:#fff;">
  CHIDVIELA SPAREPALLI
</h1>

<!-- TYPING SVG -->
<img src="https://readme-typing-svg.demolab.com?font=Orbitron&size=20&duration=2500&pause=800&color=F72585&center=true&vCenter=true&multiline=true&repeat=true&width=700&height=140&lines=%E2%9A%94%EF%B8%8F+%E2%80%9C+I+Am+The+Shadow+Monarch+%E2%80%9D;%F0%9F%91%A8%EF%B8%8F+%E2%80%9C+The+Strongest+%E2%80%9D;%F0%9F%8E%AF+%E2%80%9C+Striker+No.1+%E2%80%9D" alt="Typing SVG" />

<!-- BADGES ROW -->
<div style="display:flex; justify-content:center; gap:10px; flex-wrap:wrap; margin:15px 0;">
  <img src="https://komarev.com/ghpvc/?username=chidvielasparepalli&color=F72585&style=for-the-badge&label=%E2%9A%94%EF%B8%8F+LEVEL" alt="Level" />
  <img src="https://img.shields.io/badge/%F0%9F%94%A5+ARISE-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=F72585" alt="Arise" />
  <img src="https://img.shields.io/badge/%F0%9F%91%A8%EF%B8%8F+Solo+Leveling-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=7209B7" alt="Solo" />
  <img src="https://img.shields.io/badge/%F0%9F%90%B9+JJK-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=4361EE" alt="JJK" />
  <img src="https://img.shields.io/badge/%E2%9A%94%EF%B8%8F+Naruto-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=F77F00" alt="Naruto" />
  <img src="https://img.shields.io/bage/%E2%9A%BD+Blue+Lock-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=00B4D8" alt="BlueLock" />
  <img src="https://img.shields.io/badge/%F0%9F%94%B1+Chainsaw+Man-0a0a0f?style=for-the-badge&labelColor=0a0a0f&color=FF0000" alt="CSM" />
</div>

</div>

---

<!-- WAVE DIVIDER -->
<div class="wave-divider"></div>

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 1: SHADOW MONARCH CARD -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass particles" style="margin: 30px auto; max-width:700px;">

```
  ╔══════════════════════════════════════════════════════════════╗
  ║                                                              ║
  ║     ░██████╗░██████╗░██╗░░░██╗██╗██████╗░████████╗██╗░░░░░  ║
  ║     ██╔════╝██╔═══██╗██║░░░██║██║██╔══██╗╚══██╔══╝██║░░░░░  ║
  ║     ╚█████╗░██║██╗██║██║░░░██║██║██████╔╝░░░██║░░░██║░░░░░  ║
  ║     ░╚═══██╗╚██████╔╝██║░░░██║██║██╔══██╗░░░██║░░░██║░░░░░  ║
  ║     ██████╔╝░╚═██╔═╝░╚██████╔╝██║██║░░██║░░░██║░░░███████╗  ║
  ║     ╚═════╝░░░░╚═╝░░░░╚═════╝░╚═╝╚═╝░░╚═╝░░░╚═╝░░░╚══════╝ ║
  ║                                                              ║
  ╚══════════════════════════════════════════════════════════════╝
```

<div align="center">

| `FIELD` | `STATUS` |
|:---|:---|
| ⚔️ **CLASS** | `Shadow Monarch` |
| 📊 **LEVEL** | `∞ (Maxed)` |
| 🎮 **GUILD** | `Full Stack Developers` |
| 🏆 **RANK** | `S-Rank Hunter` |
| 💀 **DUNGEONS CLEARED** | `∞` |
| 🌑 **SHADOW ARMY** | `Deploying...` |

> *"I alone level up."* — **Sung Jin-Woo**

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 2: DOMAIN EXPANSION STATS -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border" style="margin: 30px auto; max-width:800px;">

### <span class="neon-purple">🔮 DOMAIN EXPANSION — 「 STAT REALM 」</span>

<div align="center">

<table>
<tr>
<td width="50%">
<div class="glass" style="margin:5px;">

**📊 Contribution Matrix**

<img src="https://github-readme-stats.vercel.app/api?username=chidvielasparepalli&show_icons=true&theme=tokyonight&bg_color=0a0a0f&hide_border=true&title_color=F72585&icon_color=7209B7&text_color=C9D1D9&border_color=F72585&include_all_commits=true&count_private=true" width="100%" />

</div>
</td>
<td width="50%">
<div class="glass-blue" style="margin:5px;">

**🔥 Chakra Streak**

<img src="https://github-readme-streak-stats.herokuapp.com/?user=chidvielasparepalli&theme=tokyonight&background=0a0a0f&hide_border=true&ring=F72585&fire=FFD700&currStreakLabel=F72585&sideLabels=C9D1D9&stroke=F72585" width="100%" />

</div>
</td>
</tr>
</table>

<div class="glass-purple" style="max-width:650px; margin:10px auto;">

**🧬 Technique Affinity — Top Languages**

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=chidvielasparepalli&layout=compact&theme=tokyonight&bg_color=0a0a0f&hide_border=true&title_color=F72585&text_color=C9D1D9&langs_count=8&border_color=7209B7" width="100%" />

</div>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 3: TECHNIQUE CARD -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass particles" style="margin: 30px auto; max-width:800px;">

### <span class="neon-pink">⚔️ TECHNIQUE: 「 FULL STACK MANIPULATION 」</span>

<div align="center" class="float">

#### ── 🖥️ FRONTEND JUTSU ──

<div style="margin: 10px 0;">
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB&color=F72585" alt="React" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white&color=F77F00" alt="Next.js" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white&color=4361EE" alt="TypeScript" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white&color=00B4D8" alt="Tailwind" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white&color=7209B7" alt="Redux" />
</div>

#### ── ⚙️ BACKEND NINJUTSU ──

<div style="margin: 10px 0;">
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white&color=4361EE" alt="Node.js" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white&color=00B4D8" alt="Python" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white&color=4361EE" alt="Django" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white&color=F72585" alt="PostgreSQL" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white&color=F72585" alt="GraphQL" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma" />
</div>

#### ── 🔧 DEPLOYMENT SENJUTSU ──

<div style="margin: 10px 0;">
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white&color=4361EE" alt="Docker" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white&color=F77F00" alt="AWS" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&color=F72585" alt="GitHub" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img class="skill-card hover-bounce" src="https://img.shields.io/badge/CI%2FCD-00B4D8?style=for-the-badge&logoColor=white&color=00B4D8" alt="CICD" />
</div>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 4: GITHUB CONTRIBUTION SNAKE -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass" style="margin: 30px auto; max-width:800px;">

### <span class="neon-blue">🐍 EVOLUTION SNAKE — ACTIVITY FEED</span>

<div align="center">

<img src="https://raw.githubusercontent.com/chidvielasparepalli/chidvielasparepalli/output/github-contribution-grid-snake-dark.svg" alt="Snake" width="100%" style="border-radius:12px;" />

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 5: ACHIEVEMENTS TABLE -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass-purple" style="margin: 30px auto; max-width:700px;">

### <span class="neon-pink">🏆 HUNTER ACHIEVEMENTS — 「 QUEST LOG 」</span>

<div align="center">

<table>
<tr>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

🗡️
<br><b>First Blood</b>
<br><code>First Commit</code>
<br>✅ Unlocked

</div>
</td>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

🐛
<br><b>Bug Slayer</b>
<br><code>Fixed 100 Bugs</code>
<br>✅ Unlocked

</div>
</td>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

🔥
<br><b>On Fire</b>
<br><code>100 Day Streak</code>
<br>🔄 In Progress

</div>
</td>
</tr>
<tr>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

👹
<br><b>Domain Expand</b>
<br><code>1000+ Commits</code>
<br>🔄 In Progress

</div>
</td>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

🏅
<br><b>S-Rank</b>
<br><code>100 Stars Earned</code>
<br>⏳ Locked

</div>
</td>
<td align="center" width="30%">
<div class="glass" style="padding:15px; margin:5px;">

🌑
<br><b>Shadow Army</b>
<br><code>50+ Repos</code>
<br>⏳ Locked

</div>
</td>
</tr>
</table>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 6: SKILL LEVEL BARS -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass" style="margin: 30px auto; max-width:700px;">

### <span class="neon-blue">📊 POWER LEVEL — 「 STAT DISTRIBUTION 」</span>

<div style="margin:8px 0;">
  <b style="color:#61DAFB; font-family:'Rajdhani';">⚛️ React ████████████████████░░░░ 85%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:85%; background: linear-gradient(90deg, #61DAFB, #F72585);"></div></div>
</div>

<div style="margin:8px 0;">
  <b style="color:#68A063; font-family:'Rajdhani';">🟢 Node.js ███████████████████░░░░░ 80%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:80%; background: linear-gradient(90deg, #68A063, #F72585);"></div></div>
</div>

<div style="margin:8px 0;">
  <b style="color:#3178C6; font-family:'Rajdhani';">🔵 TypeScript █████████████████░░░░░░░ 75%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:75%; background: linear-gradient(90deg, #3178C6, #4361EE);"></div></div>
</div>

<div style="margin:8px 0;">
  <b style="color:#3776AB; font-family:'Rajdhani';">🐍 Python ████████████████░░░░░░░░ 70%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:70%; background: linear-gradient(90deg, #3776AB, #00B4D8);"></div></div>
</div>

<div style="margin:8px 0;">
  <b style="color:#2496ED; font-family:'Rajdhani';">🐳 Docker ██████████████░░░░░░░░░░ 60%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:60%; background: linear-gradient(90deg, #2496ED, #4361EE);"></div></div>
</div>

<div style="margin:8px 0;">
  <b style="color:#F72585; font-family:'Rajdhani';">🌑 Shadow Arts █████████████████████░░░ 90%</b>
  <div class="progress-bar"><div class="progress-fill" style="width:90%; background: linear-gradient(90deg, #F72585, #7209B7);"></div></div>
</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 7: ANIME QUOTES -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass particles" style="margin: 30px auto; max-width:700px;">

### <span class="neon-purple">🎭 DOMAIN EXPANSION — 「 QUOTES REALM 」</span>

<div align="center" class="float">

<table>
<tr>
<td width="50%">
<div class="glass" style="padding:15px; margin:5px; border-left:3px solid #F72585;">

> *"Throughout heaven and earth, I alone am the honored one."*
> — **Gojo Satoru** 👹

</div>
</td>
<td width="50%">
<div class="glass" style="padding:15px; margin:5px; border-left:3px solid #7209B7;">

> *"I will become the strongest. I will kill all the monsters."*
> — **Sung Jin-Woo** 🌑

</div>
</td>
</tr>
<tr>
<td width="50%">
<div class="glass" style="padding:15px; margin:5px; border-left:3px solid #F77F00;">

> *"Those who break the rules are scum... but those who abandon their friends are worse than scum."*
> — **Kakashi Hatake** 🍥

</div>
</td>
<td width="50%">
<div class="glass" style="padding:15px; margin:5px; border-left:3px solid #00B4D8;">

> *"I will become the greatest striker the world has ever seen."*
> — **Isagi Yoichi** ⚽

</div>
</td>
</tr>
<tr>
<td colspan="2">
<div class="glass" style="padding:15px; margin:5px; border-left:3px solid #FF0000; text-align:center;">

> *"CONSUME."*
> — **Denji** 🔗

</div>
</td>
</tr>
</table>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 8: PINNED REPOS SHOWCASE -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass" style="margin: 30px auto; max-width:700px;">

### <span class="neon-pink">📦 SUMMONED ARTIFACTS — 「 PINNED REPOS 」</span>

<div align="center">

<a href="https://github.com/chidvielasparepalli?tab=repositories&sort=stargazers">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=chidvielasparepalli&repo=1&theme=tokyonight&bg_color=0a0a0f&hide_border=true&title_color=F72585&text_color=C9D1D9" style="margin:5px; border-radius:12px;" alt="Repo1" />
</a>
<a href="https://github.com/chidvielasparepalli?tab=repositories&sort=stargazers">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=chidvielasparepalli&repo=2&theme=tokyonight&bg_color=0a0a0f&hide_border=true&title_color=4361EE&text_color=C9D1D9" style="margin:5px; border-radius:12px;" alt="Repo2" />
</a>
<a href="https://github.com/chidvielasparepalli?tab=repositories&sort=stargazers">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=chidvielasparepalli&repo=3&theme=tokyonight&bg_color=0a0a0f&hide_border=true&title_color=7209B7&text_color=C9D1D9" style="margin:5px; border-radius:12px;" alt="Repo3" />
</a>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 9: CURRENT ANIME WATCHLIST -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass" style="margin: 30px auto; max-width:700px;">

### <span class="neon-blue">📺 CURRENT ARC — 「 ANIME LOG 」</span>

<div align="center" class="float">

| # | Anime | Status | Rating |
|:---:|:---:|:---:|:---:|
| 1 | ⚔️ **Solo Leveling S2** | 🟢 Watching | ⭐⭐⭐⭐⭐ |
| 2 | 👹 **Jujutsu Kaisen** | 🟢 Watching | ⭐⭐⭐⭐⭐ |
| 3 | 🔗 **Chainsaw Man** | 🟢 Watching | ⭐⭐⭐⭐⭐ |
| 4 | ⚽ **Blue Lock** | 🟢 Watching | ⭐⭐⭐⭐⭐ |
| 5 | 🍥 **Naruto Shippuden** | 🟡 Rewatching | ⭐⭐⭐⭐⭐ |

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- SECTION 10: CONNECT / SOCIAL -->
<!-- ═══════════════════════════════════════ -->
<div class="glow-border glass particles" style="margin: 30px auto; max-width:600px;">

### <span class="neon-pink">📡 COMMUNICATION CHANNEL — 「 SUMMON 」</span>

<div align="center" style="margin: 15px 0;">

<table>
<tr>
<td align="center">
<a href="https://github.com/chidvielasparepalli">
<div class="glass hover-bounce" style="padding:15px 25px; border-radius:12px; display:inline-block;">
  <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&color=F72585" alt="GitHub" />
</div>
</a>
</td>
<td align="center">
<a href="#">
<div class="glass hover-bounce" style="padding:15px 25px; border-radius:12px; display:inline-block;">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&color=4361EE" alt="LinkedIn" />
</div>
</a>
</td>
</tr>
<tr>
<td align="center">
<a href="#">
<div class="glass hover-bounce" style="padding:15px 25px; border-radius:12px; display:inline-block;">
  <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white&color=00B4D8" alt="Twitter" />
</div>
</a>
</td>
<td align="center">
<a href="#">
<div class="glass hover-bounce" style="padding:15px 25px; border-radius:12px; display:inline-block;">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white&color=F77F00" alt="Email" />
</div>
</a>
</td>
</tr>
</table>

</div>

</div>

---

<!-- ═══════════════════════════════════════ -->
<!-- FOOTER -->
<!-- ═══════════════════════════════════════ -->
<div class="wave-divider"></div>

<div align="center" style="margin: 30px 0;">

<div class="glass" style="display:inline-block; padding:20px 40px; border-radius:16px; max-width:600px;">

### <span class="glitch" style="font-family:'Orbitron',sans-serif;">🌑 ARISE 🌑</div>

*"Even if death approaches, I will never stop evolving."*

<br>

<img src="https://komarev.com/ghpvc/?username=chidvielasparepalli&color=F72585&style=flat-square&label=SHADOW+MONARCH+VISITORS&labelColor=0a0a0f" alt="Visitors" />

<br><br>

<img src="https://raw.githubusercontent.com/Plarameo/animated-github-svg/main/line_animation.svg" width="100%" />

*Made with ⚔️ by **Chidviela Sparepalli** — The Shadow Monarch*

</div>

</div>
