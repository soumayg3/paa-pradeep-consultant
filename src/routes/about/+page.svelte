<script>
  const credentials = [
    { icon: '🎓', title: 'IIT Roorkee', sub: 'B.E. Wood Science & Pulp and Paper Technology' },
    { icon: '🏅', title: 'Lean Six Sigma', sub: 'Green Belt Certified' },
    { icon: '📜', title: 'IMS Internal Auditor', sub: 'Integrated Management Systems' },
    { icon: '🏛️', title: 'Independent Director', sub: 'Indian Institute of Corporate Affairs' },
  ];

  const timeline = [
    { period: '1996–2008', org: 'Hindustan Paper Corporation Ltd', role: 'Asst / Shift Superintendent → Shift Superintendent', desc: 'Over 12 years across Nagaon and Hailakandi mills — pulp mill operations, quality control, central laboratory, planning & development, and OHSAS 18000 implementation.' },
    { period: '2008–2010', org: 'Hindustan Newsprint Limited', role: 'Senior Shift Superintendent', desc: 'Managed shift operations in Pulp Mill at Kottayam, Kerala. Led HIRA documentation for Soda Recovery during OHSAS 18000 implementation.' },
    { period: '2010–2019', org: 'Hindustan Paper Corporation Ltd', role: 'Senior Shift Superintendent → Manager', desc: 'Returned to Hailakandi as Sectional Head. Drove continuous improvement in quality output, sustainable productivity, and operational efficiency.' },
    { period: '2019–Present', org: 'Independent Consultant', role: 'Consultant & Director', desc: 'Facilitating competitiveness in the MSME sector. Director at Palanhaar Solutions (Railways & Transport). Project Management Consultant at Ganpathi Plastic & Engineering.' },
    { period: '2026–Present', org: 'Indian Institute of Corporate Affairs', role: 'Independent Director', desc: 'Board-level governance work. Building resilient, sustainable corporates of global standards meeting Sustainable Development Goals.' },
  ];

  const pillars = [
    'Quality Management', 'ESG & Sustainability',
    'Corporate Governance', 'Operational Excellence',
    'ISO Standards', 'Lean & Six Sigma',
    'CSR & SDGs', 'Industry 4.0',
  ];
</script>

<svelte:head>
  <title>About — Pradeep Kumar Gupta</title>
  <meta name="description" content="IIT Roorkee alumnus, Lean Six Sigma Green Belt, and Independent Director with 25+ years in quality, ESG, and corporate governance." />
  <link rel="canonical" href="https://www.pradeepkumargupta.in/about" />
  <meta property="og:title" content="About — Pradeep Kumar Gupta" />
  <meta property="og:description" content="IIT Roorkee alumnus, Lean Six Sigma Green Belt, and Independent Director with 25+ years in quality, ESG, and corporate governance." />
  <meta property="og:url" content="https://www.pradeepkumargupta.in/about" />
  <meta name="twitter:title" content="About — Pradeep Kumar Gupta" />
  <meta name="twitter:description" content="IIT Roorkee alumnus, Lean Six Sigma Green Belt, and Independent Director with 25+ years in quality, ESG, and corporate governance." />
</svelte:head>

<main>
  <!-- ── Page Hero ── -->
  <section class="page-hero">
    <div class="hero-bg">
      <!-- Blueprint grid overlay -->
      <svg class="blueprint-grid" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <defs>
          <pattern id="about-grid" x="0" y="0" width="60" height="60" patternUnits="userSpaceOnUse">
            <path d="M60 0H0V60" fill="none" stroke="rgba(20,97,164,0.07)" stroke-width="0.8"/>
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#about-grid)"/>
      </svg>
      <!-- Accent circle -->
      <div class="hero-orb" aria-hidden="true"></div>
    </div>
    <div class="container hero-content">
      <span class="tag">About Me</span>
      <h1 class="section-title">A career built on <em>expertise</em></h1>
      <p class="hero-sub">
        25+ years in quality, sustainability, and governance — from the pulp mill floor
        to the boardroom.
      </p>
    </div>
  </section>

  <!-- ── Main About ── -->
  <section class="about-main">
    <div class="container grid">
      <div class="photo-col">
        <div class="photo-frame">
          <!-- Decorative corner marks -->
          <div class="corner tl" aria-hidden="true"></div>
          <div class="corner br" aria-hidden="true"></div>
          <img
            src="https://www.pradeepkumargupta.in/image.jpeg"
            alt="Pradeep Kumar Gupta – Business Consultant"
            loading="lazy"
          />
        </div>

        <div class="credential-cards">
          {#each credentials as c}
            <div class="cred-card">
              <div class="cred-icon">{c.icon}</div>
              <div>
                <div class="cred-title">{c.title}</div>
                <div class="cred-sub">{c.sub}</div>
              </div>
            </div>
          {/each}
        </div>
      </div>

      <div class="text-col">
        <div class="divider"></div>
        <p>
          With extensive experience in business consulting and strategic advisory, I help
          organisations achieve operational excellence, implement sustainable practices, and
          drive continuous improvement across all facets of their operations.
        </p>
        <p>
          My core expertise was forged over 23 years at Hindustan Paper Corporation Limited
          and Hindustan Newsprint Limited — managing pulp mill operations, quality control,
          and safety systems across plants in Assam and Kerala.
        </p>
        <p>
          Since 2019 I have served as an independent consultant and director, bringing that
          operational depth to MSME sector competitiveness, plastics, water treatment, and
          board-level governance. I am an alumnus of IIT Roorkee (B.E. Wood Science & Pulp
          and Paper Technology) and hold certifications in Lean Six Sigma, IMS Internal
          Auditing, Project Management, and Independent Directorship.
        </p>

        <div class="pillars">
          {#each pillars as p}
            <div class="pillar">
              <div class="pillar-dot"></div>
              {p}
            </div>
          {/each}
        </div>

        <div class="actions">
          <a href="/contact" class="btn btn-primary">Work With Me</a>
          <a href="/work" class="btn btn-outline">View Services</a>
        </div>
      </div>
    </div>
  </section>

  <!-- ── Career Timeline ── -->
  <section class="timeline-section">
    <div class="container">
      <div class="section-head">
        <div class="head-mark" aria-hidden="true">
          <svg width="48" height="12" viewBox="0 0 48 12" fill="none">
            <rect x="0" y="5" width="16" height="2" fill="var(--accent)" opacity="0.8"/>
            <rect x="20" y="5" width="6" height="2" fill="var(--accent)" opacity="0.4"/>
            <rect x="30" y="5" width="4" height="2" fill="var(--accent)" opacity="0.25"/>
          </svg>
        </div>
        <span class="tag">Career Journey</span>
        <h2 class="section-title">Building <em>expertise</em> over decades</h2>
        <div class="divider"></div>
      </div>

      <div class="timeline">
        {#each timeline as t}
          <div class="tl-item">
            <div class="tl-left">
              <div class="tl-period">{t.period}</div>
              <div class="tl-org">{t.org}</div>
            </div>
            <div class="tl-connector">
              <div class="tl-dot"></div>
              <div class="tl-line"></div>
            </div>
            <div class="tl-content">
              <h3>{t.role}</h3>
              <p>{t.desc}</p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ── Why Work With Me ── -->
  <section class="why-section">
    <div class="container">
      <div class="section-head">
        <span class="tag">Why Choose Me</span>
        <h2 class="section-title">Delivering <em>value</em> through expertise</h2>
        <div class="divider"></div>
      </div>
      <div class="why-grid">
        {#each [
          { icon: '🏆', title: 'Proven Track Record', desc: 'Over 25 years of hands-on experience with a documented history of measurable improvements in quality, safety, and sustainability.' },
          { icon: '💡', title: 'Operational Depth', desc: 'Recommendations grounded in real production-floor and boardroom experience — not just textbook frameworks.' },
          { icon: '👥', title: 'Partnership Approach', desc: 'Work alongside your team to build internal capability, not dependency. Engagements are built to create lasting change.' },
          { icon: '📊', title: 'Measurable Outcomes', desc: 'Every engagement defines clear KPIs upfront. Results are reported in business metrics that matter to leadership.' },
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
</main>

<style>
main { padding-top: 0; }

/* ── Hero — inherits light styles from app.css .page-hero ── */
.blueprint-grid { position: absolute; inset: 0; width: 100%; height: 100%; }
.hero-orb {
  position: absolute;
  right: -5%;
  top: 50%;
  transform: translateY(-50%);
  width: 600px;
  height: 600px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(20,97,164,0.06) 0%, transparent 65%);
}

/* ── About Main ── */
.about-main {
  padding-block: var(--section-pad);
  background: var(--off-white);
}
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(3rem, 6vw, 6rem);
  align-items: start;
}

.photo-col { display: flex; flex-direction: column; gap: 1.5rem; }
.photo-frame {
  position: relative;
  border-radius: 6px;
  overflow: visible;
}
/* Engineering corner marks */
.corner {
  position: absolute;
  width: 20px;
  height: 20px;
  z-index: 1;
}
.corner.tl { top: -6px; left: -6px; border-top: 2px solid var(--accent); border-left: 2px solid var(--accent); }
.corner.br { bottom: -6px; right: -6px; border-bottom: 2px solid var(--accent); border-right: 2px solid var(--accent); }
.photo-frame img {
  width: 100%;
  aspect-ratio: 4/5;
  object-fit: cover;
  object-position: top;
  border-radius: 6px;
  filter: grayscale(15%) contrast(1.05);
  transition: filter 0.4s;
  display: block;
}
.photo-frame:hover img { filter: none; }

.credential-cards { display: flex; flex-direction: column; gap: 0.85rem; }
.cred-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  background: var(--navy);
  color: #fff;
  border-radius: var(--radius);
  padding: 0.85rem 1.2rem;
  border-left: 3px solid var(--accent);
}
.cred-icon { font-size: 1.25rem; flex-shrink: 0; }
.cred-title { font-family: var(--font-display); font-size: 1rem; font-weight: 400; color: var(--accent-light); }
.cred-sub { font-size: 0.72rem; color: rgba(255,255,255,0.5); margin-top: 0.1rem; letter-spacing: 0.04em; }

.head-mark { margin-bottom: 0.75rem; }
.text-col p { color: var(--muted); font-size: 0.97rem; line-height: 1.8; margin-top: 1rem; }

.pillars {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.65rem;
  margin-top: 1.75rem;
}
.pillar {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  font-size: 0.82rem;
  font-weight: 500;
  color: var(--navy);
  letter-spacing: 0.02em;
}
.pillar-dot {
  width: 5px; height: 5px;
  border-radius: 50%;
  background: var(--accent);
  flex-shrink: 0;
}
.actions { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 2rem; }

/* ── Timeline ── */
.timeline-section {
  padding-block: var(--section-pad);
  background: var(--off-white);
}

.timeline { display: flex; flex-direction: column; gap: 0; }

.tl-item {
  display: grid;
  grid-template-columns: 200px 32px 1fr;
  gap: 0 1.5rem;
  align-items: start;
  padding-block: 1.75rem 0;
}
.tl-left { text-align: right; padding-top: 0.1rem; }
.tl-period {
  font-family: var(--font-display);
  font-size: 0.82rem;
  color: var(--accent);
  letter-spacing: 0.06em;
  margin-bottom: 0.25rem;
}
.tl-org {
  font-size: 0.7rem;
  letter-spacing: 0.06em;
  color: var(--muted);
  text-transform: uppercase;
}
.tl-connector {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 0.1rem;
}
.tl-dot {
  width: 12px; height: 12px;
  border-radius: 50%;
  background: var(--accent);
  border: 2px solid var(--navy);
  outline: 1.5px solid var(--accent);
  flex-shrink: 0;
  z-index: 1;
}
.tl-line {
  flex: 1;
  width: 1px;
  min-height: 3rem;
  background: var(--border);
  margin-top: 4px;
}
.tl-item:last-child .tl-line { display: none; }
.tl-content { padding-bottom: 1.75rem; }
.tl-content h3 {
  font-family: var(--font-display);
  font-size: 1.05rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.4rem;
  line-height: 1.3;
}
.tl-content p { font-size: 0.85rem; color: var(--muted); line-height: 1.75; }

/* ── Why ── */
.why-section {
  padding-block: var(--section-pad);
  background: var(--off-white);
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
  bottom: -20px;
  right: -20px;
  width: 80px;
  height: 80px;
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

@media (max-width: 900px) {
  .grid { grid-template-columns: 1fr; }
  .photo-col { max-width: 420px; }
  .tl-item { grid-template-columns: 120px 28px 1fr; gap: 0 1rem; }
  .tl-org { display: none; }
}
@media (max-width: 560px) {
  .tl-item { grid-template-columns: 1fr; }
  .tl-left { text-align: left; }
  .tl-connector { display: none; }
  .tl-content { padding-bottom: 1.5rem; }
}
</style>
