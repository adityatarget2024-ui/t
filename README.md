# t
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>For Tashu</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300;1,400&family=Inter:wght@300;400&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #1a1730;
    --bg-2: #241d3d;
    --text: #f3ecff;
    --muted: rgba(243, 236, 255, 0.7);
    --faint: rgba(243, 236, 255, 0.5);
    --accent: #e6b8c4;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html, body { height: 100%; }
  body {
    font-family: 'Inter', sans-serif;
    font-weight: 300;
    background: linear-gradient(180deg, var(--bg) 0%, var(--bg-2) 100%);
    color: var(--text);
    overflow-x: hidden;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }
  .stars { position: fixed; inset: 0; pointer-events: none; z-index: 0; }
  .star {
    position: absolute; background: rgba(255,255,255,0.7);
    border-radius: 50%;
    animation: twinkle 4s ease-in-out infinite;
  }
  @keyframes twinkle {
    0%, 100% { opacity: 0.2; }
    50% { opacity: 1; }
  }
  .moon {
    position: fixed; top: 12%; right: 12%;
    width: 180px; height: 180px; border-radius: 50%;
    background: radial-gradient(circle at 35% 35%, rgba(255,255,255,0.18), rgba(255,255,255,0.04));
    box-shadow: 0 0 60px rgba(255,255,255,0.06);
    animation: float 10s ease-in-out infinite;
    pointer-events: none; z-index: 0;
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
  }
  section {
    position: relative; z-index: 1;
    min-height: 70vh;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    padding: 3rem 1.5rem; text-align: center;
  }
  .hero { min-height: 100vh; }
  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 300;
    letter-spacing: 0.04em;
    color: rgba(255,255,255,0.9);
  }
  .hero h1.line1 { font-size: clamp(2.5rem, 6vw, 4.5rem); }
  .hero h1.line2 {
    font-size: clamp(3rem, 8vw, 6rem);
    margin-top: 0.5rem;
    color: #fff;
    letter-spacing: 0.06em;
  }
  .hero p {
    margin-top: 2.5rem; max-width: 34rem;
    font-style: italic; color: var(--muted);
    font-size: clamp(1rem, 2vw, 1.25rem);
  }
  .verse {
    max-width: 40rem;
    font-size: clamp(1.25rem, 2.4vw, 1.75rem);
    line-height: 2;
    color: rgba(255,255,255,0.8);
    font-weight: 300;
  }
  .highlight {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.5rem, 3vw, 2.25rem);
    color: var(--accent);
    margin-top: 1.5rem;
    line-height: 1.6;
  }
  .eyebrow {
    font-size: 0.75rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: rgba(230, 184, 196, 0.6);
    margin-bottom: 1.5rem;
  }
  .soft-note {
    margin-top: 2rem; max-width: 32rem;
    color: var(--faint); font-size: 1rem; line-height: 2;
  }
  .outro { min-height: 90vh; padding-bottom: 5rem; }
  .outro p {
    font-size: clamp(1.25rem, 2vw, 1.5rem);
    color: rgba(255,255,255,0.7);
    line-height: 2.2; margin-bottom: 3rem;
  }
  .outro .goodnight {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(2rem, 5vw, 3.25rem);
    color: rgba(255,255,255,0.6);
    letter-spacing: 0.08em;
  }
  .divider {
    width: 2rem; height: 1px;
    background: rgba(230, 184, 196, 0.4);
    margin: 0 auto 1.25rem;
  }
  .reveal {
    opacity: 0; transform: translateY(20px);
    transition: opacity 1.2s ease, transform 1.2s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>
<div class="stars" id="stars"></div>
<div class="moon"></div>
<section class="hero">
  <div class="reveal visible">
    <h1 class="line1">Good night,</h1>
    <h1 class="line2">Tashuuu baby</h1>
    <p>Just a little space to say sleep well, and that I'm glad you're around.</p>
  </div>
</section>
<section>
  <div class="verse reveal">
    The day is finally quiet.<br />
    I hope you're cozy,<br />
    and I hope tomorrow is kind to you.
  </div>
</section>
<section>
  <div class="reveal" style="max-width: 40rem;">
    <p class="verse" style="margin-bottom: 2rem;">Even though you delete my photos...</p>
    <p class="highlight">I'll still be living rent-free in your heart.</p>
  </div>
</section>
<section>
  <div class="reveal" style="max-width: 40rem;">
    <p class="eyebrow">A little note</p>
    <p class="verse" style="margin-bottom: 1.5rem;">And if anything I said or did ever hurt you,</p>
    <p class="highlight">I'm really sorry.</p>
    <p class="soft-note">I didn't mean to. I just want you to be happy, and to sleep tonight knowing that.</p>
  </div>
</section>
<section class="outro">
  <div class="reveal">
    <p>Get some rest.<br />Dream of nice things.</p>
    <div class="divider"></div>
    <h3 class="goodnight">Goodnight.</h3>
  </div>
</section>
<script>
  const starsEl = document.getElementById('stars');
  for (let i = 0; i < 80; i++) {
    const s = document.createElement('div');
    s.className = 'star';
    const size = Math.random() * 2 + 0.5;
    s.style.width = size + 'px';
    s.style.height = size + 'px';
    s.style.top = Math.random() * 100 + '%';
    s.style.left = Math.random() * 100 + '%';
    s.style.animationDelay = (Math.random() * 5) + 's';
    starsEl.appendChild(s);
  }
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.15 });
  document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>
</body>
</html>
