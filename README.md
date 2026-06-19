<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>getAOSP — GitHub Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Inter:wght@300;400;500;600&display=swap');

  :root {
    --bg:        #0a0c10;
    --surface:   #0f1117;
    --border:    #1e2330;
    --green:     #3dffa0;
    --green-dim: #1a7a4a;
    --blue:      #58a6ff;
    --purple:    #bc8cff;
    --text:      #c9d1d9;
    --muted:     #484f58;
    --white:     #f0f6fc;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
    padding: 40px 20px;
  }

  .card {
    max-width: 780px;
    margin: 0 auto;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  /* ─── HERO ─── */
  .hero {
    padding: 40px 40px 32px;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 280px; height: 280px;
    background: radial-gradient(circle, rgba(61,255,160,.10) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-top {
    display: flex;
    align-items: flex-start;
    gap: 24px;
    margin-bottom: 24px;
  }

  .avatar {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--green-dim), var(--green));
    display: flex; align-items: center; justify-content: center;
    font-family: 'JetBrains Mono', monospace;
    font-size: 22px;
    font-weight: 700;
    color: #0a0c10;
    flex-shrink: 0;
    border: 2px solid var(--green-dim);
  }

  .hero-name {
    font-family: 'JetBrains Mono', monospace;
    font-size: 26px;
    font-weight: 700;
    color: var(--white);
    letter-spacing: -0.5px;
    line-height: 1.1;
  }

  .hero-name span { color: var(--green); }

  .hero-role {
    font-size: 13px;
    color: var(--muted);
    margin-top: 6px;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: .5px;
  }

  .hero-bio {
    font-size: 14.5px;
    line-height: 1.7;
    color: var(--text);
    max-width: 580px;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 20px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 11.5px;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 600;
    letter-spacing: .3px;
    border: 1px solid;
  }

  .badge-green  { color: var(--green);  border-color: var(--green-dim);  background: rgba(61,255,160,.06); }
  .badge-blue   { color: var(--blue);   border-color: #1b3a5c;           background: rgba(88,166,255,.06); }
  .badge-purple { color: var(--purple); border-color: #3d2b6b;           background: rgba(188,140,255,.06); }

  .dot { width: 6px; height: 6px; border-radius: 50%; background: currentColor; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

  /* ─── SECTIONS ─── */
  .section {
    padding: 28px 40px;
    border-bottom: 1px solid var(--border);
  }
  .section:last-child { border-bottom: none; }

  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    font-weight: 600;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 18px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ─── CURRENT PROJECT ─── */
  .project-card {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px 24px;
    position: relative;
    overflow: hidden;
  }

  .project-card::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--green);
    border-radius: 3px 0 0 3px;
  }

  .project-name {
    font-family: 'JetBrains Mono', monospace;
    font-size: 15px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .wip-tag {
    font-size: 9px;
    padding: 2px 8px;
    border-radius: 3px;
    background: rgba(61,255,160,.12);
    color: var(--green);
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .project-desc {
    font-size: 13.5px;
    color: var(--text);
    line-height: 1.65;
    margin-bottom: 14px;
  }

  .tag-row { display: flex; flex-wrap: wrap; gap: 6px; }

  .tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10.5px;
    padding: 3px 8px;
    border-radius: 4px;
    color: var(--blue);
    background: rgba(88,166,255,.08);
    border: 1px solid rgba(88,166,255,.2);
  }

  /* ─── DEVICE HISTORY ─── */
  .device-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 10px;
  }

  .device-item {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 7px;
    padding: 12px 14px;
    transition: border-color .2s;
  }

  .device-item:hover { border-color: var(--muted); }

  .device-vendor {
    font-size: 10px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 4px;
  }

  .device-name {
    font-size: 13px;
    font-weight: 500;
    color: var(--white);
  }

  /* ─── TECH STACK ─── */
  .stack-group { margin-bottom: 18px; }
  .stack-group:last-child { margin-bottom: 0; }

  .stack-group-title {
    font-size: 10.5px;
    font-family: 'JetBrains Mono', monospace;
    color: var(--purple);
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .pill-row { display: flex; flex-wrap: wrap; gap: 7px; }

  .pill {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11.5px;
    padding: 5px 12px;
    border-radius: 5px;
    color: var(--text);
    background: rgba(255,255,255,.04);
    border: 1px solid var(--border);
    transition: background .15s;
  }

  .pill:hover { background: rgba(255,255,255,.08); }

  /* ─── STATS ─── */
  .stats-img {
    width: 100%;
    border-radius: 8px;
    border: 1px solid var(--border);
    display: block;
  }

  /* ─── FOOTER ─── */
  .footer {
    padding: 20px 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
  }

  .footer-note {
    font-size: 12px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
  }

  .footer-note span { color: var(--green); }

  .links { display: flex; gap: 14px; }

  .link {
    font-size: 12px;
    font-family: 'JetBrains Mono', monospace;
    color: var(--blue);
    text-decoration: none;
    opacity: .8;
    transition: opacity .15s;
  }

  .link:hover { opacity: 1; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 560px) {
    .hero, .section, .footer { padding-left: 24px; padding-right: 24px; }
    .hero-top { flex-direction: column; gap: 16px; }
    .hero-name { font-size: 21px; }
    .device-grid { grid-template-columns: repeat(2, 1fr); }
  }
</style>
</head>
<body>

<div class="card">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-top">
      <div class="avatar">gA</div>
      <div>
        <div class="hero-name"><span>get</span>AOSP</div>
        <div class="hero-role">// Android Developer · Custom ROM Maintainer</div>
      </div>
    </div>

    <p class="hero-bio">
      Building clean, bloat-free Android experiences — from bare AOSP bring-ups to LineageOS
      device trees. Obsessed with the gap between broken vendor sources and a smooth daily
      driver. I write the code that bridges it.
    </p>

    <div class="badge-row">
      <span class="badge badge-green"><span class="dot"></span>Active — POCO F7 Ultra</span>
      <span class="badge badge-blue">LineageOS 23.2 · Android 16</span>
      <span class="badge badge-purple">Linux · AOSP · Kernel</span>
    </div>
  </div>

  <!-- CURRENT PROJECT -->
  <div class="section">
    <div class="section-label">Current Focus</div>

    <div class="project-card">
      <div class="project-name">
        POCO F7 Ultra <code style="font-size:12px;color:var(--muted)">(miro)</code>
        <span class="wip-tag">In Progress</span>
      </div>
      <p class="project-desc">
        Bringing up LineageOS 23.2 on Android 16 with custom hardware baseline
        implementations — sidestepping broken vendor sources entirely. Heavy focus on HAL
        compatibility, kernel patches, and making the camera stack not cry.
      </p>
      <div class="tag-row">
        <span class="tag">LineageOS 23.2</span>
        <span class="tag">Android 16</span>
        <span class="tag">custom HALs</span>
        <span class="tag">vendor bypass</span>
        <span class="tag">Snapdragon</span>
      </div>
    </div>
  </div>

  <!-- DEVICE HISTORY -->
  <div class="section">
    <div class="section-label">Device History</div>
    <div class="device-grid">
      <div class="device-item"><div class="device-vendor">POCO</div><div class="device-name">F7 Ultra</div></div>
      <div class="device-item"><div class="device-vendor">POCO</div><div class="device-name">F3</div></div>
      <div class="device-item"><div class="device-vendor">POCO</div><div class="device-name">F1</div></div>
      <div class="device-item"><div class="device-vendor">Xiaomi</div><div class="device-name">11T Pro</div></div>
      <div class="device-item"><div class="device-vendor">Redmi</div><div class="device-name">Note 9 Pro</div></div>
      <div class="device-item"><div class="device-vendor">Samsung</div><div class="device-name">Galaxy A51</div></div>
      <div class="device-item"><div class="device-vendor">Samsung</div><div class="device-name">Galaxy S2 ✦</div></div>
      <div class="device-item"><div class="device-vendor">Google</div><div class="device-name">Nexus 5X</div></div>
      <div class="device-item"><div class="device-vendor">Motorola</div><div class="device-name">Moto X Play</div></div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-label">Tech Stack</div>

    <div class="stack-group">
      <div class="stack-group-title">OS / Platform</div>
      <div class="pill-row">
        <span class="pill">AOSP</span>
        <span class="pill">LineageOS</span>
        <span class="pill">Kernel Compilation</span>
        <span class="pill">HAL Development</span>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-title">Languages</div>
      <div class="pill-row">
        <span class="pill">C</span>
        <span class="pill">C++</span>
        <span class="pill">Java</span>
        <span class="pill">Kotlin</span>
        <span class="pill">Bash / Shell</span>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-title">Environment</div>
      <div class="pill-row">
        <span class="pill">Ubuntu / Debian</span>
        <span class="pill">Termux</span>
        <span class="pill">Git</span>
        <span class="pill">ADB / Fastboot</span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-label">GitHub Stats</div>
    <img
      class="stats-img"
      src="https://github-readme-stats.vercel.app/api?username=getAOSP&show_icons=true&theme=dark&bg_color=0d1117&border_color=1e2330&title_color=3dffa0&icon_color=58a6ff&text_color=c9d1d9&hide_border=false"
      alt="getAOSP GitHub Stats"
    />
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span class="footer-note">// explore repos · report bugs in issue trackers · <span>PRs welcome</span></span>
    <div class="links">
      <a class="link" href="https://github.com/getAOSP">github.com/getAOSP</a>
    </div>
  </div>

</div>
</body>
</html>
