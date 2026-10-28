<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ömer Denizhan Profile</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700&family=Figtree:wght@400;500;600&display=swap" rel="stylesheet">
<style>
/* Layout: one centered column of frosted glass panels floating over a dark aurora mesh. */
:root {
  --bg: #0a0d1f;
  --ink: #f2f4ff;
  --ink-soft: rgba(242, 244, 255, 0.78);
  --aurora-violet: #7b4dff;
  --aurora-rose: #ff4d8d;
  --aurora-cyan: #22d3ee;
  --aurora-amber: #ffb84d;
  --glass: rgba(255, 255, 255, 0.07);
  --glass-strong: rgba(255, 255, 255, 0.12);
  --glass-edge: rgba(255, 255, 255, 0.2);
  --glass-shine: rgba(255, 255, 255, 0.35);
  --shadow: 0 18px 50px rgba(3, 4, 18, 0.45);
  --font-display: "Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
  --font-body: "Figtree", "Segoe UI", system-ui, sans-serif;
  color-scheme: dark;
}

*, *::before, *::after { box-sizing: border-box; }

html { background: var(--bg); }

body {
  margin: 0;
  min-height: 100%;
  background: var(--bg);
  color: var(--ink);
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.6;
  padding-block: 40px 56px;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  position: relative;
  overflow-x: hidden;
}

/* Aurora backdrop: the glass needs colour behind it to refract. */
.aurora {
  position: fixed;
  inset: 0;
  z-index: 0;
  overflow: hidden;
  pointer-events: none;
}
.aurora span {
  position: absolute;
  border-radius: 50%;
  filter: blur(90px);
  opacity: 0.55;
}
.aurora .o1 { width: 52vmax; height: 52vmax; left: -14vmax; top: -16vmax; background: var(--aurora-violet); }
.aurora .o2 { width: 44vmax; height: 44vmax; right: -12vmax; top: 18vh; background: var(--aurora-rose); opacity: 0.4; }
.aurora .o3 { width: 48vmax; height: 48vmax; left: 12vw; bottom: -22vmax; background: var(--aurora-cyan); opacity: 0.38; }
.aurora .o4 { width: 26vmax; height: 26vmax; right: 14vw; bottom: 8vh; background: var(--aurora-amber); opacity: 0.22; }

.page {
  position: relative;
  z-index: 1;
  width: 100%;
  max-width: 1080px;
  margin-inline: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 28px;
}

/* Glass surface shared by every panel. */
.glass {
  background: linear-gradient(145deg, var(--glass-strong), var(--glass));
  border: 1px solid var(--glass-edge);
  border-radius: 24px;
  box-shadow: var(--shadow), inset 0 1px 0 var(--glass-shine);
  -webkit-backdrop-filter: blur(22px) saturate(160%);
  backdrop-filter: blur(22px) saturate(160%);
}

/* Hero */
.hero {
  width: 100%;
  padding: clamp(36px, 7vw, 72px) clamp(20px, 5vw, 56px);
  text-align: center;
  border-radius: 32px;
}
.hero h1 {
  margin: 0;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: clamp(2rem, 6.4vw, 4rem);
  line-height: 1.1;
  letter-spacing: -0.02em;
  text-wrap: balance;
  background: linear-gradient(100deg, #ffffff 10%, #c9b8ff 50%, #8fe9ff 90%);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.visitors {
  padding: 8px 14px;
  border-radius: 999px;
  display: inline-flex;
  align-items: center;
  line-height: 0;
}
.visitors img { display: block; height: 20px; width: auto; }

/* Section headings */
.section {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}
.section-title {
  margin: 0;
  padding: 10px 28px;
  border-radius: 999px;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: clamp(0.95rem, 2.4vw, 1.15rem);
  letter-spacing: 0.14em;
  text-transform: uppercase;
  text-align: center;
  text-wrap: balance;
}

/* About */
.about {
  width: 100%;
  max-width: 760px;
  padding: clamp(22px, 4vw, 38px);
  text-align: center;
  color: var(--ink-soft);
  font-size: clamp(1rem, 2.2vw, 1.12rem);
}
.about p { margin: 0; }

/* Project cards */
.cards {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
}
.card {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 12px;
  border-radius: 20px;
  text-decoration: none;
  transition: transform 0.25s ease, border-color 0.25s ease, background 0.25s ease;
}
.card img { display: block; width: 100%; height: auto; border-radius: 12px; }
.card:hover, .card:focus-visible {
  transform: translateY(-4px);
  border-color: rgba(255, 255, 255, 0.45);
  background: linear-gradient(145deg, rgba(255, 255, 255, 0.18), rgba(255, 255, 255, 0.09));
}
.card:focus-visible, .badge:focus-visible, .stat:focus-visible, .chips a:focus-visible {
  outline: 2px solid var(--aurora-cyan);
  outline-offset: 3px;
}
.cards.single { grid-template-columns: minmax(0, 420px); justify-content: center; }

/* Tech stack */
.chips {
  padding: 18px 28px;
  border-radius: 20px;
  display: flex;
  justify-content: center;
}
.chips a { display: block; line-height: 0; border-radius: 12px; }
.chips img { display: block; max-width: 100%; height: auto; }

/* Stats */
.stats {
  width: 100%;
  padding: clamp(16px, 3vw, 28px);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 18px;
}
.stat { display: block; line-height: 0; max-width: 100%; border-radius: 12px; }
.stat img { display: block; max-width: 100%; height: auto; border-radius: 12px; }

/* Socials */
.badges {
  padding: 20px clamp(16px, 4vw, 32px);
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 14px;
}
.badge {
  display: block;
  line-height: 0;
  padding: 8px;
  border-radius: 16px;
  transition: transform 0.25s ease, border-color 0.25s ease;
}
.badge img { display: block; height: 28px; width: auto; border-radius: 6px; }
.badge:hover, .badge:focus-visible { transform: translateY(-3px); border-color: rgba(255, 255, 255, 0.45); }

/* Footer */
.footer {
  max-width: 100%;
  padding: 14px 28px;
  border-radius: 999px;
  text-align: center;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--ink-soft);
  text-wrap: balance;
}

@media (max-width: 760px) {
  body { padding-block: 24px 40px; }
  .cards { grid-template-columns: minmax(0, 1fr); }
  .cards.single { grid-template-columns: minmax(0, 1fr); }
  .section-title { padding-inline: 20px; letter-spacing: 0.1em; }
}

@media (prefers-reduced-motion: reduce) {
  .card, .badge { transition: none; }
  .card:hover, .card:focus-visible, .badge:hover, .badge:focus-visible { transform: none; }
}

/* Browsers without backdrop-filter get a more opaque panel so text stays readable. */
@supports not ((backdrop-filter: blur(1px)) or (-webkit-backdrop-filter: blur(1px))) {
  .glass { background: rgba(28, 32, 62, 0.92); }
}
</style>
</head>
<body>
<div class="aurora" aria-hidden="true"><span class="o1"></span><span class="o2"></span><span class="o3"></span><span class="o4"></span></div>

<main class="page">

  <!-- Header banner -->
  <header class="hero glass">
    <h1>👋 Hi, I'm Ömer 👋</h1>
  </header>

  <!-- Visitor counter -->
  <a class="visitors glass" href="#!">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=omerdenizhan&left_text=Visitors" alt="Visitors">
  </a>

  <!-- About Me -->
  <section class="section">
    <h2 class="section-title glass">💫 About Me</h2>
    <div class="about glass">
      <p>I am a peaceful person who does no harm to anyone, is married, happy and has children.<br>All of my work is for hobby purposes and I do not have a commercial purpose.<br>I update my current projects and work on new projects whenever I get the chance.</p>
    </div>
  </section>

  <!-- Projects -->
  <section class="section">
    <h2 class="section-title glass">⚙️ Projects</h2>
    <div class="cards">
      <a class="card glass" href="https://github.com/omerdenizhan/Video-Downloader">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=Video-Downloader&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="D-Tube Video Downloader">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/Site360Pro">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=Site360Pro&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Site360Pro">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/Kisisel-Finans-Yonetimi">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=Kisisel-Finans-Yonetimi&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Kişisel Finans Yönetimi">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/Kredi-Taksit-Takip-Sistemi">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=Kredi-Taksit-Takip-Sistemi&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Kredi Taksit Takip Sistemi">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/IPTV-M3U-Editor">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=IPTV-M3U-Editor&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="IPTV M3U Editor">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/IPTV-M3U">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=IPTV-M3U&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="IPTV M3U">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/batch-scripts">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=batch-scripts&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Batch Scripts">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/Material-Design-Dark-Cursors">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=Material-Design-Dark-Cursors&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Material Design Dark Cursors">
      </a>
      <a class="card glass" href="https://github.com/omerdenizhan/win-reg-compilations">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=win-reg-compilations&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="Regedit Compilations">
      </a>
    </div>
  </section>

  <!-- Projects Web Pages -->
  <section class="section">
    <h2 class="section-title glass">⚙️ Projects Web Pages</h2>
    <div class="cards single">
      <a class="card glass" href="https://omerdenizhan.github.io/IPTV-M3U-Editor">
        <img src="https://github-readme-stats.shion.dev/api/pin/?username=omerdenizhan&repo=IPTV-M3U-Editor&theme=radical&show_owner=false&border_radius=10&card_width=400&description_lines_count=1" alt="IPTV M3U Editor Web Page">
      </a>
    </div>
  </section>

  <!-- Tech Stack -->
  <section class="section">
    <h2 class="section-title glass">💻 Tech Stack</h2>
    <div class="chips glass">
      <a href="https://skillicons.dev">
        <img src="https://skillicons.dev/icons?i=html,tailwind,css,js,python,php,kotlin&theme=dark" alt="Tech Stack">
      </a>
    </div>
  </section>

  <!-- GitHub Stats -->
  <section class="section">
    <h2 class="section-title glass">📊 GitHub Stats</h2>
    <div class="stats glass">
      <a class="stat" href="#!">
        <img src="https://github-readme-stats.shion.dev/api?username=omerdenizhan&theme=radical&hide_border=false&include_all_commits=false&count_private=false&border_radius=10" alt="GitHub Stats">
      </a>
      <a class="stat" href="#!">
        <img src="https://streak-stats.demolab.com/?user=omerdenizhan&theme=radical&hide_border=false&border_radius=10" alt="Current Streaks">
      </a>
      <a class="stat" href="#!">
        <img src="https://github-readme-stats.shion.dev/api/top-langs/?username=omerdenizhan&theme=radical&hide_border=false&include_all_commits=false&count_private=false&layout=compact&border_radius=10" alt="Most Used Languages">
      </a>
    </div>
  </section>

  <!-- Socials -->
  <section class="section">
    <h2 class="section-title glass">🌐 Socials</h2>
    <div class="badges glass">
      <a class="badge glass" href="https://facebook.com/dnzhn77" title="Facebook">
        <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook">
      </a>
      <a class="badge glass" href="https://instagram.com/dnzhn.77" title="Instagram">
        <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram">
      </a>
      <a class="badge glass" href="https://x.com/dnzhn_77" title="X (Old Twitter)">
        <img src="https://img.shields.io/badge/Twitter/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="Twitter/X">
      </a>
      <a class="badge glass" href="https://t.me/dnzhn77" title="Telegram">
        <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
      </a>
      <a class="badge glass" href="https://reddit.com/denizhan77" title="Reddit">
        <img src="https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white" alt="Reddit">
      </a>
      <a class="badge glass" href="mailto:omer_denizhan@msn.com" title="Email">
        <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
      </a>
    </div>
  </section>

  <!-- Footer banner -->
  <footer class="footer glass">Last Update: Oct 28, 2026 • Made with ❤️</footer>

</main>
</body>
</html>
