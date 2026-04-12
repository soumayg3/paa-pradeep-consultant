<section id="about">
  <div class="container grid">
    <div class="photo-col">
      <div class="photo-frame">
        <img
          src="https://www.pradeepkumargupta.in/image.jpeg"
          alt="Pradeep Kumar Gupta – Business Consultant"
          loading="lazy"
        />
        <div class="photo-accent"></div>
      </div>

      <div class="credential-cards">
        <div class="cred-card">
          <div class="cred-icon">🎓</div>
          <div>
            <div class="cred-title">IIT Roorkee</div>
            <div class="cred-sub">Indian Institute of Technology Roorkee</div>
          </div>
        </div>
        <div class="cred-card">
          <div class="cred-icon">🏅</div>
          <div>
            <div class="cred-title">Lean Six Sigma</div>
            <div class="cred-sub">Green Belt Certified</div>
          </div>
        </div>
      </div>
    </div>

    <div class="text-col">
      <span class="tag">About Me</span>
      <h2 class="section-title">Delivering excellence through <em>expertise</em></h2>
      <div class="divider"></div>
      <p>
        With extensive experience in business consulting and strategic advisory, I help organisations
        achieve operational excellence, implement sustainable practices, and drive continuous
        improvement across all facets of their operations.
      </p>
      <p style="margin-top:1rem">
        My expertise spans Quality Management Systems, Environmental & Social Governance, Corporate
        Social Responsibility, and industry-specific solutions that deliver measurable results.
      </p>

      <div class="pillars">
        {#each ['Quality Management','ESG & Sustainability','Corporate Strategy','Operational Excellence'] as p}
          <div class="pillar">
            <div class="pillar-dot"></div>
            {p}
          </div>
        {/each}
      </div>

      <a href="#contact" class="btn btn-primary" style="margin-top:2rem">Work With Me</a>
    </div>
  </div>
</section>

<style>
section {
  padding-block: var(--section-pad);
  background: var(--off-white);
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(3rem, 6vw, 6rem);
  align-items: start;
}

/* photo */
.photo-col { display: flex; flex-direction: column; gap: 1.5rem; }

.photo-frame {
  position: relative;
  border-radius: 6px;
  overflow: hidden;
}
.photo-frame img {
  width: 100%;
  aspect-ratio: 4/5;
  object-fit: cover;
  object-position: top;
  border-radius: 6px;
  filter: grayscale(10%) contrast(1.05);
  transition: filter 0.4s;
}
.photo-frame:hover img { filter: none; }
.photo-accent {
  position: absolute;
  inset: 0;
  border: 2px solid var(--gold);
  border-radius: 6px;
  opacity: 0;
  transition: opacity 0.3s;
  pointer-events: none;
}
.photo-frame:hover .photo-accent { opacity: 0.6; }

/* credentials */
.credential-cards { display: flex; flex-direction: column; gap: 0.85rem; }
.cred-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  background: var(--navy);
  color: #fff;
  border-radius: var(--radius);
  padding: 0.85rem 1.2rem;
  border-left: 3px solid var(--gold);
}
.cred-icon { font-size: 1.25rem; flex-shrink: 0; }
.cred-title { font-family: var(--font-display); font-size: 1rem; font-weight: 400; color: var(--gold-light); }
.cred-sub   { font-size: 0.72rem; color: rgba(255,255,255,0.55); margin-top: 0.1rem; letter-spacing: 0.04em; }

/* text */
.text-col p { color: var(--muted); font-size: 0.97rem; line-height: 1.8; }

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
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--gold);
  flex-shrink: 0;
}

@media (max-width: 840px) {
  .grid { grid-template-columns: 1fr; }
  .photo-col { max-width: 420px; }
}
</style>
