<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Xavier Razafimahaleo | Portfolio Électricité & BIM</title>
  <meta name="description" content="Portfolio de Xavier Razafimahaleo - Technicien Bureau d'Études Électricité des Bâtiments, BIM, Revit, AutoCAD, Dialux, Caneco BT." />
  <style>
    :root {
      --bg: #0f172a;
      --bg-soft: #111827;
      --card: #1e293b;
      --text: #e5e7eb;
      --muted: #94a3b8;
      --accent: #38bdf8;
      --accent-2: #22c55e;
      --border: rgba(255,255,255,0.08);
      --shadow: 0 20px 40px rgba(0,0,0,0.25);
      --radius: 20px;
      --max: 1100px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: linear-gradient(180deg, #020617 0%, #0f172a 100%);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(92%, var(--max));
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(12px);
      background: rgba(2, 6, 23, 0.7);
      border-bottom: 1px solid var(--border);
    }

    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 16px 0;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .logo span { color: var(--accent); }

    .nav-links {
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
      font-size: 0.95rem;
      color: var(--muted);
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: var(--text);
    }

    .hero {
      padding: 88px 0 50px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.3fr 0.7fr;
      gap: 28px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      padding: 8px 14px;
      border: 1px solid rgba(56, 189, 248, 0.35);
      background: rgba(56, 189, 248, 0.1);
      color: var(--accent);
      border-radius: 999px;
      font-size: 0.9rem;
      margin-bottom: 18px;
    }

    h1 {
      font-size: clamp(2rem, 4vw, 4rem);
      line-height: 1.08;
      margin: 0 0 18px;
    }

    .hero p {
      color: var(--muted);
      font-size: 1.05rem;
      max-width: 720px;
      margin-bottom: 28px;
    }

    .cta {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 14px 20px;
      border-radius: 14px;
      border: 1px solid transparent;
      font-weight: 700;
      transition: 0.25s ease;
    }

    .btn-primary {
      background: var(--accent);
      color: #082f49;
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 30px rgba(56, 189, 248, 0.28);
    }

    .btn-secondary {
      border-color: var(--border);
      background: rgba(255,255,255,0.03);
      color: var(--text);
    }

    .btn-secondary:hover {
      background: rgba(255,255,255,0.06);
    }

    .hero-card,
    .card {
      background: rgba(30, 41, 59, 0.7);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .hero-card {
      padding: 26px;
    }

    .hero-card h3 {
      margin-top: 0;
      margin-bottom: 14px;
      font-size: 1.1rem;
    }

    .stats {
      display: grid;
      gap: 14px;
    }

    .stat {
      padding: 14px;
      border-radius: 16px;
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(255,255,255,0.05);
    }

    .stat strong {
      display: block;
      color: var(--accent);
      font-size: 1.25rem;
      margin-bottom: 4px;
    }

    section {
      padding: 34px 0;
    }

    .section-title {
      font-size: 1.9rem;
      margin-bottom: 8px;
    }

    .section-subtitle {
      color: var(--muted);
      margin-top: 0;
      margin-bottom: 28px;
    }

    .about-grid,
    .projects-grid,
    .skills-grid,
    .contact-grid {
      display: grid;
      gap: 22px;
    }

    .about-grid {
      grid-template-columns: 1fr 1fr;
    }

    .projects-grid {
      grid-template-columns: repeat(3, 1fr);
    }

    .skills-grid {
      grid-template-columns: repeat(4, 1fr);
    }

    .contact-grid {
      grid-template-columns: 1fr 1fr;
    }

    .card {
      padding: 24px;
    }

    .project-tag,
    .skill-tag {
      display: inline-block;
      padding: 6px 10px;
      border-radius: 999px;
      font-size: 0.85rem;
      margin: 4px 6px 0 0;
      background: rgba(56, 189, 248, 0.1);
      color: #bae6fd;
      border: 1px solid rgba(56, 189, 248, 0.2);
    }

    .project-card h3,
    .card h3 {
      margin-top: 0;
      margin-bottom: 10px;
    }

    .muted {
      color: var(--muted);
    }

    ul.clean {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    ul.clean li {
      padding: 10px 0;
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    ul.clean li:last-child {
      border-bottom: none;
    }

    .project-links {
      margin-top: 16px;
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .project-links a {
      color: var(--accent);
      font-weight: 700;
      font-size: 0.95rem;
    }

    .contact-box a {
      color: var(--accent);
    }

    footer {
      padding: 40px 0 60px;
      color: var(--muted);
      text-align: center;
    }

    @media (max-width: 960px) {
      .hero-grid,
      .about-grid,
      .contact-grid,
      .projects-grid,
      .skills-grid {
        grid-template-columns: 1fr;
      }

      .nav {
        align-items: flex-start;
        gap: 12px;
        flex-direction: column;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="logo">Xavier <span>Portfolio</span></div>
      <nav class="nav-links">
        <a href="#about">À propos</a>
        <a href="#projects">Projets</a>
        <a href="#skills">Compétences</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <div class="badge">Technicien Bureau d'Études Électricité • BIM • CFO/CFA</div>
          <h1>Je conçois des projets électriques clairs, propres et exploitables.</h1>
          <p>
            Je m'appelle Xavier Razafimahaleo. Je construis mon profil en bureau d'études électricité des bâtiments avec un focus sur le dessin technique, la modélisation BIM, les notes de calcul et l'éclairage.
          </p>
          <div class="cta">
            <a class="btn btn-primary" href="#projects">Voir mes projets</a>
            <a class="btn btn-secondary" href="#contact">Me contacter</a>
          </div>
        </div>

        <aside class="hero-card">
          <h3>Profil rapide</h3>
          <div class="stats">
            <div class="stat">
              <strong>AFPA</strong>
              <span class="muted">Formation technicien BE électricité des bâtiments</span>
            </div>
            <div class="stat">
              <strong>Outils</strong>
              <span class="muted">Revit, AutoCAD, Dialux, Caneco BT, Excel</span>
            </div>
            <div class="stat">
              <strong>Objectif</strong>
              <span class="muted">Devenir dessinateur projeteur / technicien BE en électricité</span>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <h2 class="section-title">À propos</h2>
        <p class="section-subtitle">Un profil en reconversion, orienté technique, rigueur et progression terrain.</p>

        <div class="about-grid">
          <article class="card">
            <h3>Mon parcours</h3>
            <p class="muted">
              Après plusieurs expériences professionnelles, je me spécialise aujourd'hui dans l'électricité des bâtiments. Je développe mes compétences sur des projets concrets en DAO, BIM, éclairage et dimensionnement.
            </p>
            <p class="muted">
              Mon objectif est simple : devenir un professionnel solide, capable de produire des plans, maquettes et documents techniques propres, cohérents et utilisables en entreprise.
            </p>
          </article>

          <article class="card">
            <h3>Ce que je recherche</h3>
            <ul class="clean muted">
              <li>Stage et opportunités en bureau d'études électricité</li>
              <li>Projets CFO/CFA, BIM et exécution</li>
              <li>Missions où la rigueur, la logique et la progression comptent vraiment</li>
              <li>Un environnement pour monter rapidement en niveau</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <h2 class="section-title">Projets</h2>
        <p class="section-subtitle">Remplace ces exemples par tes vrais rendus, captures et liens GitHub.</p>

        <div class="projects-grid">
          <article class="card project-card">
            <h3>Projet éclairage – crèche</h3>
            <p class="muted">Étude d'éclairage sous Dialux avec implantation des luminaires, vérification des niveaux d'éclairement et rendu de présentation.</p>
            <div>
              <span class="project-tag">Dialux</span>
              <span class="project-tag">Éclairage</span>
              <span class="project-tag">Normes</span>
            </div>
            <div class="project-links">
              <a href="#">Voir le projet</a>
              <a href="#">Capture / PDF</a>
            </div>
          </article>

          <article class="card project-card">
            <h3>Maquette BIM – cheminements CFO/CFA</h3>
            <p class="muted">Modélisation Revit de cheminements, chemins de câbles et organisation d'une maquette propre pour lecture technique et coordination.</p>
            <div>
              <span class="project-tag">Revit</span>
              <span class="project-tag">BIM</span>
              <span class="project-tag">CFO/CFA</span>
            </div>
            <div class="project-links">
              <a href="#">Voir le projet</a>
              <a href="#">Détails</a>
            </div>
          </article>

          <article class="card project-card">
            <h3>Bilan de puissance – hôtel</h3>
            <p class="muted">Tableau Excel structuré avec circuits, puissances, hypothèses de simultanéité et base d'analyse pour note de calcul.</p>
            <div>
              <span class="project-tag">Excel</span>
              <span class="project-tag">Dimensionnement</span>
              <span class="project-tag">Méthode</span>
            </div>
            <div class="project-links">
              <a href="#">Voir le projet</a>
              <a href="#">Télécharger</a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <h2 class="section-title">Compétences</h2>
        <p class="section-subtitle">Les outils et sujets que je travaille actuellement.</p>

        <div class="skills-grid">
          <article class="card">
            <h3>DAO / CAO</h3>
            <p class="muted">AutoCAD 2D, plans d'implantation, calques, blocs, schématisation.</p>
          </article>
          <article class="card">
            <h3>BIM</h3>
            <p class="muted">Revit, modélisation MEP, cheminements, familles, vues et organisation.</p>
          </article>
          <article class="card">
            <h3>Éclairage</h3>
            <p class="muted">Dialux Evo, implantation, uniformité, éclairement et présentation.</p>
          </article>
          <article class="card">
            <h3>Calcul</h3>
            <p class="muted">Caneco BT, bilans de puissance, sections, protections, logique de dimensionnement.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <h2 class="section-title">Contact</h2>
        <p class="section-subtitle">Tu peux remplacer ces infos par tes vraies coordonnées.</p>

        <div class="contact-grid">
          <article class="card contact-box">
            <h3>Coordonnées</h3>
            <p class="muted">Email : <a href="mailto:tonemail@example.com">tonemail@example.com</a></p>
            <p class="muted">LinkedIn : <a href="#">ajoute-ton-lien-linkedin</a></p>
            <p class="muted">GitHub : <a href="#">ajoute-ton-lien-github</a></p>
          </article>

          <article class="card">
            <h3>Message</h3>
            <p class="muted">
              Je suis actuellement en développement de compétences dans le domaine du bureau d'études électricité des bâtiments. Je reste ouvert aux échanges, aux opportunités de stage et aux collaborations autour de projets techniques.
            </p>
          </article>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      © 2026 Xavier Razafimahaleo — Portfolio Électricité & BIM
    </div>
  </footer>
</body>
</html>
