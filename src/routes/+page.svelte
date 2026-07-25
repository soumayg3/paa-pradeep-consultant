<script>
  import Hero from '$lib/components/Hero.svelte';

  const featured = [
    { icon: '🏛️', title: 'Board & Governance', href: '/work/board-advisory', desc: 'An independent, operations-informed perspective on risk, quality, sustainability and long-term value.' },
    { icon: '⚙️', title: 'MSME Operational Excellence', href: '/work/quality-improvement', desc: 'TQM, Lean, Six Sigma and root-cause problem solving adapted to the realities of growing manufacturers.' },
    { icon: '🏭', title: 'Pulp & Paper Technology', href: '/work/pulp-paper-industry', desc: 'Leadership and technical support spanning pulp operations, quality control, laboratory, safety and improvement.' },
    { icon: '📋', title: 'QMS & ISO Systems', href: '/work/qms-implementation', desc: 'Practical management systems, internal audits, capability building and certification readiness.' },
  ];

  const stats = [
    { num: '25+', label: 'Years of experience', sub: 'Operations, quality and consulting' },
    { num: '23', label: 'Years in paper companies', sub: 'HPC and Hindustan Newsprint' },
    { num: '3', label: 'Ways to engage', sub: 'Board · Consulting · Leadership role' },
  ];

  const roleFit = [
    { label: 'Board mandates', value: 'Independent Director · Board Adviser', note: 'Manufacturing, MSME, quality, safety and sustainability oversight' },
    { label: 'Permanent roles', value: 'Technical / Quality / Operational Excellence Leader', note: 'Pulp & paper and process manufacturing; India or international' },
    { label: 'Consulting', value: 'TQM · Lean Six Sigma · QMS · Mill Improvement', note: 'Diagnostic, implementation and capability-building assignments' },
  ];

  const evidence = [
    '23 years with Hindustan Paper Corporation and Hindustan Newsprint',
    'Progressed from Assistant / Shift Superintendent to Manager and Sectional Head',
    'Experience across Assam and Kerala mill operations',
    'Pulp operations, quality control, central laboratory, planning and safety systems',
    'IIT Roorkee engineering alumnus; Lean Six Sigma Green Belt; IMS internal auditor',
    'Independent consulting practice since 2019',
  ];
</script>

<svelte:head>
  <title>Pradeep Kumar Gupta | Independent Director Candidate, Pulp & Paper & Quality Leader</title>
  <meta name="description" content="IIT Roorkee pulp and paper technologist with 25+ years in mill operations, quality, TQM, Lean Six Sigma and MSME improvement. Open to board, consulting and international leadership opportunities." />
  <link rel="canonical" href="https://www.pradeepkumargupta.in/" />
  <meta property="og:title" content="Pradeep Kumar Gupta | Board, Quality & Pulp and Paper Leader" />
  <meta property="og:description" content="25+ years across pulp and paper operations, quality systems and MSME consulting. Available for board, consulting and international leadership opportunities." />
  <meta property="og:url" content="https://www.pradeepkumargupta.in/" />
  <meta name="twitter:title" content="Pradeep Kumar Gupta | Board, Quality & Pulp and Paper Leader" />
  <meta name="twitter:description" content="25+ years across pulp and paper operations, quality systems and MSME consulting." />
</svelte:head>

<main>
  <Hero />

  <section class="snapshot">
    <div class="container">
      <div class="snapshot-head">
        <div>
          <span class="tag">Recruiter Snapshot</span>
          <h2 class="section-title">Fit at a <em>glance</em></h2>
        </div>
        <a href="/about#print-profile" class="btn btn-outline">Print / save career profile</a>
      </div>

      <div class="snapshot-grid">
        <div class="role-list">
          {#each roleFit as role}
            <article class="role-row">
              <span>{role.label}</span>
              <div>
                <h3>{role.value}</h3>
                <p>{role.note}</p>
              </div>
            </article>
          {/each}
        </div>
        <aside class="evidence-card">
          <h3>Evidence behind the profile</h3>
          <ul>
            {#each evidence as item}<li>{item}</li>{/each}
          </ul>
        </aside>
      </div>
    </div>
  </section>

  <!-- ── Featured Services ── -->
  <section class="featured">
    <div class="container">
      <!-- Section header with accent mark -->
      <div class="section-head">
        <div class="head-mark" aria-hidden="true">
          <svg width="48" height="12" viewBox="0 0 48 12" fill="none">
            <rect x="0" y="5" width="16" height="2" fill="var(--accent)" opacity="0.8"/>
            <rect x="20" y="5" width="6" height="2" fill="var(--accent)" opacity="0.4"/>
            <rect x="30" y="5" width="4" height="2" fill="var(--accent)" opacity="0.25"/>
          </svg>
        </div>
        <span class="tag">Opportunity Fit</span>
        <h2 class="section-title">Experience aligned to <em>three mandates</em></h2>
        <p class="section-sub">
          A focused proposition for boards, manufacturing businesses and employers seeking
          mature technical leadership grounded in real operating experience.
        </p>
      </div>

      <div class="cards">
        {#each featured as s, i}
          <a href={s.href} class="card">
            <div class="card-corner" aria-hidden="true"></div>
            <span class="card-num">0{i + 1}</span>
            <span class="card-icon">{s.icon}</span>
            <h3>{s.title}</h3>
            <p>{s.desc}</p>
            <span class="card-link">
              View details
              <svg width="14" height="10" viewBox="0 0 14 10" fill="none" aria-hidden="true">
                <path d="M1 5h12M8 1l5 4-5 4" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </span>
          </a>
        {/each}
      </div>

      <div class="all-cta">
        <a href="/work" class="btn btn-outline">Explore capabilities</a>
      </div>
    </div>
  </section>

  <!-- ── Stats / Social Proof ── -->
  <section class="proof">
    <div class="container">
      <div class="proof-header">
        <div class="proof-rule" aria-hidden="true">
          <svg width="100%" height="24" viewBox="0 0 800 24" preserveAspectRatio="none" fill="none">
            <line x1="0" y1="12" x2="800" y2="12" stroke="var(--border)" stroke-width="1" stroke-dasharray="4 6"/>
            <circle cx="0" cy="12" r="3" fill="var(--accent)" opacity="0.4"/>
            <circle cx="800" cy="12" r="3" fill="var(--accent)" opacity="0.4"/>
          </svg>
        </div>
        <span class="tag proof-tag">Track Record</span>
      </div>

      <div class="proof-grid">
        {#each stats as s, i}
          <div class="proof-item">
            <!-- SVG arc ring graphic -->
            <div class="ring-wrap">
              <svg viewBox="0 0 96 96" class="ring-svg" aria-hidden="true">
                <circle cx="48" cy="48" r="42" fill="none" stroke="rgba(20,97,164,0.1)" stroke-width="1.5"/>
                <circle cx="48" cy="48" r="42" fill="none" stroke="rgba(20,97,164,0.45)" stroke-width="1.5"
                  stroke-dasharray="{i === 0 ? 180 : i === 1 ? 220 : i === 2 ? 200 : 120} 264"
                  stroke-linecap="round" transform="rotate(-90 48 48)"/>
                <!-- tick marks -->
                {#each [0, 60, 120, 180, 240, 300] as angle}
                  <line
                    x1="48" y1="6"
                    x2="48" y2="10"
                    stroke="rgba(20,97,164,0.2)"
                    stroke-width="1"
                    transform="rotate({angle} 48 48)"
                  />
                {/each}
              </svg>
              <div class="proof-num">{s.num}</div>
            </div>
            <div class="proof-label">{s.label}</div>
            <div class="proof-sub">{s.sub}</div>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ── CTA band ── -->
  <section class="cta-band">
    <!-- Background graphic -->
    <div class="cta-bg" aria-hidden="true">
      <svg class="cta-mesh" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <pattern id="cta-grid" x="0" y="0" width="48" height="48" patternUnits="userSpaceOnUse">
            <path d="M48 0H0V48" fill="none" stroke="rgba(255,255,255,0.07)" stroke-width="0.8"/>
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#cta-grid)"/>
      </svg>
      <div class="cta-orb"></div>
    </div>

    <div class="container cta-inner">
      <div class="cta-text">
        <h2 class="section-title" style="color:#fff">Have a board, consulting or <em>leadership mandate?</em></h2>
        <p>Share the challenge, role or geography. The first conversation is confidential and without obligation.</p>
      </div>
      <div class="cta-actions">
        <a href="/contact" class="btn btn-primary">Start a conversation</a>
        <a href="/about" class="btn btn-outline-ghost">View career profile</a>
      </div>
    </div>
  </section>
</main>

<style>
main { overflow: hidden; }
.snapshot { padding-block: clamp(3.5rem, 7vw, 6rem); background: var(--navy); color: #fff; }
.snapshot .section-title { color: #fff; }
.snapshot .section-title em { color: var(--logo-gold-lt); }
.snapshot .tag { color: var(--logo-gold-lt); border-color: var(--logo-gold-lt); }
.snapshot-head { display: flex; align-items: end; justify-content: space-between; gap: 2rem; margin-bottom: 2.5rem; }
.snapshot-head .btn { color: #fff; border-color: rgba(255,255,255,.45); }
.snapshot-head .btn:hover { border-color: var(--accent); }
.snapshot-grid { display: grid; grid-template-columns: 1.35fr .9fr; gap: 1.5rem; }
.role-list { border-top: 1px solid rgba(255,255,255,.16); }
.role-row { display: grid; grid-template-columns: 9rem 1fr; gap: 1.5rem; padding: 1.25rem 0; border-bottom: 1px solid rgba(255,255,255,.16); }
.role-row > span { color: var(--logo-gold-lt); text-transform: uppercase; letter-spacing: .12em; font-size: .68rem; }
.role-row h3 { font-family: var(--font-display); font-size: 1.25rem; font-weight: 400; }
.role-row p { margin-top: .25rem; color: rgba(255,255,255,.62); font-size: .82rem; }
.evidence-card { background: #fff; color: var(--text); border-top: 4px solid var(--accent); padding: 1.8rem; }
.evidence-card h3 { font-family: var(--font-display); font-size: 1.35rem; margin-bottom: 1rem; }
.evidence-card ul { list-style: none; display: grid; gap: .75rem; }
.evidence-card li { position: relative; padding-left: 1rem; color: var(--muted); font-size: .82rem; line-height: 1.55; }
.evidence-card li::before { content: ''; position: absolute; left: 0; top: .65em; width: 5px; height: 5px; background: var(--accent); }
@media (max-width: 780px) {
  .snapshot-head { align-items: flex-start; flex-direction: column; }
  .snapshot-grid { grid-template-columns: 1fr; }
  .role-row { grid-template-columns: 1fr; gap: .45rem; }
}

/* ── Featured ── */
.featured {
  padding-block: var(--section-pad);
  background: var(--off-white);
}
.head-mark {
  margin-bottom: 0.75rem;
}

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(260px,100%), 1fr));
  gap: 1.25rem;
}
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  background: var(--white);
  border: 1px solid rgba(0,0,0,0.07);
  border-top: 3px solid var(--accent);
  border-radius: 6px;
  padding: 2rem;
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  color: var(--text);
  overflow: hidden;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 48px rgba(20,97,164,0.12);
  border-color: var(--accent);
}
/* corner decoration */
.card-corner {
  position: absolute;
  top: 0; right: 0;
  width: 60px; height: 60px;
  background: linear-gradient(225deg, var(--accent-dim) 0%, transparent 70%);
  pointer-events: none;
}
.card-num {
  position: absolute;
  top: 1.1rem; right: 1.25rem;
  font-family: var(--font-display);
  font-size: 2rem;
  font-weight: 300;
  color: rgba(20,97,164,0.1);
  line-height: 1;
}
.card-icon { font-size: 1.75rem; margin-bottom: 1rem; display: block; }
.card h3 {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.55rem;
}
.card p {
  font-size: 0.84rem;
  color: var(--muted);
  line-height: 1.7;
  flex: 1;
  margin-bottom: 1.25rem;
}
.card-link {
  display: flex;
  align-items: center;
  gap: 0.4rem;
  font-size: 0.73rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 500;
  transition: gap 0.2s;
}
.card:hover .card-link { gap: 0.65rem; }

.all-cta {
  margin-top: 2.5rem;
  text-align: center;
}

/* ── Proof ── */
.proof {
  padding-block: var(--section-pad);
  background: var(--cream);
}
.proof-header { margin-bottom: 3rem; }
.proof-rule { margin-bottom: 1.25rem; opacity: 0.8; }
.proof-tag { border-color: var(--border); }

.proof-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(200px,100%), 1fr));
  gap: 2rem;
}
.proof-item { text-align: center; }

.ring-wrap {
  position: relative;
  width: 96px;
  height: 96px;
  margin: 0 auto 1rem;
}
.ring-svg {
  width: 96px;
  height: 96px;
}
.proof-num {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-size: 1.6rem;
  font-weight: 300;
  color: var(--accent);
  line-height: 1;
}
.proof-label {
  font-size: 0.78rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--navy);
}
.proof-sub {
  font-size: 0.72rem;
  color: var(--muted);
  margin-top: 0.3rem;
}

/* ── CTA Band ── */
.cta-band {
  position: relative;
  padding-block: var(--section-pad);
  background: var(--accent);
  overflow: hidden;
}
.cta-bg { position: absolute; inset: 0; pointer-events: none; }
.cta-mesh { position: absolute; inset: 0; width: 100%; height: 100%; }
.cta-orb {
  position: absolute;
  right: -10%;
  top: 50%;
  transform: translateY(-50%);
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(255,255,255,0.08) 0%, transparent 70%);
}
.cta-inner {
  position: relative;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 3rem;
  flex-wrap: wrap;
}
.cta-text p {
  color: rgba(255,255,255,0.75);
  font-size: 0.97rem;
  margin-top: 0.75rem;
}
.cta-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  flex-shrink: 0;
}
.btn-outline-ghost {
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
  color: rgba(255,255,255,0.9);
  border: 1px solid rgba(255,255,255,0.4);
}
.btn-outline-ghost:hover {
  background: rgba(255,255,255,0.12);
  border-color: rgba(255,255,255,0.7);
  color: #fff;
  transform: translateY(-2px);
}
</style>
