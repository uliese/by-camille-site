@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap');

:root {
  color-scheme: dark;
  --bg: #000;
  --panel: #0d0d0d;
  --panel-2: #151515;
  --text: #fff;
  --muted: rgba(255, 255, 255, 0.62);
  --faint: rgba(255, 255, 255, 0.36);
  --line: rgba(255, 255, 255, 0.1);
  --accent: #ef4444;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}
a { color: inherit; text-decoration: none; }
img { display: block; max-width: 100%; }

.site-shell { min-height: 100vh; background: #000; }
.site-header {
  position: sticky;
  top: 0;
  z-index: 50;
  border-bottom: 1px solid var(--line);
  background: rgba(0,0,0,.82);
  backdrop-filter: blur(18px);
}
.nav {
  max-width: 1280px;
  margin: 0 auto;
  padding: 16px 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}
.logo {
  font-size: 13px;
  letter-spacing: .52em;
  font-weight: 700;
  white-space: nowrap;
}
.nav-links { display: flex; gap: 32px; font-size: 14px; }
.nav-links a { color: rgba(255,255,255,.82); transition: color .25s ease; }
.nav-links a:hover { color: var(--accent); }
.nav-cta {
  border: 1px solid rgba(255,255,255,.22);
  border-radius: 999px;
  padding: 12px 20px;
  background: rgba(255,255,255,.08);
  transition: all .25s ease;
  font-size: 14px;
  font-weight: 600;
}
.nav-cta:hover { background: #fff; color: #000; }

.hero {
  min-height: 100vh;
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: flex-end;
  padding: 128px 24px 96px;
}
.hero-image {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: .74;
  transform: scale(1.02);
}
.hero-overlay {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at 72% 34%, transparent 0%, rgba(0,0,0,.58) 62%),
    linear-gradient(to top, #000 0%, rgba(0,0,0,.52) 48%, rgba(0,0,0,.22) 100%);
}
.hero-content {
  position: relative;
  z-index: 2;
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
}
.eyebrow {
  margin: 0 0 22px;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: .42em;
  font-size: 13px;
  font-weight: 700;
}
.eyebrow.muted { color: var(--faint); }
h1, h2, h3 { font-family: "Playfair Display", Georgia, serif; margin: 0; font-weight: 600; }
h1 {
  max-width: 1060px;
  font-size: clamp(56px, 11vw, 148px);
  line-height: .9;
  letter-spacing: -.055em;
}
h2 {
  font-size: clamp(48px, 7vw, 104px);
  line-height: 1;
  letter-spacing: -.045em;
}
.button-row { display: flex; flex-wrap: wrap; gap: 16px; margin-top: 40px; }
.button {
  border-radius: 999px;
  padding: 16px 32px;
  font-weight: 700;
  transition: all .25s ease;
}
.button-light { background: #fff; color: #000; }
.button-light:hover { background: var(--accent); color: #fff; }
.button-outline { border: 1px solid rgba(255,255,255,.24); }
.button-outline:hover { background: #fff; color: #000; }

.marquee-strip {
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
  padding: 20px 24px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 26px;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: .24em;
  font-size: 13px;
}
.section { padding: 128px 24px; }
.section-heading {
  max-width: 1280px;
  margin: 0 auto 48px;
}
.section-heading.split {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  gap: 32px;
}
.section-heading.center { text-align: center; }
.section-copy {
  max-width: 460px;
  margin: 0;
  color: var(--muted);
  line-height: 1.7;
}
.portfolio-grid {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 20px;
}
.portfolio-card {
  overflow: hidden;
  border-radius: 32px;
  border: 1px solid var(--line);
  background: var(--panel);
}
.portfolio-image-wrap { height: 340px; overflow: hidden; }
.portfolio-card.tall .portfolio-image-wrap { height: 560px; }
.portfolio-image-wrap img {
  width: 100%; height: 100%; object-fit: cover;
  transition: transform .75s ease;
}
.portfolio-card:hover img { transform: scale(1.055); }
.portfolio-caption {
  background: #000;
  padding: 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.portfolio-caption p {
  margin: 0 0 8px;
  color: var(--faint);
  text-transform: uppercase;
  letter-spacing: .22em;
  font-size: 11px;
  font-weight: 700;
}
.portfolio-caption h3 { font-size: 28px; }
.portfolio-caption span { color: var(--muted); font-size: 24px; }
.about-section { background: var(--panel); }
.about-grid {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: .82fr 1.18fr;
  gap: 56px;
  align-items: center;
}
.about-image-wrap {
  overflow: hidden;
  border-radius: 32px;
  border: 1px solid var(--line);
}
.about-image-wrap img { width: 100%; height: 620px; object-fit: cover; }
.about-copy p:not(.eyebrow) {
  margin: 28px 0 0;
  max-width: 760px;
  color: rgba(255,255,255,.72);
  font-size: 18px;
  line-height: 1.8;
}
.trait-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 34px; }
.trait-grid div { border: 1px solid var(--line); border-radius: 20px; padding: 22px; background: #000; }
.trait-grid strong { display: block; font-family: "Playfair Display", serif; font-size: 30px; font-weight: 600; }
.trait-grid span { display: block; margin-top: 6px; color: var(--faint); }
.archive-grid {
  max-width: 1280px;
  margin: 0 auto;
  columns: 3 280px;
  column-gap: 18px;
}
.archive-grid img {
  width: 100%;
  margin: 0 0 18px;
  border-radius: 24px;
  border: 1px solid var(--line);
  break-inside: avoid;
}
.services-section { border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); }
.services-inner { max-width: 980px; margin: 0 auto; text-align: center; }
.services-inner p:not(.eyebrow) { max-width: 760px; margin: 32px auto 0; color: var(--muted); font-size: 18px; line-height: 1.8; }
.contact-grid {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr .9fr;
  gap: 56px;
  align-items: center;
}
.contact-grid p:not(.eyebrow) { color: var(--muted); font-size: 18px; line-height: 1.8; max-width: 580px; }
.contact-details { margin-top: 28px; color: var(--muted); }
.contact-details p { margin: 10px 0; }
.contact-form {
  border: 1px solid var(--line);
  background: var(--panel);
  padding: 24px;
  border-radius: 32px;
  display: grid;
  gap: 14px;
}
.contact-form input,
.contact-form select,
.contact-form textarea {
  width: 100%;
  border: 1px solid var(--line);
  background: #000;
  color: #fff;
  border-radius: 18px;
  padding: 16px;
  font: inherit;
  outline: none;
}
.contact-form textarea { min-height: 140px; resize: vertical; }
.contact-form input:focus,
.contact-form select:focus,
.contact-form textarea:focus { border-color: var(--accent); }
.contact-form button {
  border: 0;
  border-radius: 999px;
  padding: 16px;
  background: #fff;
  color: #000;
  font-weight: 800;
  cursor: pointer;
  transition: all .25s ease;
}
.contact-form button:hover { background: var(--accent); color: #fff; }
.footer {
  border-top: 1px solid var(--line);
  padding: 32px 24px;
  max-width: 1280px;
  margin: 0 auto;
  color: var(--faint);
  display: flex;
  justify-content: space-between;
  gap: 24px;
  font-size: 14px;
}

@media (max-width: 900px) {
  .nav-links { display: none; }
  .hero { padding-bottom: 72px; }
  .section { padding: 96px 20px; }
  .section-heading.split, .about-grid, .contact-grid { grid-template-columns: 1fr; display: grid; }
  .portfolio-grid { grid-template-columns: 1fr; }
  .portfolio-card.tall .portfolio-image-wrap, .portfolio-image-wrap { height: 460px; }
  .about-image-wrap img { height: 520px; }
  .trait-grid { grid-template-columns: 1fr; }
  .footer { flex-direction: column; }
}

@media (max-width: 560px) {
  .logo { letter-spacing: .32em; }
  .hero { padding-inline: 18px; }
  .button-row { flex-direction: column; }
  .button { text-align: center; }
  .portfolio-card.tall .portfolio-image-wrap, .portfolio-image-wrap { height: 380px; }
}
Site update.
