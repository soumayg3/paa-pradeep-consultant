<section id="home">
  <div class="hero-bg">
    <div class="overlay"></div>
    <svg class="dot-grid" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
      <defs>
        <pattern id="hero-dots" x="0" y="0" width="36" height="36" patternUnits="userSpaceOnUse">
          <circle cx="2" cy="2" r="1.5" fill="rgba(20,97,164,0.055)"/>
        </pattern>
      </defs>
      <rect width="100%" height="100%" fill="url(#hero-dots)"/>
    </svg>
  </div>

  <div class="shapes" aria-hidden="true">
    <div class="shape ring-lg"></div>
    <div class="shape ring-sm"></div>
    <div class="shape rect-tilt"></div>
    <div class="shape bracket-r">
      <svg viewBox="0 0 60 120" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M20 8 L8 8 L8 112 L20 112" stroke="rgba(20,97,164,0.2)" stroke-width="1.5"/>
        <path d="M40 30 L52 30 L52 90 L40 90" stroke="rgba(20,97,164,0.1)" stroke-width="1"/>
      </svg>
    </div>
    <div class="accent-line"></div>
  </div>

  <div class="container hero-content">
    <div class="eyebrow">
      <span class="line"></span>
      <span class="eyebrow-text">Independent Director &amp; Business Consultant</span>
    </div>

    <h1>
      <span class="name">Pradeep Kumar</span>
      <span class="surname">Gupta</span>
    </h1>

    <p class="tagline">
      Building resilient, sustainable organisations through expertise in Quality Management,
      ESG, Corporate Governance, and Operational Excellence.
    </p>

    <div class="hero-actions">
      <a href="/contact" class="btn btn-primary">Get In Touch</a>
      <a href="/about" class="btn btn-outline-dark">Learn More</a>
    </div>

    <div class="stats">
      {#each [['25+','Years Experience'],['50+','Projects Completed']] as [num, label]}
        <div class="stat">
          <span class="stat-num">{num}</span>
          <span class="stat-label">{label}</span>
        </div>
      {/each}
    </div>
  </div>

  <div class="scroll-hint" aria-hidden="true">
    <span>Scroll</span>
    <div class="scroll-line"></div>
  </div>
</section>

<style>
section {
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(140deg, #EDF3FB 0%, #F4F8FD 55%, #E8F0FA 100%);
}
.overlay {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 55% 70% at 85% 45%, rgba(20,97,164,0.07) 0%, transparent 70%),
    radial-gradient(ellipse 40% 60% at 5% 80%, rgba(20,97,164,0.04) 0%, transparent 60%);
}
.dot-grid {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
}

.shapes {
  position: absolute;
  inset: 0;
  pointer-events: none;
  overflow: hidden;
}
.shape { position: absolute; }

.ring-lg {
  width: 520px;
  height: 520px;
  border: 1px solid rgba(20,97,164,0.07);
  border-radius: 50%;
  top: -12%;
  right: 6%;
  animation: slowSpin 90s linear infinite;
}
.ring-lg::after {
  content: '';
  position: absolute;
  inset: 24px;
  border: 1px solid rgba(20,97,164,0.05);
  border-radius: 50%;
}
.ring-sm {
  width: 220px;
  height: 220px;
  border: 1px solid rgba(20,97,164,0.12);
  border-radius: 50%;
  top: 38%;
  right: 18%;
  animation: slowSpinRev 55s linear infinite;
}
.ring-sm::after {
  content: '';
  position: absolute;
  top: 50%; left: 50%;
  width: 6px; height: 6px;
  border-radius: 50%;
  background: rgba(20,97,164,0.25);
  transform: translate(-50%,-50%);
}
.rect-tilt {
  width: 140px;
  height: 140px;
  border: 1px solid rgba(20,97,164,0.1);
  transform: rotate(28deg);
  bottom: 18%;
  right: 10%;
  animation: slowSpin 70s linear infinite;
}
.bracket-r {
  width: 60px;
  height: 120px;
  right: 4%;
  top: 50%;
  transform: translateY(-50%);
}
.accent-line {
  position: absolute;
  left: 0;
  top: 55%;
  width: 45%;
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(20,97,164,0.15), transparent);
}

@keyframes slowSpin    { to { transform: rotate(360deg); } }
@keyframes slowSpinRev { to { transform: rotate(-360deg); } }

.hero-content {
  position: relative;
  z-index: 2;
  padding-top: 8rem;
  padding-bottom: 6rem;
}

.eyebrow {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.75rem;
  animation: fadeUp 0.9s ease both;
}
.line {
  display: block;
  width: 3rem;
  height: 1px;
  background: var(--accent);
}
.eyebrow-text {
  font-size: 0.68rem;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 500;
}

h1 {
  font-family: var(--font-display);
  font-weight: 300;
  line-height: 1;
  margin-bottom: 1.5rem;
  animation: fadeUp 0.9s 0.1s ease both;
}
.name {
  display: block;
  font-size: clamp(3rem, 8vw, 7rem);
  color: var(--navy);
}
.surname {
  display: block;
  font-size: clamp(3rem, 8vw, 7rem);
  color: var(--logo-gold);
  font-style: italic;
}

.tagline {
  font-size: clamp(0.95rem, 1.5vw, 1.1rem);
  color: var(--muted);
  max-width: 55ch;
  line-height: 1.75;
  margin-bottom: 2.5rem;
  animation: fadeUp 0.9s 0.2s ease both;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 4rem;
  animation: fadeUp 0.9s 0.3s ease both;
}
.btn-outline-dark {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-family: var(--font-body);
  font-size: 0.78rem;
  font-weight: 500;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  padding: 0.85em 2.2em;
  border-radius: var(--radius);
  cursor: pointer;
  transition: all 0.25s ease;
  background: transparent;
  color: var(--navy);
  border: 1px solid rgba(11,28,45,0.3);
}
.btn-outline-dark:hover {
  background: var(--navy);
  color: #fff;
  border-color: var(--navy);
  transform: translateY(-2px);
}

.stats {
  display: flex;
  gap: clamp(2rem, 5vw, 4rem);
  animation: fadeUp 0.9s 0.4s ease both;
  padding-top: 2rem;
  border-top: 1px solid var(--border);
}
.stat { display: flex; flex-direction: column; }
.stat-num {
  font-family: var(--font-display);
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 300;
  color: var(--accent);
  line-height: 1;
}
.stat-label {
  font-size: 0.68rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  margin-top: 0.3rem;
}

.scroll-hint {
  position: absolute;
  bottom: 2.5rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  color: var(--muted);
  font-size: 0.6rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  z-index: 2;
}
.scroll-line {
  width: 1px;
  height: 3rem;
  background: linear-gradient(to bottom, var(--accent), transparent);
  animation: scrollPulse 2s ease infinite;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes scrollPulse {
  0%,100% { opacity: 0.4; transform: scaleY(0.8); }
  50%      { opacity: 1;   transform: scaleY(1); }
}
</style>
