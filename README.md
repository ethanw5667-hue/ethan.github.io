<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Ethan Wang — Portfolio</title>
  <meta name="description" content="Personal website and portfolio of Ethan Wang." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="assets/css/styles.css" />
</head>
<body>
  <!-- Header / Nav -->
  <header class="site-header">
    <nav class="container nav">
      <a class="brand" href="#home">Ethan Wang</a>
      <button class="nav-toggle" aria-label="Toggle navigation">☰</button>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#resume">Resume</a></li>
        <li><a href="#cv">CV</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero container">
    <div class="hero-inner">
      <h1>Hi, I’m <span class="accent">Ethan</span>.</h1>
      <p class="lead">I tinker with physics and write about how ideas turn into things. Here’s a simple, fast website you can build on.</p>
      <div class="hero-cta">
        <a href="#projects" class="btn">See Projects</a>
        <a href="#contact" class="btn btn-ghost">Get in Touch</a>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="section container">
    <h2 class="section-title">About</h2>
    <div class="grid-2">
      <div>
        <p>
          I’m a student who loves mechanics-based physics, astronomy, and building hands-on experiments.
          This site is a starter you can edit in minutes. Keep the structure, swap the content.
        </p>
        <p>
          Highlights: competitions, lab projects, and writing. Replace this with your own summary and a photo if you like.
        </p>
      </div>
      <div>
        <div class="card">
          <h3>Quick Facts</h3>
          <ul class="list">
            <li>Based in Toronto • open to remote collab</li>
            <li>Physics, math, and writing projects</li>
            <li>Contact below</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects" class="section container">
    <h2 class="section-title">Projects</h2>
    <div class="cards">
      <article class="card">
        <h3>Basement Lab Experiments</h3>
        <p>Oscillations, Arduino data logging, curve fits. Swap in yours.</p>
        <a class="card-link" href="#">Read more →</a>
      </article>
      <article class="card">
        <h3>Astrophysics Notes</h3>
        <p>Kepler’s laws, vis-viva, anomalies. Put your repo or PDF link here.</p>
        <a class="card-link" href="#">Open repo →</a>
      </article>
      <article class="card">
        <h3>Writing</h3>
        <p>Essays on autonomy, narrative, and science communication.</p>
        <a class="card-link" href="#">View essays →</a>
      </article>
    </div>
  </section>

  <!-- Resume (blank placeholder) -->
  <section id="resume" class="section container">
    <h2 class="section-title">Resume</h2>
    <div class="muted">
      <p><em>Placeholder:</em> Add your resume here later. You can embed a PDF or link to a file in this repo.</p>
      <!-- Example embed (uncomment and replace when ready): -->
      <!-- <iframe class="embed" src="assets/resume.pdf" title="Resume"></iframe> -->
    </div>
  </section>

  <!-- CV (blank placeholder) -->
  <section id="cv" class="section container">
    <h2 class="section-title">CV</h2>
    <div class="muted">
      <p><em>Placeholder:</em> Add a detailed CV here later. Consider a Markdown → HTML render or PDF embed.</p>
      <!-- <iframe class="embed" src="assets/cv.pdf" title="CV"></iframe> -->
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="section container">
    <h2 class="section-title">Contact</h2>
    <div class="grid-2">
      <p>
        The simplest way: send me an email.
      </p>
      <form class="contact" action="mailto:you@example.com" method="post" enctype="text/plain">
        <label>
          Name
          <input type="text" name="name" required>
        </label>
        <label>
          Email
          <input type="email" name="email" required>
        </label>
        <label>
          Message
          <textarea name="message" rows="4" required></textarea>
        </label>
        <button class="btn" type="submit">Send</button>
      </form>
    </div>
  </section>

  <footer class="site-footer">
    <div class="container footer-inner">
      <span>© <span id="year"></span> Ethan Wang</span>
      <a href="https://github.com/" target="_blank" rel="noreferrer">GitHub</a>
    </div>
  </footer>

  <script src="assets/js/main.js"></script>
</body>
</html>
