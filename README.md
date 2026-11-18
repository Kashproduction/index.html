<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kashproduction — Studio de Jeux Mobiles</title>
<meta name="description" content="Kashproduction — Studio indépendant créant des jeux mobiles multilingues. Découvrez QUIZ TAUPE et nos futurs titres.">
<meta name="author" content="Kashproduction">
<style>
:root{
  --bg:#0d0908;
  --bg-2:#150e0c;
  --surface:#1a1212;
  --surface-2:#251a18;
  --border:#3a2a26;
  --border-bright:#5c3f3a;
  --text:#f5ede0;
  --text-dim:#c9b9a8;
  --muted:#8a7568;
  --crimson:#c41e3a;
  --crimson-bright:#e63946;
  --crimson-deep:#7a0e1f;
  --amber:#e9b44c;
  --gold:#f5d67e;
  --emerald:#5a9477;
  --navy:#1a2845;
  --navy-bright:#2a4870;
}

*{margin:0;padding:0;box-sizing:border-box}
html{-webkit-text-size-adjust:100%}
body{
  background:var(--bg);
  color:var(--text);
  font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Helvetica Neue',Arial,sans-serif;
  min-height:100vh;
  overflow-x:hidden;
  position:relative;
  line-height:1.6;
}
body::before{
  content:'';
  position:fixed;
  inset:0;
  z-index:0;
  pointer-events:none;
  background:
    radial-gradient(ellipse 80% 60% at 15% 0%,rgba(196,30,58,0.13) 0%,transparent 50%),
    radial-gradient(ellipse 60% 50% at 85% 100%,rgba(233,180,76,0.07) 0%,transparent 50%),
    linear-gradient(180deg,var(--bg) 0%,var(--bg-2) 100%);
}
body::after{
  content:'';
  position:fixed;
  inset:0;
  z-index:1;
  pointer-events:none;
  opacity:.4;
  mix-blend-mode:overlay;
  background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 200 200'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3' stitchTiles='stitch'/><feColorMatrix values='0 0 0 0 0.1 0 0 0 0 0.08 0 0 0 0 0.06 0 0 0 0.7 0'/></filter><rect width='100%25' height='100%25' filter='url(%23n)' opacity='0.4'/></svg>");
}
.container{
  position:relative;
  z-index:10;
  max-width:1200px;
  margin:0 auto;
  padding:0 1.5rem;
}

/* ===== HEADER ===== */
.header{
  padding:2rem 0 1rem;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  text-align:center;
}
.header-logo{
  width:clamp(80px,15vw,140px);
  height:auto;
  margin-bottom:1.5rem;
  border-radius:50%;
  box-shadow:0 8px 40px rgba(196,30,58,0.3),0 0 0 1px var(--border-bright);
  transition:transform .3s ease;
}
.header-logo:hover{transform:scale(1.05) rotate(-2deg)}
.header-tagline{
  color:var(--amber);
  font-size:.8rem;
  letter-spacing:.3em;
  text-transform:uppercase;
  font-family:'Courier New',monospace;
  margin-top:.5rem;
  opacity:.8;
}

/* ===== HERO ===== */
.hero{
  padding:3rem 0 4rem;
  text-align:center;
}
.hero h1{
  font-family:Georgia,'Times New Roman',serif;
  font-size:clamp(2.5rem,7vw,4.5rem);
  font-weight:500;
  line-height:1;
  letter-spacing:-.025em;
  margin-bottom:1.5rem;
  background:linear-gradient(135deg,var(--text) 0%,var(--amber) 100%);
  -webkit-background-clip:text;
  background-clip:text;
  -webkit-text-fill-color:transparent;
}
.hero p{
  font-size:clamp(1rem,2.5vw,1.25rem);
  color:var(--text-dim);
  max-width:600px;
  margin:0 auto 2rem;
  line-height:1.7;
}
.hero .stamp{
  display:inline-flex;
  align-items:center;
  padding:.4rem 1rem;
  border:1px solid var(--border-bright);
  color:var(--amber);
  font-family:'Courier New',monospace;
  font-size:.7rem;
  letter-spacing:.25em;
  text-transform:uppercase;
  background:rgba(26,18,18,.5);
  margin-bottom:2rem;
}

/* ===== SECTION TITLES ===== */
.section-title{
  font-family:Georgia,serif;
  font-size:clamp(1.75rem,4vw,2.5rem);
  font-weight:500;
  text-align:center;
  margin-bottom:1rem;
  letter-spacing:-.02em;
  color:var(--text);
}
.section-title .accent{
  color:var(--crimson-bright);
  font-style:italic;
}
.section-subtitle{
  text-align:center;
  color:var(--muted);
  font-size:.9rem;
  letter-spacing:.2em;
  text-transform:uppercase;
  margin-bottom:3rem;
}

/* ===== GAMES GRID ===== */
.games-section{padding:3rem 0 4rem}
.games-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:2rem;
  margin-top:2rem;
}

/* ===== GAME CARD ===== */
.game-card{
  background:var(--surface);
  border:1px solid var(--border);
  border-radius:8px;
  overflow:hidden;
  position:relative;
  transition:all .3s ease;
  display:flex;
  flex-direction:column;
}
.game-card::before{
  content:'';
  position:absolute;
  top:0;left:0;right:0;
  height:1px;
  background:linear-gradient(90deg,transparent,var(--border-bright),transparent);
}
.game-card:hover{
  transform:translateY(-4px);
  border-color:var(--crimson);
  box-shadow:0 12px 40px rgba(196,30,58,0.25),0 0 0 1px var(--crimson);
}
.game-card-image{
  width:100%;
  aspect-ratio:16/10;
  background:linear-gradient(135deg,var(--crimson-deep) 0%,var(--crimson) 50%,var(--amber) 100%);
  position:relative;
  overflow:hidden;
  display:flex;
  align-items:center;
  justify-content:center;
}
.game-card-image::after{
  content:'';
  position:absolute;
  inset:0;
  background:
    radial-gradient(circle at 30% 40%,rgba(255,255,255,0.15) 0%,transparent 40%),
    radial-gradient(circle at 70% 60%,rgba(0,0,0,0.2) 0%,transparent 40%);
  pointer-events:none;
}
.game-card-emoji{
  font-size:5rem;
  filter:drop-shadow(0 4px 12px rgba(0,0,0,0.4));
  z-index:2;
  position:relative;
  animation:floatEmoji 3s ease-in-out infinite;
}
@keyframes floatEmoji{
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-8px)}
}
.game-card-badge{
  position:absolute;
  top:1rem;
  right:1rem;
  background:rgba(26,18,18,0.85);
  border:1px solid var(--amber);
  color:var(--amber);
  padding:.25rem .75rem;
  font-family:'Courier New',monospace;
  font-size:.65rem;
  letter-spacing:.2em;
  text-transform:uppercase;
  z-index:3;
  border-radius:4px;
  backdrop-filter:blur(4px);
}
.game-card-body{
  padding:1.75rem;
  flex:1;
  display:flex;
  flex-direction:column;
}
.game-card-title{
  font-family:Georgia,serif;
  font-size:1.5rem;
  font-weight:600;
  margin-bottom:.5rem;
  color:var(--text);
}
.game-card-genre{
  color:var(--amber);
  font-size:.75rem;
  letter-spacing:.15em;
  text-transform:uppercase;
  font-family:'Courier New',monospace;
  margin-bottom:1rem;
}
.game-card-desc{
  color:var(--text-dim);
  font-size:.95rem;
  line-height:1.6;
  margin-bottom:1.5rem;
  flex:1;
}
.game-card-features{
  display:flex;
  flex-wrap:wrap;
  gap:.5rem;
  margin-bottom:1.5rem;
}
.feature-tag{
  background:var(--surface-2);
  border:1px solid var(--border);
  padding:.3rem .7rem;
  border-radius:4px;
  font-size:.75rem;
  color:var(--text-dim);
}
.game-card-cta{
  display:flex;
  gap:.5rem;
  flex-wrap:wrap;
}
.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:.5rem;
  padding:.75rem 1.25rem;
  border:1px solid var(--border-bright);
  color:var(--text);
  text-decoration:none;
  font-weight:500;
  font-size:.85rem;
  letter-spacing:.1em;
  text-transform:uppercase;
  border-radius:4px;
  transition:all .2s ease;
  flex:1;
  min-width:120px;
}
.btn:hover{
  background:var(--surface-2);
  border-color:var(--crimson);
  color:var(--crimson-bright);
  transform:translateY(-1px);
}
.btn-primary{
  background:linear-gradient(135deg,var(--crimson-deep) 0%,var(--crimson) 100%);
  border-color:var(--crimson-bright);
  color:#fff;
  box-shadow:0 4px 16px rgba(196,30,58,0.3);
}
.btn-primary:hover{
  background:linear-gradient(135deg,var(--crimson) 0%,var(--crimson-bright) 100%);
  color:#fff;
  box-shadow:0 6px 24px rgba(196,30,58,0.5);
}

/* ===== COMING SOON CARD ===== */
.game-card.coming-soon{
  opacity:.5;
  border-style:dashed;
  border-color:var(--border);
}
.game-card.coming-soon:hover{
  opacity:.7;
  transform:none;
  border-color:var(--muted);
  box-shadow:none;
}
.game-card.coming-soon .game-card-image{
  background:linear-gradient(135deg,var(--surface-2) 0%,var(--surface) 100%);
}
.game-card.coming-soon .game-card-emoji{
  opacity:.5;
  animation:none;
}

/* ===== ABOUT SECTION ===== */
.about-section{
  padding:4rem 0;
  background:var(--bg-2);
  position:relative;
}
.about-section::before{
  content:'';
  position:absolute;
  top:0;left:0;right:0;
  height:1px;
  background:linear-gradient(90deg,transparent,var(--border-bright),transparent);
}
.about-content{
  max-width:700px;
  margin:0 auto;
  text-align:center;
}
.about-content p{
  color:var(--text-dim);
  font-size:1.05rem;
  line-height:1.8;
  margin-bottom:1rem;
}
.about-stats{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
  gap:2rem;
  margin-top:3rem;
}
.stat{
  text-align:center;
}
.stat-number{
  font-family:Georgia,serif;
  font-size:2.5rem;
  font-weight:600;
  color:var(--amber);
  display:block;
  margin-bottom:.5rem;
}
.stat-label{
  color:var(--muted);
  font-size:.8rem;
  letter-spacing:.15em;
  text-transform:uppercase;
}

/* ===== FOOTER ===== */
.footer{
  padding:3rem 0 2rem;
  text-align:center;
  border-top:1px solid var(--border);
  margin-top:2rem;
}
.footer-logo{
  width:60px;
  height:auto;
  border-radius:50%;
  margin-bottom:1rem;
  opacity:.7;
}
.footer p{
  color:var(--muted);
  font-size:.85rem;
  margin-bottom:.5rem;
}
.footer .footer-links{
  display:flex;
  justify-content:center;
  gap:2rem;
  margin-top:1.5rem;
  flex-wrap:wrap;
}
.footer-links a{
  color:var(--text-dim);
  text-decoration:none;
  font-size:.85rem;
  letter-spacing:.1em;
  text-transform:uppercase;
  transition:color .2s;
}
.footer-links a:hover{color:var(--amber)}
.footer .copyright{
  margin-top:2rem;
  color:var(--muted);
  font-size:.8rem;
  font-style:italic;
}

/* ===== RESPONSIVE ===== */
@media(max-width:600px){
  .container{padding:0 1rem}
  .header{padding:1.5rem 0 .5rem}
  .hero{padding:2rem 0 3rem}
  .games-grid{grid-template-columns:1fr;gap:1.5rem}
  .about-stats{grid-template-columns:repeat(2,1fr);gap:1.5rem}
  .stat-number{font-size:2rem}
}
</style>
</head>
<body>

<div class="container">

  <!-- ===== HEADER ===== -->
  <header class="header">
    <img src="logo.jpg" alt="Kashproduction Logo" class="header-logo">
    <div class="header-tagline">Studio Indépendant · Jeux Mobiles</div>
  </header>

  <!-- ===== HERO ===== -->
  <section class="hero">
    <div class="stamp">🎮 Mobile Gaming Studio</div>
    <h1>Kashproduction</h1>
    <p>
      Studio indépendant créant des jeux mobiles multilingues,
      conviviaux et originaux. Des expériences pensées pour les soirées
      entre amis et les moments de partage en famille.
    </p>
  </section>

  <!-- ===== GAMES SECTION ===== -->
  <section class="games-section">
    <h2 class="section-title">Nos <span class="accent">Jeux</span></h2>
    <p class="section-subtitle">— Découvrez nos créations —</p>

    <div class="games-grid">

      <!-- QUIZ TAUPE -->
      <article class="game-card">
        <div class="game-card-image">
          <span class="game-card-badge">● Live</span>
          <span class="game-card-emoji">🕵️</span>
        </div>
        <div class="game-card-body">
          <h3 class="game-card-title">QUIZ TAUPE</h3>
          <div class="game-card-genre">Party Game · Trivia · Multijoueur</div>
          <p class="game-card-desc">
            Un quiz où la trahison paie trois fois plus. L'un de vous est
            secrètement la taupe et doit saboter la partie sans être démasqué.
            2 481 questions en 3 langues, 12 thèmes saisonniers.
          </p>
          <div class="game-card-features">
            <span class="feature-tag">🌍 3 langues (FR/EN/ES)</span>
            <span class="feature-tag">👥 2-4 joueurs</span>
            <span class="feature-tag">❓ 2481 questions</span>
            <span class="feature-tag">🎃 Thèmes saisonniers</span>
          </div>
          <div class="game-card-cta">
            <a href="https://www.amazon.com/dp/B0HPZ1DFLJ" target="_blank" rel="noopener" class="btn btn-primary">📱 Amazon Appstore</a>
          </div>
        </div>
      </article>

      <!-- COMING SOON PLACEHOLDER -->
      <article class="game-card coming-soon">
        <div class="game-card-image">
          <span class="game-card-badge">Bientôt</span>
          <span class="game-card-emoji">🚀</span>
        </div>
        <div class="game-card-body">
          <h3 class="game-card-title">Prochain jeu</h3>
          <div class="game-card-genre">À venir · Restez connectés</div>
          <p class="game-card-desc">
            Notre prochain titre est en cours de développement.
            Kashproduction continue de créer des expériences de jeu
            uniques et multilingues. Suite à venir...
          </p>
          <div class="game-card-features">
            <span class="feature-tag">🎨 En développement</span>
          </div>
        </div>
      </article>

    </div>
  </section>

  <!-- ===== ABOUT SECTION ===== -->
  <section class="about-section">
    <div class="about-content">
      <h2 class="section-title">Le <span class="accent">Studio</span></h2>
      <p class="section-subtitle">— Notre vision —</p>

      <p>
        Kashproduction est un studio indépendant dédié à la création
        de jeux mobiles accessibles, multilingues et conviviaux.
      </p>
      <p>
        Notre approche : des applications 100% locales qui fonctionnent
        hors ligne, sans collecte de données personnelles, pour une
        expérience utilisateur sereine et respectueuse de la vie privée.
      </p>

      <div class="about-stats">
        <div class="stat">
          <span class="stat-number">1</span>
          <span class="stat-label">Jeu publié</span>
        </div>
        <div class="stat">
          <span class="stat-number">3</span>
          <span class="stat-label">Langues</span>
        </div>
        <div class="stat">
          <span class="stat-number">2 481</span>
          <span class="stat-label">Questions</span>
        </div>
        <div class="stat">
          <span class="stat-number">100%</span>
          <span class="stat-label">Offline</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer class="footer">
    <img src="logo.jpg" alt="Kashproduction" class="footer-logo">
    <p><strong>Kashproduction</strong></p>
    <p>Studio indépendant de jeux mobiles</p>

    <div class="footer-links">
      <a href="https://www.amazon.com/dp/B0HPZ1DFLJ" target="_blank" rel="noopener">Amazon Appstore</a>
      <a href="https://kashproduction.github.io/QUIZ-TAUPE/" target="_blank" rel="noopener">Privacy Policy</a>
      <a href="mailto:contact@kashproduction.com">Contact</a>
    </div>

    <p class="copyright">
      © 2026 Kashproduction. Tous droits réservés.
    </p>
  </footer>

</div>

</body>
</html>
