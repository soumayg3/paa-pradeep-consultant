<script>
  const services = [
    { icon: '⚙️', title: 'Quality Improvement',  desc: 'Implement proven methodologies to enhance product quality, streamline processes, and achieve operational excellence through continuous improvement initiatives.' },
    { icon: '🌱', title: 'ESG Consulting',        desc: 'Environmental, Social, and Governance advisory services to help your organisation meet sustainability goals and stakeholder expectations.' },
    { icon: '🤝', title: 'CSR Strategy',          desc: 'Develop and implement impactful Corporate Social Responsibility programs that create value for both your business and the community.' },
    { icon: '📋', title: 'QMS Implementation',   desc: 'Design and deploy Quality Management Systems aligned with ISO standards to ensure consistent quality and regulatory compliance.' },
    { icon: '🦺', title: 'OHSAS / ISO 45001',    desc: 'Occupational Health and Safety management system implementation to create safer workplaces and reduce workplace incidents.' },
    { icon: '🏭', title: 'Pulp & Paper Industry', desc: 'Specialised consulting for the pulp and paper sector, focusing on process optimisation, sustainability, and operational efficiency.' },
    { icon: '💰', title: 'Cost Reduction',        desc: 'Identify cost-saving opportunities and implement strategies to optimise operational expenses without compromising quality.' },
    { icon: '🌍', title: 'SDG Alignment',         desc: "Align your business strategies with UN Sustainable Development Goals to drive positive impact and long-term sustainability." },
    { icon: '🧭', title: 'Corporate Strategy',    desc: 'Strategic planning and advisory services to help organisations define their vision, set objectives, and achieve sustainable growth.' },
    { icon: '🏛️', title: 'Board Advisory',        desc: 'Expert guidance for board-level decisions, governance frameworks, and strategic direction to ensure organisational success.' },
    { icon: '🔩', title: 'Plastic Moulding',      desc: 'Technical consulting for plastic moulding operations, focusing on process optimisation, quality control, and sustainable practices.' },
  ];

  const whys = [
    { icon: '🏆', title: 'Proven Expertise',       desc: 'Decades of experience across diverse industries with a track record of successful implementations.' },
    { icon: '💡', title: 'Innovative Solutions',   desc: 'Creative problem-solving approaches tailored to your unique business challenges.' },
    { icon: '👥', title: 'Client-Centric Approach',desc: 'Dedicated partnership focused on understanding and achieving your business objectives.' },
    { icon: '📊', title: 'Measurable Results',     desc: 'Data-driven strategies that deliver quantifiable improvements and ROI.' },
  ];
</script>

<section id="services">
  <div class="container">
    <div class="section-head">
      <span class="tag">What I Offer</span>
      <h2 class="section-title">Comprehensive <em>Services</em></h2>
      <p class="section-sub">Tailored solutions designed to solve your most complex business challenges</p>
    </div>

    <div class="cards-grid">
      {#each services as s}
        <div class="card">
          <div class="card-icon">{s.icon}</div>
          <h3>{s.title}</h3>
          <p>{s.desc}</p>
        </div>
      {/each}
    </div>

    <!-- Why Choose Me -->
    <div class="why-wrapper">
      <div class="why-header">
        <span class="tag">Why Choose Me</span>
        <h2 class="section-title">Delivering <em>value</em> through expertise</h2>
        <div class="divider"></div>
      </div>
      <div class="why-grid">
        {#each whys as w}
          <div class="why-card">
            <span class="why-icon">{w.icon}</span>
            <h4>{w.title}</h4>
            <p>{w.desc}</p>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<style>
section {
  padding-block: var(--section-pad);
  background: var(--cream);
}

.section-head {
  margin-bottom: 3.5rem;
}

/* service cards */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(280px, 100%), 1fr));
  gap: 1.25rem;
}

.card {
  background: #fff;
  border: 1px solid rgba(0,0,0,0.07);
  border-radius: 6px;
  padding: 1.75rem;
  transition: transform 0.25s, box-shadow 0.25s, border-color 0.25s;
  cursor: default;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 40px rgba(0,0,0,0.1);
  border-color: var(--border);
}
.card-icon {
  font-size: 1.75rem;
  margin-bottom: 1rem;
  display: block;
}
.card h3 {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.6rem;
}
.card p {
  font-size: 0.84rem;
  color: var(--muted);
  line-height: 1.7;
}

/* why */
.why-wrapper {
  margin-top: 6rem;
}
.why-header { margin-bottom: 2.5rem; }

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
  border-top: 3px solid var(--gold);
}
.why-icon { font-size: 2rem; display: block; margin-bottom: 1rem; }
.why-card h4 {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 400;
  color: var(--gold-light);
  margin-bottom: 0.6rem;
}
.why-card p { font-size: 0.84rem; color: rgba(255,255,255,0.6); line-height: 1.7; }
</style>
