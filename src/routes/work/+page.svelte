<script>
  import { services } from '$lib/data/services.js';
</script>

<svelte:head>
  <title>Work & Services — Pradeep Kumar Gupta</title>
  <meta name="description" content="11 consulting service domains — Quality Improvement, ESG, Corporate Strategy, QMS, ISO Compliance, and more. 25+ years of hands-on industry experience." />
  <link rel="canonical" href="https://www.pradeepkumargupta.in/work" />
  <meta property="og:title" content="Work & Services — Pradeep Kumar Gupta" />
  <meta property="og:description" content="11 consulting service domains — Quality Improvement, ESG, Corporate Strategy, QMS, ISO Compliance, and more." />
  <meta property="og:url" content="https://www.pradeepkumargupta.in/work" />
  <meta name="twitter:title" content="Work & Services — Pradeep Kumar Gupta" />
  <meta name="twitter:description" content="11 consulting service domains — Quality Improvement, ESG, Corporate Strategy, QMS, ISO Compliance, and more." />
</svelte:head>

<main>
  <!-- ── Page Hero ── -->
  <section class="page-hero">
    <div class="hero-bg">
      <svg class="grid-pattern" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <defs>
          <pattern id="work-grid" x="0" y="0" width="60" height="60" patternUnits="userSpaceOnUse">
            <path d="M60 0H0V60" fill="none" stroke="rgba(20,97,164,0.07)" stroke-width="0.8"/>
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#work-grid)"/>
      </svg>
      <div class="hero-orb"></div>
    </div>
    <div class="container hero-content">
      <!-- Bracket graphic -->
      <div class="bracket-mark" aria-hidden="true">
        <svg viewBox="0 0 80 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 0 L0 24 L12 24" stroke="rgba(20,97,164,0.35)" stroke-width="1.5"/>
          <path d="M80 0 L80 24 L68 24" stroke="rgba(20,97,164,0.2)" stroke-width="1"/>
        </svg>
      </div>
      <span class="tag">Services</span>
      <h1 class="section-title">Work & <em>Expertise</em></h1>
      <p class="hero-sub">
        Eleven service domains grounded in 25+ years of operational and consulting experience —
        delivered as a genuine partnership with your team.
      </p>
      <div class="hero-count" aria-hidden="true">
        <span class="count-num">11</span>
        <span class="count-label">Service Domains</span>
      </div>
    </div>
  </section>

  <!-- ── Services Grid ── -->
  <section class="services-section">
    <div class="container">
      <!-- Count rule -->
      <div class="grid-header">
        <div class="grid-rule" aria-hidden="true">
          <svg width="100%" height="1" preserveAspectRatio="none">
            <line x1="0" y1="0" x2="100%" y2="0" stroke="var(--border)" stroke-width="1"/>
          </svg>
        </div>
        <span class="grid-count">{services.length} services</span>
      </div>

      <div class="grid">
        {#each services as s, i}
          <a href="/work/{s.slug}" class="card">
            <div class="card-index" aria-hidden="true">{String(i + 1).padStart(2, '0')}</div>
            <span class="card-icon">{s.icon}</span>
            <div class="card-body">
              <h3>{s.title}</h3>
              <p class="tagline">{s.tagline}</p>
              <p class="desc">{s.desc}</p>
            </div>
            <span class="card-arrow">
              <svg viewBox="0 0 20 12" fill="none" xmlns="http://www.w3.org/2000/svg" width="20" height="12">
                <path d="M1 6h18M13 1l6 5-6 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </span>
          </a>
        {/each}
      </div>
    </div>
  </section>

  <!-- ── Why Choose Me ── -->
  <section class="why-section">
    <div class="container">
      <div class="section-head">
        <span class="tag">Why Choose Me</span>
        <h2 class="section-title">Delivering <em>value</em> through expertise</h2>
        <div class="divider"></div>
      </div>
      <div class="why-grid">
        {#each [
          { icon: '🏆', title: 'Proven Expertise',        desc: 'Decades of industry experience with a track record of successful, measurable implementations.' },
          { icon: '💡', title: 'Practical Solutions',     desc: 'Recommendations built on operational depth — not just frameworks and slides.' },
          { icon: '👥', title: 'Client-Centric',          desc: 'Dedicated partnership focused on understanding and achieving your specific business objectives.' },
          { icon: '📊', title: 'Measurable Results',      desc: 'Data-driven strategies reported in business KPIs that matter to leadership.' },
        ] as w}
          <div class="why-card">
            <span class="why-icon">{w.icon}</span>
            <h4>{w.title}</h4>
            <p>{w.desc}</p>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ── CTA ── -->
  <section class="cta-band">
    <div class="cta-bg" aria-hidden="true">
      <svg xmlns="http://www.w3.org/2000/svg" class="cta-mesh">
        <defs>
          <pattern id="cta-dots" x="0" y="0" width="36" height="36" patternUnits="userSpaceOnUse">
            <circle cx="2" cy="2" r="1.2" fill="rgba(255,255,255,0.08)"/>
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#cta-dots)"/>
      </svg>
    </div>
    <div class="container cta-inner">
      <div>
        <h2 class="section-title" style="color:#fff">Not sure where to <em>start?</em></h2>
        <p>A free consultation will identify the highest-impact areas for your organisation.</p>
      </div>
      <a href="/contact" class="btn btn-primary">Get In Touch</a>
    </div>
  </section>
</main>

<style>
main { padding-top: 0; }

/* ── Hero — inherits light styles from app.css .page-hero ── */
.grid-pattern, .cta-mesh { position: absolute; inset: 0; width: 100%; height: 100%; }
.hero-orb {
  position: absolute;
  right: -8%;
  top: 50%;
  transform: translateY(-50%);
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(20,97,164,0.06) 0%, transparent 65%);
}
.bracket-mark { margin-bottom: 1rem; }
.bracket-mark svg { width: 80px; height: 24px; }

.hero-count {
  display: flex;
  align-items: baseline;
  gap: 0.75rem;
  margin-top: 2rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--border);
}
.count-num {
  font-family: var(--font-display);
  font-size: 2rem;
  font-weight: 300;
  color: var(--accent);
  line-height: 1;
}
.count-label {
  font-size: 0.72rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--muted);
}

/* ── Grid ── */
.services-section {
  padding-block: var(--section-pad);
  background: var(--off-white);
}
.grid-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 2rem;
}
.grid-rule { flex: 1; }
.grid-count {
  font-size: 0.72rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  white-space: nowrap;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(300px,100%), 1fr));
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
}
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  background: var(--white);
  padding: 1.75rem;
  transition: background 0.2s;
  color: var(--text);
}
.card:hover { background: var(--off-white); }
.card:hover .card-arrow { transform: translateX(4px); color: var(--accent); }

.card-index {
  position: absolute;
  top: 1rem; right: 1.25rem;
  font-family: var(--font-display);
  font-size: 1.8rem;
  font-weight: 300;
  color: rgba(20,97,164,0.08);
  line-height: 1;
}
.card-icon { font-size: 1.75rem; margin-bottom: 0.85rem; display: block; }
.card-body { flex: 1; margin-bottom: 1.5rem; }
.card h3 {
  font-family: var(--font-display);
  font-size: 1.12rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.2rem;
}
.tagline {
  font-size: 0.7rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 0.65rem;
  font-weight: 500;
}
.desc { font-size: 0.84rem; color: var(--muted); line-height: 1.7; }
.card-arrow {
  color: var(--muted);
  transition: transform 0.2s, color 0.2s;
  align-self: flex-end;
}

/* ── Why ── */
.why-section {
  padding-block: var(--section-pad);
  background: var(--cream);
}
.why-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 1.5rem;
}
.why-card {
  background: var(--navy);
  border-radius: 6px;
  padding: 2rem 1.75rem;
  color: #fff;
  border-top: 3px solid var(--accent);
  position: relative;
  overflow: hidden;
}
.why-card::after {
  content: '';
  position: absolute;
  bottom: -20px; right: -20px;
  width: 80px; height: 80px;
  border: 1px solid rgba(20,97,164,0.15);
  border-radius: 50%;
  pointer-events: none;
}
.why-icon { font-size: 2rem; display: block; margin-bottom: 1rem; }
.why-card h4 {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 400;
  color: var(--accent-light);
  margin-bottom: 0.6rem;
}
.why-card p { font-size: 0.84rem; color: rgba(255,255,255,0.55); line-height: 1.7; }

/* ── CTA ── */
.cta-band {
  position: relative;
  padding-block: var(--section-pad);
  background: var(--accent);
  overflow: hidden;
}
.cta-bg { position: absolute; inset: 0; pointer-events: none; }
.cta-inner {
  position: relative;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 3rem;
  flex-wrap: wrap;
}
.cta-inner p {
  color: rgba(255,255,255,0.78);
  font-size: 0.97rem;
  margin-top: 0.75rem;
}
</style>
