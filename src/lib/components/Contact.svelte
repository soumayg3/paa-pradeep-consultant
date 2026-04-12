<section id="contact">
  <div class="bg-layer"></div>
  <div class="container grid">
    <div class="info-col">
      <span class="tag">Get In Touch</span>
      <h2 class="section-title" style="color:#fff">Let's <em>transform</em><br/>your business</h2>
      <div class="divider"></div>
      <p>Reach out for a consultation and discover how expert guidance can drive measurable results for your organisation.</p>

      <div class="contact-items">
        <a href="mailto:shyamaprojects@yahoo.co.in" class="c-item">
          <div class="c-icon">✉️</div>
          <div>
            <div class="c-label">Email</div>
            <div class="c-value">shyamaprojects@yahoo.co.in</div>
          </div>
        </a>
        <a href="https://wa.me/917669697397" class="c-item" target="_blank" rel="noopener">
          <div class="c-icon">📱</div>
          <div>
            <div class="c-label">WhatsApp</div>
            <div class="c-value">+91 76696 97397</div>
          </div>
        </a>
        <div class="c-item">
          <div class="c-icon">📍</div>
          <div>
            <div class="c-label">Location</div>
            <div class="c-value">India</div>
          </div>
        </div>
        <a href="https://www.linkedin.com/in/pkg9673/" class="c-item" target="_blank" rel="noopener">
          <div class="c-icon">🔗</div>
          <div>
            <div class="c-label">LinkedIn</div>
            <div class="c-value">linkedin.com/in/pkg9673</div>
          </div>
        </a>
      </div>
    </div>

    <div class="cta-col">
      <div class="whatsapp-card">
        <div class="wa-icon">
          <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 0 0-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413z"/>
          </svg>
        </div>
        <h3>Connect on WhatsApp</h3>
        <p>Get in touch directly for quick consultations and inquiries</p>
        <a
          href="https://wa.me/917669697397?text=Hi%2C%20I%27m%20interested%20in%20learning%20more%20about%20your%20services"
          class="btn btn-primary wa-btn"
          target="_blank"
          rel="noopener"
        >
          Message on WhatsApp
        </a>
      </div>
    </div>
  </div>
</section>

<style>
section {
  position: relative;
  padding-block: var(--section-pad);
  overflow: hidden;
}
.bg-layer {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
  z-index: 0;
}

.container { position: relative; z-index: 1; }

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(3rem, 6vw, 5rem);
  align-items: start;
}

/* info */
.info-col p {
  color: rgba(255,255,255,0.6);
  font-size: 0.95rem;
  line-height: 1.8;
  margin-bottom: 2rem;
}

.contact-items { display: flex; flex-direction: column; gap: 1rem; }

.c-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem 1.25rem;
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: var(--radius);
  transition: background 0.2s, border-color 0.2s;
  color: #fff;
}
a.c-item:hover {
  background: rgba(201,168,76,0.1);
  border-color: var(--border);
}
.c-icon { font-size: 1.25rem; flex-shrink: 0; }
.c-label { font-size: 0.65rem; letter-spacing: 0.14em; text-transform: uppercase; color: var(--gold); margin-bottom: 0.1rem; }
.c-value { font-size: 0.88rem; color: rgba(255,255,255,0.8); }

/* CTA card */
.whatsapp-card {
  background: #fff;
  border-radius: 8px;
  padding: 2.5rem;
  text-align: center;
  box-shadow: 0 20px 60px rgba(0,0,0,0.25);
}
.wa-icon {
  width: 3.5rem; height: 3.5rem;
  background: #25D366;
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  margin: 0 auto 1.5rem;
  color: #fff;
}
.wa-icon svg { width: 1.75rem; height: 1.75rem; }

.whatsapp-card h3 {
  font-family: var(--font-display);
  font-size: 1.5rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 0.65rem;
}
.whatsapp-card p {
  font-size: 0.88rem;
  color: var(--muted);
  margin-bottom: 2rem;
  line-height: 1.7;
}
.wa-btn {
  background: #25D366 !important;
  width: 100%;
  justify-content: center;
}
.wa-btn:hover {
  background: #20ba59 !important;
  box-shadow: 0 8px 24px rgba(37,211,102,0.35) !important;
}

@media (max-width: 840px) {
  .grid { grid-template-columns: 1fr; }
}
</style>
