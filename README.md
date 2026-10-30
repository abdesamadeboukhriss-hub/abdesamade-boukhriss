<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Portfolio d'Abdessamad Boukhriss, étudiant en informatique et futur professionnel de la cybersécurité.">
  <title>Abdessamad Boukhriss | Cybersecurity Portfolio</title>
  <style>
    :root {
      --bg: #080d12;
      --panel: #101922;
      --panel-2: #0c141c;
      --text: #edf4f7;
      --muted: #9aabb5;
      --green: #52f2a5;
      --line: rgba(154, 171, 181, .18);
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: radial-gradient(circle at 80% 5%, rgba(27, 112, 86, .16), transparent 28rem), var(--bg);
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.65;
    }
    a { color: inherit; text-decoration: none; }
    .container { width: min(1080px, 90%); margin: auto; }
    header { position: sticky; top: 0; z-index: 10; background: rgba(8,13,18,.88); backdrop-filter: blur(14px); border-bottom: 1px solid var(--line); }
    nav { min-height: 72px; display: flex; align-items: center; justify-content: space-between; gap: 20px; }
    .brand { font-weight: 800; letter-spacing: .04em; font-size: 1.05rem; }
    .brand span { color: var(--green); }
    .nav-links { display: flex; gap: 25px; color: var(--muted); font-size: .9rem; }
    .nav-links a:hover { color: var(--green); }
    .hero { min-height: 650px; display: grid; grid-template-columns: 1.35fr .85fr; align-items: center; gap: 55px; padding: 90px 0; }
    .eyebrow { color: var(--green); font: 600 .78rem/1.4 ui-monospace, SFMono-Regular, Menlo, monospace; letter-spacing: .15em; text-transform: uppercase; }
    h1 { font-size: clamp(2.7rem, 6vw, 5rem); line-height: 1.07; letter-spacing: -.055em; margin: 20px 0; }
    h1 span { color: var(--green); }
    .intro { max-width: 620px; color: var(--muted); font-size: 1.08rem; }
    .actions { display: flex; flex-wrap: wrap; gap: 13px; margin-top: 30px; }
    .button { display: inline-flex; align-items: center; justify-content: center; padding: 12px 18px; border-radius: 8px; border: 1px solid var(--green); font-weight: 700; font-size: .9rem; transition: .2s; }
    .button.primary { background: var(--green); color: #07110d; }
    .button:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(82,242,165,.12); }
    .hero-side { display: grid; gap: 18px; max-width: 390px; width: 100%; justify-self: end; }
    .portrait-card { padding: 10px; border: 1px solid var(--line); border-radius: 18px; background: linear-gradient(145deg, #14232b, #0b1219); box-shadow: 0 25px 80px rgba(0,0,0,.28); }
    .portrait { display: block; width: 100%; aspect-ratio: 1 / 1.08; object-fit: cover; object-position: center 28%; border-radius: 12px; }
    .portrait-caption { display:flex; justify-content:space-between; gap:12px; padding: 12px 5px 4px; color: var(--muted); font: .75rem ui-monospace, monospace; }
    .portrait-caption strong { color: var(--green); font-weight: 600; }
    .terminal { background: linear-gradient(145deg, #121e27, #0b1219); border: 1px solid var(--line); border-radius: 15px; overflow: hidden; box-shadow: 0 25px 80px rgba(0,0,0,.28); }
    .terminal-top { display: flex; align-items: center; gap: 7px; padding: 14px 17px; border-bottom: 1px solid var(--line); color: var(--muted); font: .75rem ui-monospace, monospace; }
    .dot { width: 8px; height: 8px; border-radius: 50%; background: #50616b; }
    .terminal-body { padding: 24px; font: .88rem/2 ui-monospace, SFMono-Regular, Menlo, monospace; color: var(--muted); }
    .terminal-body .green { color: var(--green); }
    .terminal-body .white { color: var(--text); }
    section { padding: 78px 0; border-top: 1px solid var(--line); }
    .section-kicker { color: var(--green); font: .75rem ui-monospace, monospace; letter-spacing: .15em; text-transform: uppercase; }
    h2 { font-size: clamp(1.8rem, 4vw, 2.6rem); margin: 9px 0 28px; letter-spacing: -.035em; }
    .about-grid { display: grid; grid-template-columns: 1.2fr .8fr; gap: 35px; }
    .copy { color: var(--muted); max-width: 680px; }
    .info-card, .card { background: var(--panel); border: 1px solid var(--line); border-radius: 13px; padding: 23px; }
    .info-card p { color: var(--muted); font-size: .92rem; margin-top: 8px; }
    .info-card strong { color: var(--green); }
    .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
    .card .icon { color: var(--green); font: 1.3rem ui-monospace, monospace; }
    .card h3 { margin: 13px 0 7px; font-size: 1.05rem; }
    .card p { color: var(--muted); font-size: .9rem; }
    .tag { display: inline-block; margin: 12px 5px 0 0; padding: 4px 9px; border: 1px solid var(--line); border-radius: 5px; color: #c4d2d9; font-size: .75rem; }
    .project-note { color: var(--muted); margin-top: 18px; font-size: .88rem; }
    .contact-box { display: flex; align-items: center; justify-content: space-between; gap: 25px; background: linear-gradient(120deg, rgba(82,242,165,.1), rgba(16,25,34,.8)); border: 1px solid rgba(82,242,165,.25); border-radius: 15px; padding: 30px; }
    .contact-box p { color: var(--muted); }
    footer { padding: 25px 0; color: var(--muted); font-size: .82rem; border-top: 1px solid var(--line); }
    footer .container { display: flex; justify-content: space-between; gap: 15px; flex-wrap: wrap; }
    @media (max-width: 760px) {
      .nav-links { gap: 12px; font-size: .78rem; }
      .hero { min-height: auto; grid-template-columns: 1fr; gap: 35px; padding: 75px 0; }
      .hero-side { justify-self: start; max-width: 420px; }
      .about-grid, .cards { grid-template-columns: 1fr; }
      section { padding: 60px 0; }
      .contact-box { align-items: flex-start; flex-direction: column; }
    }
    @media (max-width: 430px) {
      nav { align-items: flex-start; flex-direction: column; padding: 15px 0; }
      .nav-links { width: 100%; justify-content: space-between; }
    }
  </style>
</head>
<body>
  <header>
    <nav class="container">
      <a class="brand" href="#home">AB<span>.</span></a>
      <div class="nav-links">
        <a href="#about">À propos</a>
        <a href="#skills">Compétences</a>
        <a href="#projects">Projets</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero container" id="home" style="border:0">
      <div>
        <p class="eyebrow">Portfolio personnel / 2026</p>
        <h1>Abdessamad<br><span>Boukhriss.</span></h1>
        <p class="intro">Étudiant en informatique, curieux des technologies et particulièrement intéressé par la cybersécurité. Je construis progressivement mes compétences en programmation, systèmes et réseaux.</p>
        <div class="actions">
          <a class="button primary" href="#projects">Voir mon parcours</a>
          <a class="button" href="#contact">Me contacter</a>
        </div>
      </div>
      <div class="hero-side">
        <div class="portrait-card">
          <img class="portrait" src="assets/abdessamad-profile.jpeg" alt="Portrait professionnel d'Abdessamad Boukhriss">
          <div class="portrait-caption"><span>ABDESSAMAD BOUKHRISS</span><strong>● OPEN TO LEARN</strong></div>
        </div>
        <div class="terminal" aria-label="Présentation technique">
          <div class="terminal-top"><i class="dot"></i><i class="dot"></i><i class="dot"></i><span style="margin-left:8px">abdessamad@portfolio: ~</span></div>
          <div class="terminal-body">
            <div><span class="green">$</span> whoami</div>
            <div class="white">DUT Student · Morocco</div>
            <div><span class="green">$</span> focus</div>
            <div class="white">Cybersecurity · Networks · Data</div>
            <div><span class="green">$</span> status</div>
            <div class="white">Always learning_</div>
          </div>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <p class="section-kicker">01 / À propos</p>
        <h2>Apprendre. Construire. Progresser.</h2>
        <div class="about-grid">
          <p class="copy">Je suis étudiant en première année de DUT Informatique Décisionnelle et Statistique. Je m'intéresse à l'informatique, au fonctionnement des systèmes et à la sécurité numérique. Mon objectif est de développer des bases solides et d'évoluer progressivement vers le domaine de la cybersécurité.</p>
          <div class="info-card">
            <strong>Actuellement</strong>
            <p>En formation — DUT Informatique Décisionnelle et Statistique</p>
            <p>Objectif — Approfondir les systèmes, les réseaux et la cybersécurité</p>
            <p>Localisation — Maroc</p>
          </div>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <p class="section-kicker">02 / Compétences</p>
        <h2>Mes bases actuelles & centres d'intérêt</h2>
        <div class="cards">
          <article class="card"><div class="icon">01 //</div><h3>Développement web</h3><p>Découverte de la structure des pages web et de leur mise en forme.</p><span class="tag">HTML</span><span class="tag">CSS — en apprentissage</span></article>
          <article class="card"><div class="icon">02 //</div><h3>Algorithmique</h3><p>Apprentissage de la logique, des variables, des conditions et des boucles.</p><span class="tag">Bases</span><span class="tag">Exercices</span></article>
          <article class="card"><div class="icon">03 //</div><h3>Cybersécurité</h3><p>Domaine que je souhaite explorer : sécurité des systèmes, réseaux et bonnes pratiques numériques.</p><span class="tag">Objectif professionnel</span><span class="tag">En découverte</span></article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <p class="section-kicker">03 / Projets & apprentissage</p>
        <h2>Mon évolution</h2>
        <div class="cards">
          <article class="card"><div class="icon">&lt;/&gt;</div><h3>Première page web</h3><p>Exercices d'initiation à la création de pages avec HTML et CSS dans le cadre de mon apprentissage.</p><span class="tag">HTML</span><span class="tag">CSS</span></article>
          <article class="card"><div class="icon">{ }</div><h3>Algorithmique</h3><p>Travail sur les notions fondamentales et la résolution de petits problèmes.</p><span class="tag">Logique</span><span class="tag">Boucles</span></article>
          <article class="card"><div class="icon">[ + ]</div><h3>Prochaines étapes</h3><p>Renforcer mes connaissances en réseaux, systèmes et programmation avant d'aborder des projets pratiques en cybersécurité.</p><span class="tag">En préparation</span></article>
        </div>
        <p class="project-note">Ce portfolio présente mon niveau actuel et mes objectifs. De nouveaux projets seront ajoutés au fur et à mesure de mon apprentissage.</p>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <p class="section-kicker">04 / Contact</p>
        <h2>Restons en contact.</h2>
        <div class="contact-box">
          <div><h3>Échangeons autour de l'informatique.</h3><p>Retrouvez-moi sur LinkedIn pour échanger autour de l’informatique et de la cybersécurité.</p></div>
          <div class="actions" style="margin:0">
            <!-- Remplace les liens ci-dessous par tes vrais liens -->
            <a class="button primary" href="https://www.linkedin.com/in/abde-samade-boukhriss-150a4a446/" target="_blank" rel="noopener noreferrer">LinkedIn ↗</a>

          </div>
        </div>
      </div>
    </section>
  </main>

  <footer><div class="container"><span>© 2026 Abdessamad Boukhriss</span><span>Conçu avec HTML & CSS.</span></div></footer>
</body>
</html
