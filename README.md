<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<base href="./">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="dns-prefetch" href="https://cdn.jsdelivr.net">
<link rel="dns-prefetch" href="https://cdnjs.cloudflare.com">
<title>Muhammad Numan - Senior Full Stack Developer</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Pacifico&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg-main: #0a0e1a;
    --bg-card: #0f1526;
    --bg-section: #111827;
    --purple: #7c3aed;
    --purple-light: #a855f7;
    --cyan: #06b6d4;
    --yellow: #f59e0b;
    --green: #10b981;
    --pink: #ec4899;
    --text: #e2e8f0;
    --text-muted: #94a3b8;
    --border: #1e2a3a;
    --gradient: linear-gradient(135deg, #7c3aed, #06b6d4);
  }

  body {
    font-family: 'Poppins', sans-serif;
    background: #060b18;
    color: var(--text);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 20px;
  }

  .card {
    background: var(--bg-card);
    border: 1px solid #1a2540;
    border-radius: 16px;
    width: 100%;
    max-width: 860px;
    overflow: hidden;
    box-shadow: 0 0 60px rgba(124, 58, 237, 0.15), 0 0 120px rgba(6, 182, 212, 0.05);
  }

  /* ── HERO ── */
  .hero {
    background: linear-gradient(135deg, #0a0e1a 0%, #0f1526 50%, #0d1220 100%);
    padding: 28px 30px 20px;
    position: relative;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 16px;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(124,58,237,0.12) 0%, transparent 70%);
    border-radius: 50%;
  }
  .hero-left { flex: 1; z-index: 1; }
  .hero-greeting {
    font-family: 'Pacifico', cursive;
    font-size: 18px;
    color: var(--text-muted);
    margin-bottom: 4px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .hero-greeting .wave { font-size: 20px; }
  .hero-name {
    font-size: clamp(28px, 5vw, 42px);
    font-weight: 800;
    line-height: 1.1;
    margin-bottom: 10px;
  }
  .hero-name span { color: var(--purple-light); }
  .hero-badge {
    display: inline-block;
    background: var(--gradient);
    border-radius: 6px;
    padding: 5px 16px;
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 10px;
  }
  .hero-tags {
    font-size: 11px;
    color: var(--text-muted);
    margin-bottom: 12px;
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
    align-items: center;
  }
  .hero-tags span { display: flex; align-items: center; gap: 4px; }
  .hero-tags .dot { width: 4px; height: 4px; background: var(--text-muted); border-radius: 50%; }
  .hero-quote {
    background: rgba(255,255,255,0.04);
    border-left: 2px solid var(--purple);
    border-radius: 6px;
    padding: 10px 14px;
    font-size: 12px;
    color: var(--text-muted);
    max-width: 400px;
    position: relative;
  }
  .hero-quote .qq { color: var(--purple-light); font-size: 18px; font-weight: 700; line-height: 1; }
  .hero-quote .qq.left { margin-right: 4px; }
  .hero-quote .qq.right { margin-left: 4px; }

  .hero-avatar {
    width: 180px;
    height: 180px;
    flex-shrink: 0;
    position: relative;
    z-index: 1;
  }
  .hero-avatar img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid rgba(124,58,237,0.4);
  }
  /* Glow behind avatar */
  .avatar-glow {
    position: absolute;
    inset: -20px;
    background: radial-gradient(circle, rgba(248,220,100,0.25) 0%, rgba(124,58,237,0.15) 40%, transparent 70%);
    border-radius: 50%;
    z-index: 0;
  }

  /* ── SOCIAL LINKS ── */
  .social-bar {
    display: flex;
    gap: 1px;
    background: var(--border);
    border-top: 1px solid var(--border);
  }
  .social-item {
    flex: 1;
    background: var(--bg-section);
    padding: 10px 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3px;
    text-decoration: none;
    transition: background 0.2s;
    border-right: 1px solid var(--border);
  }
  .social-item:last-child { border-right: none; }
  .social-item:hover { background: #151e30; }
  .social-icon {
    width: 28px; height: 28px;
    border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px; color: #fff;
  }
  .si-portfolio { background: #1a3a5c; }
  .si-github    { background: #24292e; }
  .si-linkedin  { background: #0a66c2; }
  .si-email     { background: #c0392b; }
  .si-whatsapp  { background: #25d366; }
  .social-label { font-size: 11px; font-weight: 600; color: var(--text); }
  .social-val   { font-size: 9px; color: var(--text-muted); }

  /* ── BODY GRID ── */
  .body-grid {
    display: grid;
    grid-template-columns: 220px 1fr;
    gap: 1px;
    background: var(--border);
  }

  .left-col { background: var(--bg-card); display: flex; flex-direction: column; gap: 1px; }
  .right-col { background: var(--border); display: flex; flex-direction: column; gap: 1px; }

  .section {
    background: var(--bg-section);
    padding: 16px;
  }

  .section-title {
    font-size: 12px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 7px;
    color: var(--text);
  }
  .section-title i { color: var(--purple-light); font-size: 14px; }

  /* ABOUT ME */
  .about-list { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .about-list li {
    display: flex; align-items: flex-start; gap: 8px;
    font-size: 11px; color: var(--text-muted); line-height: 1.4;
  }
  .about-list li i { color: var(--purple-light); font-size: 12px; margin-top: 1px; flex-shrink: 0; }

  /* WHAT I DO */
  .whatido-list { list-style: none; display: flex; flex-direction: column; gap: 7px; }
  .whatido-list li {
    display: flex; align-items: center; gap: 8px;
    font-size: 11px; color: var(--text-muted);
  }
  .whatido-list li i { color: var(--cyan); font-size: 11px; flex-shrink: 0; }

  /* GITHUB STATS */
  .gh-stats { display: flex; flex-direction: column; gap: 6px; }
  .gh-stat-row {
    display: flex; justify-content: space-between; align-items: center;
    font-size: 11px;
  }
  .gh-stat-row .stat-label { display: flex; align-items: center; gap: 6px; color: var(--text-muted); }
  .gh-stat-row .stat-label i { font-size: 11px; color: var(--text-muted); }
  .gh-stat-row .stat-val { font-weight: 700; color: var(--text); }

  /* TECH STACK */
  .tech-table { width: 100%; border-collapse: collapse; }
  .tech-table tr + tr td { padding-top: 12px; }
  .tech-row-label {
    font-size: 11px; font-weight: 700; color: var(--text);
    padding-right: 12px; white-space: nowrap; vertical-align: middle;
    width: 80px;
  }
  .tech-icons { display: flex; flex-wrap: wrap; gap: 10px; align-items: center; }
  .tech-icon {
    display: flex; flex-direction: column; align-items: center; gap: 4px;
    font-size: 9px; color: var(--text-muted);
  }
  .tech-icon img { width: 28px; height: 28px; object-fit: contain; }

  /* PROFESSIONAL SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
  }
  .skill-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 8px 10px;
    display: flex; flex-direction: column; align-items: center; gap: 6px;
    text-align: center;
  }
  .skill-card-icon { font-size: 22px; }
  .skill-card-name { font-size: 10px; font-weight: 600; line-height: 1.3; }
  .skill-bar-wrap { width: 100%; background: rgba(255,255,255,0.08); border-radius: 4px; height: 4px; }
  .skill-bar { height: 4px; border-radius: 4px; background: var(--gradient); }
  .skill-pct { font-size: 10px; font-weight: 700; color: var(--purple-light); }

  /* BOTTOM ROW */
  .bottom-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1px;
    background: var(--border);
  }
  .bottom-section { background: var(--bg-section); padding: 14px; }

  /* STREAK */
  .streak-ring {
    width: 80px; height: 80px;
    border-radius: 50%;
    border: 4px solid transparent;
    background: linear-gradient(var(--bg-section), var(--bg-section)) padding-box,
                conic-gradient(var(--purple-light) 0% 75%, rgba(255,255,255,0.1) 75% 100%) border-box;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    margin: 8px auto 12px;
  }
  .streak-days { font-size: 22px; font-weight: 800; color: var(--text); line-height: 1; }
  .streak-label { font-size: 9px; color: var(--text-muted); }
  .streak-stats { display: flex; flex-direction: column; gap: 6px; }
  .streak-row { font-size: 11px; display: flex; flex-direction: column; gap: 1px; }
  .streak-row .s-label { color: var(--text-muted); font-size: 10px; }
  .streak-row .s-val { font-weight: 700; color: var(--green); }
  .streak-row .s-val.orange { color: var(--yellow); }

  /* TOP LANGUAGES */
  .lang-donut-wrap { display: flex; justify-content: center; margin: 6px 0 10px; }
  .lang-donut {
    width: 80px; height: 80px;
    border-radius: 50%;
    background: conic-gradient(
      #f1e05a 0% 35.3%,
      #3178c6 35.3% 58.4%,
      #3572a5 58.4% 74.4%,
      #8892be 74.4% 86.6%,
      #6e6e6e 86.6% 100%
    );
    position: relative;
  }
  .lang-donut::after {
    content: '';
    position: absolute;
    inset: 18px;
    background: var(--bg-section);
    border-radius: 50%;
  }
  .lang-list { display: flex; flex-direction: column; gap: 4px; }
  .lang-item { display: flex; align-items: center; gap: 6px; font-size: 10px; color: var(--text-muted); }
  .lang-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  /* TROPHIES */
  .trophies-grid { display: flex; flex-wrap: wrap; gap: 6px; justify-content: center; margin: 6px 0; }
  .trophy {
    width: 40px; height: 40px;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px;
  }
  .trophy-more { font-size: 10px; color: var(--text-muted); text-align: center; }
  .trophy-cta { font-size: 11px; font-weight: 600; color: var(--yellow); text-align: center; margin-top: 4px; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 700px) {
    body { padding: 10px; }
    .hero { flex-direction: column-reverse; align-items: center; padding: 20px; }
    .hero-avatar { width: 130px; height: 130px; }
    .body-grid { grid-template-columns: 1fr; }
    .skills-grid { grid-template-columns: repeat(2, 1fr); }
    .bottom-grid { grid-template-columns: 1fr; }
    .social-bar { flex-wrap: wrap; }
    .social-item { min-width: calc(33.33% - 1px); }
  }
  @media (max-width: 480px) {
    .skills-grid { grid-template-columns: repeat(2, 1fr); }
    .tech-icons { gap: 8px; }
    .tech-icon img { width: 22px; height: 22px; }
    .social-item { min-width: calc(50% - 1px); }
  }
</style>
</head>
<body>

<div class="card">

  <!-- ── HERO ── -->
  <div class="hero">
    <div class="hero-left">
      <div class="hero-greeting">
        <span style="font-family:'Pacifico',cursive;font-size:17px;color:#94a3b8;">Hi</span>
        <span class="wave">👋</span>
        <span style="font-family:'Pacifico',cursive;font-size:17px;color:#94a3b8;">, I'm</span>
      </div>
      <div class="hero-name">Muhammad <span>Numan</span></div>
      <div class="hero-badge">Senior Full Stack Developer &amp; Team Lead</div>
      <div class="hero-tags">
        <span>MERN Stack Developer</span>
        <span class="dot"></span>
        <span>LAMP Stack Specialist</span>
        <span class="dot"></span>
        <span>Python Developer</span>
        <span class="dot"></span>
        <span>AI Engineer</span>
        <span class="dot"></span>
        <span>Chatbot Developer</span>
      </div>
      <div class="hero-quote">
        <span class="qq left">"</span>Building scalable, efficient and intelligent digital solutions that empower businesses and users.<span class="qq right">"</span>
      </div>
    </div>
    <div class="hero-avatar" style="position:relative;">
      <div class="avatar-glow"></div>
      <img src="https://i.imgur.com/2X8Nm9b.png"
           onerror="this.onerror=null;this.src='https://api.dicebear.com/7.x/avataaars/svg?seed=MuhammadNuman&backgroundColor=b6e3f4&hair=short&eyes=default&mouth=smile'"
           alt="Muhammad Numan" style="position:relative;z-index:1;">
    </div>
  </div>

  <!-- ── SOCIAL BAR ── -->
  <div class="social-bar">
    <a href="https://muhammadnouman.site/" class="social-item" target="_blank" rel="noopener noreferrer">
      <div class="social-icon si-portfolio"><i class="fas fa-globe"></i></div>
      <div class="social-label">Portfolio</div>
      <div class="social-val">muhammadnouman.site</div>
    </a>
    <a href="https://github.com/muhammadnuman-eng" class="social-item" target="_blank" rel="noopener noreferrer">
      <div class="social-icon si-github"><i class="fab fa-github"></i></div>
      <div class="social-label">GitHub</div>
      <div class="social-val">muhammadnuman-eng</div>
    </a>
    <a href="https://www.linkedin.com/in/nomanfull-stack-developer/" class="social-item" target="_blank" rel="noopener noreferrer">
      <div class="social-icon si-linkedin"><i class="fab fa-linkedin-in"></i></div>
      <div class="social-label">LinkedIn</div>
      <div class="social-val">nomanfull-stack-developer</div>
    </a>
    <a href="mailto:nomandev304@gmail.com" class="social-item">
      <div class="social-icon si-email"><i class="fas fa-envelope"></i></div>
      <div class="social-label">Email</div>
      <div class="social-val">nomandev304@gmail.com</div>
    </a>
    <a href="https://wa.me/923120630864" class="social-item" target="_blank" rel="noopener noreferrer">
      <div class="social-icon si-whatsapp"><i class="fab fa-whatsapp"></i></div>
      <div class="social-label">WhatsApp</div>
      <div class="social-val">+92 312 0630864</div>
    </a>
  </div>

  <!-- ── BODY GRID ── -->
  <div class="body-grid">

    <!-- LEFT COLUMN -->
    <div class="left-col">

      <!-- ABOUT ME -->
      <div class="section">
        <div class="section-title"><i class="fas fa-user"></i> ABOUT ME</div>
        <ul class="about-list">
          <li><i class="fas fa-briefcase"></i> Senior Full Stack Developer &amp; Team Lead</li>
          <li><i class="fas fa-check-circle"></i> 7+ Projects Completed</li>
          <li><i class="fas fa-layer-group"></i> Expert in MERN &amp; LAMP Stacks</li>
          <li><i class="fas fa-robot"></i> Python Developer &amp; AI Enthusiast</li>
          <li><i class="fas fa-cloud"></i> Chatbot &amp; SaaS Solution Architect</li>
          <li><i class="fas fa-heart"></i> Passionate about clean code, automation &amp; innovation</li>
        </ul>
      </div>

      <!-- WHAT I DO -->
      <div class="section">
        <div class="section-title"><i class="fas fa-rocket"></i> WHAT I DO</div>
        <ul class="whatido-list">
          <li><i class="fas fa-code"></i> Full Stack Web Development</li>
          <li><i class="fas fa-robot"></i> AI Chatbots &amp; Automation</li>
          <li><i class="fas fa-plug"></i> RESTful API Development</li>
          <li><i class="fas fa-database"></i> Database Design &amp; Optimization</li>
          <li><i class="fas fa-users"></i> Team Management &amp; Leadership</li>
          <li><i class="fas fa-bug"></i> Problem Solving &amp; Debugging</li>
        </ul>
      </div>

      <!-- GITHUB STATS -->
      <div class="section">
        <div class="section-title"><i class="fab fa-github"></i> GITHUB STATS</div>
        <div class="gh-stats">
          <div class="gh-stat-row">
            <span class="stat-label"><i class="fas fa-folder"></i> Repositories</span>
            <span class="stat-val">71</span>
          </div>
          <div class="gh-stat-row">
            <span class="stat-label"><i class="fas fa-plus-circle"></i> Contributions</span>
            <span class="stat-val">670+</span>
          </div>
          <div class="gh-stat-row">
            <span class="stat-label"><i class="fas fa-code-commit"></i> Commits</span>
            <span class="stat-val">670+</span>
          </div>
          <div class="gh-stat-row">
            <span class="stat-label"><i class="fas fa-star"></i> Stars</span>
            <span class="stat-val">15</span>
          </div>
          <div class="gh-stat-row">
            <span class="stat-label"><i class="fas fa-code-pull-request"></i> Pull Requests</span>
            <span class="stat-val">25</span>
          </div>
        </div>
      </div>

    </div><!-- /left-col -->

    <!-- RIGHT COLUMN -->
    <div class="right-col">

      <!-- TECH STACK -->
      <div class="section">
        <div class="section-title"><i class="fas fa-cogs"></i> TECH STACK</div>
        <table class="tech-table">
          <tr>
            <td class="tech-row-label">FRONTEND</td>
            <td>
              <div class="tech-icons">
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React"><span>React</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" alt="Next.js" style="filter:invert(1)"><span>Next.js</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JS"><span>JavaScript</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TS"><span>TypeScript</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5"><span>HTML5</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3"><span>CSS3</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" alt="Tailwind"><span>Tailwind CSS</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" alt="Bootstrap"><span>Bootstrap</span></div>
              </div>
            </td>
          </tr>
          <tr>
            <td class="tech-row-label">BACKEND</td>
            <td>
              <div class="tech-icons">
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js"><span>Node.js</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" alt="Express" style="filter:invert(1)"><span>Express.js</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="PHP"><span>PHP</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" alt="Laravel"><span>Laravel</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python"><span>Python</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg" alt="FastAPI"><span>FastAPI</span></div>
              </div>
            </td>
          </tr>
          <tr>
            <td class="tech-row-label">DATABASE</td>
            <td>
              <div class="tech-icons">
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB"><span>MongoDB</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" alt="MySQL"><span>MySQL</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" alt="Firebase"><span>Firebase</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" alt="Redis"><span>Redis</span></div>
              </div>
            </td>
          </tr>
          <tr>
            <td class="tech-row-label" style="font-size:10px;">TOOLS &amp; DEVOPS</td>
            <td>
              <div class="tech-icons">
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git"><span>Git</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="filter:invert(1)"><span>GitHub</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt="Docker"><span>Docker</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" alt="Linux"><span>Linux</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="VS Code"><span>VS Code</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg" alt="Postman"><span>Postman</span></div>
                <div class="tech-icon"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" alt="Figma"><span>Figma</span></div>
              </div>
            </td>
          </tr>
        </table>
      </div>

      <!-- PROFESSIONAL SKILLS -->
      <div class="section">
        <div class="section-title"><i class="fas fa-chart-bar"></i> PROFESSIONAL SKILLS</div>
        <div class="skills-grid">
          <div class="skill-card">
            <div class="skill-card-icon">🖥️</div>
            <div class="skill-card-name">Web Development</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:95%"></div></div>
            <div class="skill-pct">95%</div>
          </div>
          <div class="skill-card">
            <div class="skill-card-icon">🤖</div>
            <div class="skill-card-name">AI Chatbot Development</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:90%"></div></div>
            <div class="skill-pct">90%</div>
          </div>
          <div class="skill-card">
            <div class="skill-card-icon" style="background:linear-gradient(135deg,#7c3aed,#06b6d4);-webkit-background-clip:text;-webkit-text-fill-color:transparent;">SaaS</div>
            <div class="skill-card-name">SaaS Development</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:90%"></div></div>
            <div class="skill-pct">90%</div>
          </div>
          <div class="skill-card">
            <div class="skill-card-icon" style="font-family:monospace;font-weight:800;font-size:14px;color:#06b6d4;">API</div>
            <div class="skill-card-name">API Development</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:95%"></div></div>
            <div class="skill-pct">95%</div>
          </div>
          <div class="skill-card">
            <div class="skill-card-icon">🗄️</div>
            <div class="skill-card-name">Database Management</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:90%"></div></div>
            <div class="skill-pct">90%</div>
          </div>
          <div class="skill-card">
            <div class="skill-card-icon">👥</div>
            <div class="skill-card-name">Team Leadership</div>
            <div class="skill-bar-wrap"><div class="skill-bar" style="width:95%"></div></div>
            <div class="skill-pct">95%</div>
          </div>
        </div>
      </div>

    </div><!-- /right-col -->
  </div><!-- /body-grid -->

  <!-- ── BOTTOM ROW ── -->
  <div class="bottom-grid">

    <!-- STREAK STATS -->
    <div class="bottom-section">
      <div class="section-title"><i class="fas fa-fire" style="color:#f59e0b;"></i> STREAK STATS</div>
      <div class="streak-ring">
        <div class="streak-days">21</div>
        <div class="streak-label">Days</div>
      </div>
      <div class="streak-stats">
        <div class="streak-row">
          <div class="s-label">Current Streak</div>
          <div class="s-val orange">21 days</div>
        </div>
        <div class="streak-row">
          <div class="s-label">Longest Streak</div>
          <div class="s-val">45 days</div>
        </div>
      </div>
    </div>

    <!-- TOP LANGUAGES -->
    <div class="bottom-section">
      <div class="section-title"><i class="fas fa-chart-pie" style="color:#10b981;"></i> TOP LANGUAGES</div>
      <div class="lang-donut-wrap">
        <div class="lang-donut"></div>
      </div>
      <div class="lang-list">
        <div class="lang-item"><div class="lang-dot" style="background:#f1e05a;"></div> JavaScript 35.3%</div>
        <div class="lang-item"><div class="lang-dot" style="background:#3178c6;"></div> TypeScript 23.1%</div>
        <div class="lang-item"><div class="lang-dot" style="background:#3572a5;"></div> Python 16%</div>
        <div class="lang-item"><div class="lang-dot" style="background:#8892be;"></div> PHP 12.6%</div>
        <div class="lang-item"><div class="lang-dot" style="background:#6e6e6e;"></div> Others 12.2%</div>
      </div>
    </div>

    <!-- GITHUB TROPHIES -->
    <div class="bottom-section">
      <div class="section-title"><i class="fas fa-trophy" style="color:#f59e0b;"></i> GITHUB TROPHIES</div>
      <div class="trophies-grid">
        <div class="trophy">🏆</div>
        <div class="trophy">🥇</div>
        <div class="trophy">⭐</div>
        <div class="trophy">🔥</div>
        <div class="trophy">💎</div>
        <div class="trophy">🚀</div>
        <div class="trophy">⚡</div>
        <div class="trophy">🎯</div>
      </div>
      <div class="trophy-more">And More...</div>
      <div class="trophy-cta">Keep Pushing Limits! 🚀</div>
    </div>

  </div><!-- /bottom-grid -->

</div><!-- /card -->

</body>
</html>
