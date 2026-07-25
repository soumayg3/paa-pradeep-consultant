<script>
  const credentials = [
    { icon: '🎓', title: 'IIT Roorkee', sub: 'B.E. Wood Science & Pulp and Paper Technology' },
    { icon: '🏅', title: 'Lean Six Sigma', sub: 'Green Belt Certified' },
    { icon: '📜', title: 'IMS Internal Auditor', sub: 'Integrated Management Systems' },
    { icon: '🏛️', title: 'Board Readiness', sub: 'Independent director education / credential' },
  ];

  const timeline = [
    { period: '1996–2008', org: 'Hindustan Paper Corporation Ltd', role: 'Asst / Shift Superintendent → Shift Superintendent', desc: 'Over 12 years across Nagaon and Hailakandi mills — pulp mill operations, quality control, central laboratory, planning & development, and OHSAS 18001 implementation.' },
    { period: '2008–2010', org: 'Hindustan Newsprint Limited', role: 'Senior Shift Superintendent', desc: 'Managed shift operations in Pulp Mill at Kottayam, Kerala. Led HIRA documentation for Soda Recovery during OHSAS 18001 implementation.' },
    { period: '2010–2019', org: 'Hindustan Paper Corporation Ltd', role: 'Senior Shift Superintendent → Manager', desc: 'Returned to Hailakandi as Sectional Head. Drove continuous improvement in quality output, sustainable productivity, and operational efficiency.' },
    { period: '2019–Present', org: 'Independent Practice', role: 'Consultant & Director', desc: 'Supporting MSME competitiveness and management improvement, with assignments in plastics, engineering, water systems, railways and transport.' },
    { period: 'Current focus', org: 'Board & International Opportunities', role: 'Independent Director Candidate · Technical / Quality Leader', desc: 'Seeking board mandates and international roles where manufacturing, quality, safety and sustainability experience can strengthen oversight and execution.' },
  ];

  const pillars = [
    'Quality Management', 'ESG & Sustainability',
    'Corporate Governance', 'Operational Excellence',
    'ISO Standards', 'Lean & Six Sigma',
    'CSR & SDGs', 'Industry 4.0',
  ];
</script>

<svelte:head>
  <title>Career Profile | Pradeep Kumar Gupta — Pulp & Paper and Quality Leader</title>
  <meta name="description" content="Career profile of Pradeep Kumar Gupta: IIT Roorkee pulp and paper technologist with 25+ years in mill operations, quality control, safety systems, TQM and MSME consulting." />
  <link rel="canonical" href="https://www.pradeepkumargupta.in/about" />
  <meta property="og:title" content="About — Pradeep Kumar Gupta" />
  <meta property="og:description" content="IIT Roorkee pulp and paper technologist with 25+ years in mill operations, quality control, safety systems, TQM and MSME consulting." />
  <meta property="og:url" content="https://www.pradeepkumargupta.in/about" />
  <meta name="twitter:title" content="About — Pradeep Kumar Gupta" />
  <meta name="twitter:description" content="25+ years in pulp and paper operations, quality, safety systems and MSME consulting." />
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
        25+ years across mill operations, quality, safety and business improvement —
        now available for board, consulting and international leadership mandates.
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
            src="/pradeep-kumar-gupta-full.webp"
            alt="Pradeep Kumar Gupta, pulp and paper technologist and quality leader"
            width="800"
            height="1200"
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
          I am a pulp and paper technologist and quality professional whose career has been built
          in operating environments where safety, consistency, cost and production continuity
          must work together.
        </p>
        <p>
          My core expertise was forged over 23 years at Hindustan Paper Corporation Limited
          and Hindustan Newsprint Limited — managing pulp mill operations, quality control,
          and safety systems across plants in Assam and Kerala.
        </p>
        <p>
          Since 2019 I have brought that operating discipline to MSMEs and assignments in
          plastics, engineering, water treatment, railways and transport. My approach combines
          TQM, Lean Six Sigma, structured problem solving and management-system thinking with
          practical implementation alongside the client team.
        </p>
        <p>
          I am an IIT Roorkee alumnus (B.E. Wood Science &amp; Pulp and Paper Technology), a
          Lean Six Sigma Green Belt and an IMS internal auditor. I welcome independent director
          and advisory mandates, project-based consulting, and suitable pulp-and-paper or quality
          leadership roles outside India.
        </p>

        <div class="pillars">
          {#each pillars as p}
            <div class="pillar">
              <div class="pillar-dot"></div>
              {p}
            </div>
          {/each}
        </div>

        <div class="actions" id="print-profile">
          <a href="/contact" class="btn btn-primary">Discuss a role or mandate</a>
          <button type="button" class="btn btn-outline" on:click={() => window.print()}>Print / Save as PDF</button>
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
        <span class="tag">Recruiter Assessment</span>
        <h2 class="section-title">What distinguishes the <em>profile</em></h2>
        <div class="divider"></div>
      </div>
      <div class="why-grid">
        {#each [
          { icon: '🏆', title: 'Career Evidence', desc: 'More than 25 years across operating companies and consulting, including 23 years in pulp and paper organisations.' },
          { icon: '💡', title: 'Operational Depth', desc: 'Recommendations grounded in real production-floor leadership and governance discipline — not just textbook frameworks.' },
          { icon: '👥', title: 'Partnership Approach', desc: 'Work alongside your team to build internal capability, not dependency. Engagements are built to create lasting change.' },
          { icon: '📊', title: 'Measured Delivery', desc: 'Engagements begin with a baseline and agreed KPIs, then build ownership through reviews, training and standardisation.' },
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
.page-hero { padding-block: 6.5rem 3.25rem; }

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
  padding-block: clamp(2.5rem, 5vw, 4rem);
  background: var(--off-white);
}
.grid {
  display: grid;
  grid-template-columns: minmax(250px, 0.78fr) minmax(0, 1.22fr);
  gap: clamp(2rem, 4vw, 4rem);
  align-items: start;
}

.photo-col { display: flex; flex-direction: column; gap: 1rem; max-width: 360px; }
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
  height: auto;
  border-radius: 6px;
  filter: grayscale(15%) contrast(1.05);
  transition: filter 0.4s;
  display: block;
}
.photo-frame:hover img { filter: none; }

.credential-cards { display: grid; grid-template-columns: 1fr 1fr; gap: 0.55rem; }
.cred-card {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  background: #2F6F8F;
  color: #fff;
  border-radius: var(--radius);
  padding: 0.65rem 0.75rem;
  border-left: 3px solid var(--accent);
}
.cred-card:nth-child(2) { background: #4F7C70; }
.cred-card:nth-child(3) { background: #6D7187; }
.cred-card:nth-child(4) { background: #9A6A32; }
.cred-icon { font-size: 1rem; flex-shrink: 0; }
.cred-title { font-family: var(--font-display); font-size: 0.86rem; line-height: 1.2; font-weight: 600; color: #FFFFFF; }
.cred-sub { font-size: 0.59rem; line-height: 1.35; color: rgba(255,255,255,0.9); margin-top: 0.08rem; letter-spacing: 0.02em; }

.head-mark { margin-bottom: 0.75rem; }
.text-col p { color: var(--muted); font-size: 0.88rem; line-height: 1.65; margin-top: 0.75rem; }
.text-col .divider { margin-block: 0 1rem; }

.pillars {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.45rem;
  margin-top: 1.15rem;
}
.pillar {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  font-size: 0.74rem;
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
.actions { display: flex; gap: 0.75rem; flex-wrap: wrap; margin-top: 1.25rem; }

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
  background: #EAF2F7;
  border-radius: 6px;
  padding: 2rem 1.75rem;
  color: var(--navy);
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
  color: var(--navy);
  margin-bottom: 0.6rem;
}
.why-card p { font-size: 0.84rem; color: #344B5D; line-height: 1.7; }
.why-card:nth-child(2) p { color: #38584F; }
.why-card:nth-child(3) p { color: #5D4A31; }
.why-card:nth-child(4) p { color: #454B66; }
.why-card:nth-child(2) { background: #EDF3EF; }
.why-card:nth-child(3) { background: #F4EFE5; }
.why-card:nth-child(4) { background: #EEF0F6; }

@media (max-width: 900px) {
  .grid { grid-template-columns: 1fr; }
  .photo-col { max-width: 420px; }
  .tl-item { grid-template-columns: 120px 28px 1fr; gap: 0 1rem; }
  .tl-org { display: none; }
}
@media (max-width: 560px) {
  .credential-cards { grid-template-columns: 1fr; }
  .tl-item { grid-template-columns: 1fr; }
  .tl-left { text-align: left; }
  .tl-connector { display: none; }
  .tl-content { padding-bottom: 1.5rem; }
}
</style>
