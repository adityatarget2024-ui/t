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
    cursor: crosshair;
  }
  .stars { position: fixed; inset: 0; pointer-events: none; z-index: 0; }
  .star {
    position: absolute; background: rgba(255,255,255,0.7);
    border-radius: 50%;
    animation: twinkle 4s ease-in-out infinite;
  }
  .user-star {
    animation: pulse 2.5s ease-in-out infinite;
    background: var(--accent);
    box-shadow: 0 0 8px var(--accent);
  }
  @keyframes twinkle { 0%,100% {opacity:.2;} 50% {opacity:1;} }
  @keyframes pulse { 0%,100% {opacity:.5; transform:scale(1);} 50% {opacity:1; transform:scale(1.4);} }
  .moon {
    position: fixed; top: 12%; right: 12%;
    width: 180px; height: 180px; border-radius: 50%;
    background: radial-gradient(circle at 35% 35%, rgba(255,255,255,0.18), rgba(255,255,255,0.04));
    box-shadow: 0 0 60px rgba(255,255,255,0.06);
    animation: float 10s ease-in-out infinite;
    z-index: 2; cursor: pointer;
    transition: box-shadow .6s ease, transform .6s ease;
  }
  .moon.bloom { box-shadow: 0 0 120px rgba(230,184,196,.35); transform: scale(1.08); }
  .moon-msg {
    position: fixed; top: calc(12% + 200px); right: 12%;
    font-family: 'Cormorant Garamond', serif; font-style: italic;
    color: var(--accent); font-size: 1rem; z-index: 2;
    opacity: 0; transition: opacity 1s ease;
    pointer-events: none;
  }
  .moon-msg.show { opacity: 1; }
  @keyframes float { 0%,100% {transform:translateY(0);} 50% {transform:translateY(-20px);} }

  .shooting-star {
    position: fixed; width: 2px; height: 2px;
    background: white; border-radius: 50%;
    box-shadow: 0 0 6px 1px rgba(255,255,255,.8);
    z-index: 1; pointer-events: none;
  }
  .shooting-star::after {
    content: ''; position: absolute;
    top: 0; left: 0; width: 120px; height: 1px;
    background: linear-gradient(to left, rgba(255,255,255,.8), transparent);
    transform: translateX(-120px);
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
    font-weight: 300; letter-spacing: 0.04em;
    color: rgba(255,255,255,0.9);
  }
  .hero h1.line1 { font-size: clamp(2.5rem, 6vw, 4.5rem); }
  .hero h1.line2 {
    font-size: clamp(3rem, 8vw, 6rem);
    margin-top: 0.5rem; color: #fff; letter-spacing: 0.06em;
  }
  .hero p {
    margin-top: 2.5rem; max-width: 34rem;
    font-style: italic; color: var(--muted);
    font-size: clamp(1rem, 2vw, 1.25rem);
  }
  .typewriter {
    margin-top: 2.5rem;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    color: var(--accent);
    font-size: clamp(1.1rem, 2vw, 1.4rem);
    min-height: 2em;
  }
  .typewriter::after {
    content: '|'; margin-left: 2px;
    animation: blink 1s step-end infinite;
  }
  @keyframes blink { 50% { opacity: 0; } }

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
    margin-top: 1.5rem; line-height: 1.6;
  }
  .eyebrow {
    font-size: 0.75rem; letter-spacing: 0.3em;
    text-transform: uppercase;
    color: rgba(230, 184, 196, 0.6);
    margin-bottom: 1.5rem;
  }
  .soft-note {
    margin-top: 2rem; max-width: 32rem;
    color: var(--faint); font-size: 1rem; line-height: 2;
  }

  /* Reasons */
  .reasons-grid {
    display: grid; gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    max-width: 60rem; margin-top: 2rem;
  }
  .reason-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(230,184,196,0.12);
    backdrop-filter: blur(8px);
    padding: 1.5rem 1.25rem;
    border-radius: 12px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    color: rgba(255,255,255,0.85);
    font-size: 1.1rem;
    line-height: 1.5;
    transition: transform .5s ease, background .5s ease;
    transform: rotate(-1deg);
  }
  .reason-card:nth-child(even) { transform: rotate(1.2deg); }
  .reason-card:hover {
    transform: rotate(0) translateY(-4px);
    background: rgba(230,184,196,0.08);
  }

  /* Folded note */
  .note-wrap { perspective: 1200px; width: 100%; max-width: 32rem; }
  .note {
    background: linear-gradient(180deg, #f6eedd, #efe0c9);
    color: #4a3a2b;
    padding: 2.5rem 2rem;
    border-radius: 6px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 1.15rem;
    line-height: 1.9;
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    transform: rotateX(-85deg);
    transform-origin: top center;
    transition: transform 1.5s cubic-bezier(.2,.8,.2,1);
  }
  .note.open { transform: rotateX(0deg); }

  .outro { min-height: 90vh; padding-bottom: 4rem; }
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
    background: rgba(230,184,196,0.4);
    margin: 0 auto 1.25rem;
  }

  footer {
    text-align: center; padding: 2rem;
    color: rgba(255,255,255,0.3);
    font-family: 'Cormorant Garamond', serif;
    font-style: italic; letter-spacing: 0.3em;
    position: relative; z-index: 1;
  }

  .audio-toggle {
    position: fixed; top: 1.25rem; left: 1.25rem;
    z-index: 10; background: rgba(255,255,255,0.06);
    border: 1px solid rgba(230,184,196,0.25);
    color: var(--text);
    padding: 0.55rem 0.9rem;
    border-radius: 999px;
    font-family: 'Inter', sans-serif;
    font-size: 0.75rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    cursor: pointer;
    backdrop-filter: blur(10px);
    transition: all .3s ease;
  }
  .audio-toggle:hover { background: rgba(230,184,196,0.15); }
  .audio-toggle.playing { color: var(--accent); border-color: var(--accent); }
  .audio-toggle .dot {
    display: inline-block; width: 6px; height: 6px;
    border-radius: 50%; background: currentColor;
    margin-right: 8px; vertical-align: middle;
    opacity: .4;
  }
  .audio-toggle.playing .dot {
    opacity: 1; animation: pulse 1.8s ease-in-out infinite;
  }

  .star-counter {
    position: fixed; bottom: 1rem; right: 1rem;
    color: rgba(255,255,255,0.4);
    font-size: 0.7rem; letter-spacing: 0.2em;
    text-transform: uppercase;
    z-index: 5;
    font-family: 'Inter', sans-serif;
  }

  .reveal {
    opacity: 0; transform: translateY(20px);
    transition: opacity 1.2s ease, transform 1.2s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<button class="audio-toggle" id="audioBtn"><span class="dot"></span>Lullaby</button>
<div class="star-counter" id="starCounter">stars placed: 0</div>

<div class="stars" id="stars"></div>
<div class="moon" id="moon"></div>
<div class="moon-msg" id="moonMsg">you found it — sweet dreams</div>

<section class="hero">
  <div class="reveal visible">
    <h1 class="line1">Good night,</h1>
    <h1 class="line2">Tashuuu baby</h1>
    <p>Just a little space to say sleep well, and that I'm glad you're around.</p>
    <div class="typewriter" id="typewriter"></div>
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
  <div class="reveal" style="max-width: 60rem; width: 100%;">
    <p class="eyebrow">A few small reasons</p>
    <div class="reasons-grid">
      <div class="reason-card">the way you laugh at your own jokes</div>
      <div class="reason-card">how you always know the snack we actually want</div>
      <div class="reason-card">the little hum you do when you're thinking</div>
      <div class="reason-card">how you text me chaos at 2am</div>
      <div class="reason-card">the face you make when food is too good</div>
      <div class="reason-card">how you remember the dumb things I say</div>
      <div class="reason-card">the way you make ordinary days feel lighter</div>
    </div>
  </div>
</section>

<section>
  <div class="reveal" style="max-width: 40rem;">
    <p class="verse" style="margin-bottom: 2rem;">Even though you delete my photos...</p>
    <p class="highlight">I'll still be living rent-free in your heart.</p>
  </div>
</section>

<section>
  <div class="reveal" style="max-width: 32rem;">
    <p class="eyebrow">A small verse</p>
    <p class="verse" style="font-family: 'Cormorant Garamond', serif; font-style: italic;">
      the lamp is low,<br />
      the room is still,<br />
      the world can wait —<br />
      and so can I.
    </p>
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

<section>
  <div class="note-wrap reveal" id="noteWrap">
    <div class="note" id="note">
      close your eyes,<br />
      let the day go,<br />
      rest your shoulders,<br />
      you've done enough today.
    </div>
  </div>
</section>

<section class="outro">
  <div class="reveal">
    <p>Get some rest.<br />Dream of nice things.</p>
    <div class="divider"></div>
    <h3 class="goodnight">Goodnight.</h3>
  </div>
</section>

<footer>xoxo</footer>

<script>
  // Background stars
  const starsEl = document.getElementById('stars');
  for (let i = 0; i < 100; i++) {
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

  // Scroll reveal
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        if (e.target.id === 'noteWrap') {
          document.getElementById('note').classList.add('open');
        }
      }
    });
  }, { threshold: 0.15 });
  document.querySelectorAll('.reveal').forEach(el => io.observe(el));

  // Click to place a star
  let starCount = 0;
  const counter = document.getElementById('starCounter');
  document.body.addEventListener('click', (e) => {
    if (e.target.closest('button, a, .moon, .reason-card')) return;
    const s = document.createElement('div');
    s.className = 'star user-star';
    s.style.width = '4px';
    s.style.height = '4px';
    s.style.position = 'fixed';
    s.style.top = e.clientY + 'px';
    s.style.left = e.clientX + 'px';
    s.style.zIndex = 3;
    s.style.pointerEvents = 'none';
    document.body.appendChild(s);
    starCount++;
    counter.textContent = 'stars placed: ' + starCount;
  });

  // Typewriter
  const lines = [
    'thinking of you',
    'hope you had a good day',
    'sleep soft tonight',
    'glad you exist'
  ];
  const tw = document.getElementById('typewriter');
  let li = 0, ci = 0, deleting = false;
  function type() {
    const cur = lines[li];
    if (!deleting) {
      tw.textContent = cur.slice(0, ci++);
      if (ci > cur.length) { deleting = true; setTimeout(type, 1800); return; }
    } else {
      tw.textContent = cur.slice(0, ci--);
      if (ci < 0) { deleting = false; li = (li + 1) % lines.length; ci = 0; }
    }
    setTimeout(type, deleting ? 40 : 80);
  }
  type();

  // Moon tap
  const moon = document.getElementById('moon');
  const moonMsg = document.getElementById('moonMsg');
  let moonTaps = 0;
  moon.addEventListener('click', (e) => {
    e.stopPropagation();
    moon.classList.add('bloom');
    setTimeout(() => moon.classList.remove('bloom'), 700);
    moonTaps++;
    if (moonTaps >= 3) moonMsg.classList.add('show');
  });

  // Shooting stars
  function shoot() {
    const s = document.createElement('div');
    s.className = 'shooting-star';
    const startY = Math.random() * window.innerHeight * 0.5;
    const startX = window.innerWidth + 50;
    s.style.top = startY + 'px';
    s.style.left = startX + 'px';
    document.body.appendChild(s);
    const duration = 1200 + Math.random() * 600;
    s.animate([
      { transform: 'translate(0,0)', opacity: 1 },
      { transform: 'translate(-' + (window.innerWidth + 200) + 'px, ' + (150 + Math.random()*150) + 'px)', opacity: 0 }
    ], { duration, easing: 'ease-out' });
    setTimeout(() => s.remove(), duration);
    setTimeout(shoot, 5000 + Math.random() * 15000);
  }
  setTimeout(shoot, 3000);

  // Audio lullaby (Web Audio API)
  const btn = document.getElementById('audioBtn');
  let ctx, master, osc1, osc2, lfo, lfoGain, playing = false;
  btn.addEventListener('click', (e) => {
    e.stopPropagation();
    if (!playing) {
      ctx = ctx || new (window.AudioContext || window.webkitAudioContext)();
      master = ctx.createGain();
      master.gain.value = 0;
      master.connect(ctx.destination);

      osc1 = ctx.createOscillator();
      osc1.type = 'sine'; osc1.frequency.value = 220; // A3
      osc2 = ctx.createOscillator();
      osc2.type = 'sine'; osc2.frequency.value = 329.63; // E4

      const g1 = ctx.createGain(); g1.gain.value = 0.35;
      const g2 = ctx.createGain(); g2.gain.value = 0.2;

      osc1.connect(g1); g2.connect(master); g1.connect(master);
      osc2.connect(g2);

      // Slow LFO on master for gentle breathing
      lfo = ctx.createOscillator(); lfo.frequency.value = 0.1;
      lfoGain = ctx.createGain(); lfoGain.gain.value = 0.03;
      lfo.connect(lfoGain); lfoGain.connect(master.gain);

      osc1.start(); osc2.start(); lfo.start();
      master.gain.linearRampToValueAtTime(0.06, ctx.currentTime + 2);

      playing = true;
      btn.classList.add('playing');
    } else {
      master.gain.linearRampToValueAtTime(0, ctx.currentTime + 1);
      setTimeout(() => { osc1.stop(); osc2.stop(); lfo.stop(); }, 1100);
      playing = false;
      btn.classList.remove('playing');
    }
  });
</script>

</body>
</html>
 



