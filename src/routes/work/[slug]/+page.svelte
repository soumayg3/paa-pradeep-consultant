<script>
  import { page } from '$app/stores';
  import { services, getService } from '$lib/data/services.js';

  $: service = getService($page.params.slug);
  $: otherServices = services.filter(s => s.slug !== $page.params.slug).slice(0, 3);
</script>

<svelte:head>
  {#if service}
    <title>{service.title} — Pradeep Kumar Gupta</title>
    <meta name="description" content={service.desc} />
    <link rel="canonical" href="https://www.pradeepkumargupta.in/work/{service.slug}" />
    <meta property="og:title" content="{service.title} — Pradeep Kumar Gupta" />
    <meta property="og:description" content={service.desc} />
    <meta property="og:url" content="https://www.pradeepkumargupta.in/work/{service.slug}" />
    <meta name="twitter:title" content="{service.title} — Pradeep Kumar Gupta" />
    <meta name="twitter:description" content={service.desc} />
  {:else}
    <title>Service Not Found — Pradeep Kumar Gupta</title>
    <meta name="robots" content="noindex" />
  {/if}
</svelte:head>

<main>
  {#if service}
    <!-- ── Hero ── -->
    <section class="page-hero">
      <div class="hero-bg">
        <svg class="grid-pattern" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <defs>
            <pattern id="detail-grid" x="0" y="0" width="48" height="48" patternUnits="userSpaceOnUse">
              <path d="M48 0H0V48" fill="none" stroke="rgba(20,97,164,0.06)" stroke-width="0.8"/>
            </pattern>
          </defs>
          <rect width="100%" height="100%" fill="url(#detail-grid)"/>
        </svg>
        <div class="hero-orb"></div>
      </div>
      <div class="container hero-content">
        <nav class="breadcrumb" aria-label="Breadcrumb">
          <a href="/">Home</a>
          <span class="sep">/</span>
          <a href="/work">Work</a>
          <span class="sep">/</span>
          <span>{service.title}</span>
        </nav>

        <div class="hero-top">
          <div class="hero-icon-wrap" aria-hidden="true">
            <div class="icon-ring"></div>
            <span class="hero-icon">{service.icon}</span>
          </div>
          <div>
            <p class="hero-tagline">{service.tagline}</p>
            <h1 class="section-title">{service.title}</h1>
          </div>
        </div>
      </div>
    </section>

    <!-- ── Overview + Sidebar ── -->
    <section class="overview-section">
      <div class="container overview-grid">
        <div class="overview-text">
          <span class="tag">Overview</span>
          <h2 class="section-title">About this <em>service</em></h2>
          <div class="divider"></div>
          {#each service.overview.split('\n\n') as para}
            <p>{para}</p>
          {/each}
        </div>

        <aside class="sidebar">
          <div class="sidebar-card">
            <h3>Industries Served</h3>
            <ul>
              {#each service.industries as ind}
                <li>
                  <svg width="14" height="14" viewBox="0 0 14 14" fill="none" class="ind-icon" aria-hidden="true">
                    <rect x="1" y="1" width="12" height="12" rx="2" stroke="var(--accent)" stroke-width="1" fill="none"/>
                    <path d="M4 7l2 2 4-4" stroke="var(--accent)" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                  {ind}
                </li>
              {/each}
            </ul>
          </div>

          <div class="sidebar-cta">
            <p>Ready to explore how this applies to your business?</p>
            <a href="/contact" class="btn btn-primary" style="width:100%;justify-content:center">Get In Touch</a>
            <a
              href="https://wa.me/917669697397?text=Hi%2C%20I%27m%20interested%20in%20{encodeURIComponent(service.title)}"
              target="_blank"
              rel="noopener"
              class="wa-btn"
            >
              <svg viewBox="0 0 24 24" fill="currentColor" width="16" height="16" aria-hidden="true">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413z"/>
              </svg>
              Message on WhatsApp
            </a>
          </div>
        </aside>
      </div>
    </section>

    <!-- ── Benefits ── -->
    <section class="benefits-section">
      <div class="container">
        <div class="section-head">
          <span class="tag">Key Benefits</span>
          <h2 class="section-title">What you <em>gain</em></h2>
          <div class="divider"></div>
        </div>
        <div class="benefits-grid">
          {#each service.benefits as b, i}
            <div class="benefit-card">
              <div class="benefit-bar"></div>
              <div class="benefit-num">0{i + 1}</div>
              <h3>{b.title}</h3>
              <p>{b.desc}</p>
            </div>
          {/each}
        </div>
      </div>
    </section>

    <!-- ── Approach ── -->
    <section class="approach-section">
      <div class="container">
        <div class="section-head">
          <span class="tag">Methodology</span>
          <h2 class="section-title">How we <em>work together</em></h2>
          <div class="divider"></div>
        </div>

        <!-- Visual flow for desktop -->
        <div class="flow">
          {#each service.approach as step, i}
            <div class="flow-step">
              <div class="flow-node">
                <div class="flow-num">{step.step}</div>
              </div>
              <div class="flow-body">
                <h3>{step.title}</h3>
                <p>{step.desc}</p>
              </div>
              {#if i < service.approach.length - 1}
                <div class="flow-connector" aria-hidden="true">
                  <svg viewBox="0 0 32 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1 8 H28 M22 3 L28 8 L22 13" stroke="rgba(20,97,164,0.4)" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
                  </svg>
                </div>
              {/if}
            </div>
          {/each}
        </div>
      </div>
    </section>

    <!-- ── Related ── -->
    <section class="related-section">
      <div class="container">
        <div class="section-head">
          <span class="tag">Other Services</span>
          <h2 class="section-title">Related <em>expertise</em></h2>
        </div>
        <div class="related-grid">
          {#each otherServices as s}
            <a href="/work/{s.slug}" class="related-card">
              <span class="r-icon">{s.icon}</span>
              <div>
                <h3>{s.title}</h3>
                <p>{s.tagline}</p>
              </div>
              <svg class="r-arrow" viewBox="0 0 20 12" fill="none" xmlns="http://www.w3.org/2000/svg" width="20" height="12" aria-hidden="true">
                <path d="M1 6h18M13 1l6 5-6 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </a>
          {/each}
        </div>
        <div style="text-align:center;margin-top:2.5rem">
          <a href="/work" class="btn btn-outline">View All Services</a>
        </div>
      </div>
    </section>

  {:else}
    <section class="not-found">
      <div class="container">
        <h1>Service not found</h1>
        <p>The service you're looking for does not exist.</p>
        <a href="/work" class="btn btn-primary" style="margin-top:1.5rem;display:inline-flex">View All Services</a>
      </div>
    </section>
  {/if}
</main>

<style>
main { padding-top: 0; }

/* ── Hero — inherits light styles from app.css .page-hero ── */
.grid-pattern { position: absolute; inset: 0; width: 100%; height: 100%; }
.hero-orb {
  position: absolute;
  right: -5%;
  top: 50%;
  transform: translateY(-50%);
  width: 450px;
  height: 450px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(20,97,164,0.06) 0%, transparent 65%);
}

.breadcrumb {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  color: var(--muted);
  margin-bottom: 2.5rem;
}
.breadcrumb a { color: var(--muted); transition: color 0.2s; }
.breadcrumb a:hover { color: var(--navy); }
.sep { opacity: 0.35; }

.hero-top {
  display: flex;
  align-items: flex-start;
  gap: 1.75rem;
}
.hero-icon-wrap {
  position: relative;
  flex-shrink: 0;
  width: 64px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.icon-ring {
  position: absolute;
  inset: 0;
  border: 1px solid rgba(20,97,164,0.35);
  border-radius: 50%;
}
.icon-ring::after {
  content: '';
  position: absolute;
  inset: 8px;
  border: 1px solid rgba(20,97,164,0.15);
  border-radius: 50%;
}
.hero-icon { font-size: 2rem; position: relative; z-index: 1; }
.hero-tagline {
  font-size: 0.7rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--accent-light);
  margin-bottom: 0.5rem;
  font-weight: 400;
}

/* ── Overview ── */
.overview-section {
  padding-block: var(--section-pad);
  background: var(--off-white);
}
.overview-grid {
  display: grid;
  grid-template-columns: 1fr 320px;
  gap: clamp(2.5rem, 5vw, 5rem);
  align-items: start;
}
.overview-text p { color: var(--muted); font-size: 0.97rem; line-height: 1.8; margin-top: 1rem; }

.sidebar { display: flex; flex-direction: column; gap: 1.25rem; }
.sidebar-card {
  background: var(--white);
  border: 1px solid var(--border);
  border-top: 3px solid var(--accent);
  border-radius: 6px;
  padding: 1.5rem;
}
.sidebar-card h3 {
  font-size: 0.62rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 1rem;
}
.sidebar-card ul { list-style: none; display: flex; flex-direction: column; gap: 0.65rem; }
.sidebar-card li {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  font-size: 0.85rem;
  color: var(--navy);
}
.ind-icon { flex-shrink: 0; }

.sidebar-cta {
  background: var(--navy);
  border-radius: 6px;
  padding: 1.75rem;
  display: flex;
  flex-direction: column;
  gap: 0.85rem;
}
.sidebar-cta p { color: rgba(255,255,255,0.6); font-size: 0.85rem; line-height: 1.7; }
.wa-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  background: #25D366;
  color: #fff;
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 0.75em 1.5em;
  border-radius: var(--radius);
  transition: background 0.2s;
}
.wa-btn:hover { background: #20ba59; }

/* ── Benefits ── */
.benefits-section {
  padding-block: var(--section-pad);
  background: var(--cream);
}
.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(240px,100%), 1fr));
  gap: 1.25rem;
}
.benefit-card {
  background: var(--white);
  border: 1px solid rgba(0,0,0,0.06);
  border-radius: 6px;
  padding: 1.75rem;
  position: relative;
  overflow: hidden;
}
.benefit-bar {
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: linear-gradient(to right, var(--accent), var(--accent-light));
}
.benefit-num {
  font-family: var(--font-display);
  font-size: 2.5rem;
  font-weight: 300;
  color: rgba(20,97,164,0.1);
  line-height: 1;
  margin-bottom: 0.75rem;
}
.benefit-card h3 {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.5rem;
}
.benefit-card p { font-size: 0.84rem; color: var(--muted); line-height: 1.7; }

/* ── Approach ── */
.approach-section {
  padding-block: var(--section-pad);
  background: var(--cream);
}

/* Horizontal flow */
.flow {
  display: flex;
  align-items: flex-start;
  gap: 0;
  flex-wrap: wrap;
}
.flow-step {
  display: flex;
  align-items: flex-start;
  gap: 0;
  flex: 1;
  min-width: min(220px, 100%);
}
.flow-node {
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: 180px;
}
.flow-num {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: rgba(20,97,164,0.18);
  border: 1.5px solid var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 400;
  color: var(--accent-light);
  margin-bottom: 1rem;
  flex-shrink: 0;
}
.flow-body {
  flex: 1;
  padding: 0 0 2rem 0;
}
.flow-body h3 {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.5rem;
}
.flow-body p { font-size: 0.84rem; color: var(--muted); line-height: 1.7; }
.flow-connector {
  flex-shrink: 0;
  width: 32px;
  height: 48px;
  display: flex;
  align-items: center;
  align-self: flex-start;
  margin-top: 0;
}
.flow-connector svg { width: 32px; height: 16px; }

/* On narrow screens, flow becomes vertical list */
@media (max-width: 860px) {
  .flow { flex-direction: column; }
  .flow-step { flex-direction: row; align-items: flex-start; gap: 1.5rem; min-width: 0; width: 100%; }
  .flow-node { flex-direction: column; align-items: center; min-width: auto; }
  .flow-num { margin-bottom: 0; }
  .flow-connector {
    display: none;
  }
  /* vertical line between steps */
  .flow-step:not(:last-child) .flow-node::after {
    content: '';
    flex: 1;
    width: 1px;
    min-height: 2rem;
    background: rgba(20,97,164,0.25);
    margin-top: 4px;
  }
}

/* ── Related ── */
.related-section {
  padding-block: var(--section-pad);
  background: var(--off-white);
}
.related-grid {
  display: flex;
  flex-direction: column;
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
}
.related-card {
  display: flex;
  align-items: center;
  gap: 1.25rem;
  background: var(--white);
  padding: 1.25rem 1.5rem;
  color: var(--text);
  transition: background 0.2s;
}
.related-card:hover { background: var(--off-white); }
.related-card:hover .r-arrow { transform: translateX(4px); color: var(--accent); }
.r-icon { font-size: 1.75rem; flex-shrink: 0; }
.related-card div { flex: 1; }
.related-card h3 {
  font-family: var(--font-display);
  font-size: 1.05rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.15rem;
}
.related-card p { font-size: 0.78rem; color: var(--muted); }
.r-arrow {
  color: var(--muted);
  flex-shrink: 0;
  transition: transform 0.2s, color 0.2s;
}

/* ── Not Found ── */
.not-found { padding-block: 10rem; text-align: center; }
.not-found h1 {
  font-family: var(--font-display);
  font-size: 2.5rem;
  color: var(--navy);
  margin-bottom: 1rem;
}
.not-found p { color: var(--muted); }

@media (max-width: 860px) {
  .overview-grid { grid-template-columns: 1fr; }
  .sidebar { flex-direction: row; flex-wrap: wrap; }
  .sidebar-card, .sidebar-cta { flex: 1; min-width: 240px; }
}
</style>
