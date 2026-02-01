# TWWebWorks
Business Page 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TW WebWorks</title>

<style>
:root {
  --bg: #0f172a;
  --card: #111827;
  --text: #e5e7eb;
  --muted: #9ca3af;
  --accent: #38bdf8;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

body {
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

/* BACKGROUND SLIDESHOW */
.bg {
  position: fixed;
  inset: 0;
  z-index: -2;
}

.bg div {
  position: absolute;
  inset: 0;
  background-size: cover;
  background-position: center;
  opacity: 0;
  transition: opacity 2s ease;
}

.bg div.active {
  opacity: 1;
}

.overlay {
  position: fixed;
  inset: 0;
  background: rgba(15, 23, 42, 0.85);
  z-index: -1;
}

/* CONTENT */
header {
  padding: 5rem 1.5rem;
  text-align: center;
  max-width: 900px;
  margin: auto;
}

header h1 {
  font-size: 2.6rem;
}

header span {
  color: var(--accent);
}

header p {
  margin-top: 1rem;
  color: var(--muted);
  font-size: 1.1rem;
}

section {
  max-width: 900px;
  margin: 4rem auto;
  padding: 0 1.5rem;
}

h2 {
  margin-bottom: 1.25rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
}

.card {
  background: var(--card);
  padding: 1.5rem;
  border-radius: 14px;
}

.card img {
  width: 100%;
  height: 120px;
  object-fit: cover;
  border-radius: 10px;
  margin: .75rem 0;
  opacity: 0.9;
}

.price {
  color: var(--accent);
  font-weight: bold;
  margin-top: .5rem;
}

.button {
  display: inline-block;
  margin-top: 1.75rem;
  padding: .75rem 1.5rem;
  background: var(--accent);
  color: #000;
  border-radius: 999px;
  text-decoration: none;
  font-weight: bold;
}

footer {
  text-align: center;
  padding: 3rem 1.5rem;
  color: var(--muted);
}
</style>
</head>

<body>

<div class="bg">
  <div class="active" style="background-image:url('https://images.unsplash.com/photo-1503387762-592deb58ef4e?w=1600');"></div>
  <div style="background-image:url('https://images.unsplash.com/photo-1565372918679-1e129f8b6d31?w=1600');"></div>
  <div style="background-image:url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=1600');"></div>
  <div style="background-image:url('https://images.unsplash.com/photo-1504198453319-5ce911bafcde?w=1600');"></div>
</div>

<div class="overlay"></div>

<header>
  <h1>Websites Built Your Way<br><span>TW WebWorks</span></h1>
  <p>Fast, efficient, and customized exactly how you want.</p>
  <a href="#pricing" class="button">Get Started</a>
</header>

<section>
  <h2>What We Do</h2>
  <div class="grid">
    <div class="card">
      <h3>Custom Websites</h3>
      <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?w=1200">
      <p>Clean, lightweight sites designed around how you actually want to use them.</p>
    </div>

    <div class="card">
      <h3>Efficiency Tuning</h3>
      <img src="https://images.unsplash.com/photo-1555949963-aa79dcee981c?w=1200">
      <p>Speed improvements, cleanup, and optimization for existing sites.</p>
    </div>

    <div class="card">
      <h3>Personal Tweaks</h3>
      <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=1200">
      <p>Small changes, special features, or layout quirks — we make it fit you.</p>
    </div>
  </div>
</section>

<!-- MIDDLE PRICING / MESSAGE -->
<section>
  <h2>Affordable & Built for You</h2>
  <div class="card">
    <p>
      My goal with TW WebWorks is to make websites affordable, fast, and easy to work with.
      I focus on clear communication, efficient builds, and being available when you need changes.
    </p>
    <p style="margin-top:1rem;">
      You don’t need an expensive agency to get a website that works well and looks professional.
    </p>
  </div>
</section>

<!-- BOTTOM PRICING -->
<section id="pricing">
  <h2>Pricing</h2>
  <div class="grid">
    <div class="card">
      <h3>Starter Site</h3>
      <p>Simple, fast, and clean</p>
      <div class="price">$45</div>
    </div>

    <div class="card">
      <h3>Custom Build</h3>
      <p>Tailored exactly to you</p>
      <div class="price">$90</div>
    </div>

    <div class="card">
      <h3>Speed & Fixes</h3>
      <p>Improve an existing site</p>
      <div class="price">$40 or $15/hr</div>
    </div>
  </div>

  <div class="card" style="margin-top:2rem; text-align:center;">
    <p>
      📧 <strong>SONNYW02@gmail.com</strong><br>
      📞 <strong>810-241-7628</strong>
    </p>
  </div>
</section>

<footer>
  © 2026 • TW WebWorks
</footer>

<script>
const slides = document.querySelectorAll('.bg div');
let i = 0;

setInterval(() => {
  slides[i].classList.remove('active');
  i = (i + 1) % slides.length;
  slides[i].classList.add('active');
}, 6000);
</script>

</body>
</html>
