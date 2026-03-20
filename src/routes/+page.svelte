<!--
  +page.svelte — Home Page
  Hero → intro → practice areas summary → about teaser → CTA
-->
<script>
  import BirchDivider from '$lib/BirchDivider.svelte';
</script>

<svelte:head>
  <title>Birch Street Law PLLC — Probate, Estate Planning & Mediation | Shelton, WA</title>
  <meta name="description" content="Birch Street Law PLLC offers compassionate legal services in probate, guardianship, estate planning, TEDRA litigation, and mediation in Shelton, Washington." />
</svelte:head>

<!-- ── Hero ── -->
<section class="hero">
  <!-- Subtle birch tree silhouette (right side decoration) -->
  <div class="hero-tree" aria-hidden="true">
    <svg viewBox="0 0 120 400" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- trunk -->
      <rect x="52" y="200" width="16" height="200" rx="4" fill="white" opacity="0.12"/>
      <!-- bark marks -->
      <rect x="54" y="230" width="12" height="3" rx="1.5" fill="white" opacity="0.08"/>
      <rect x="54" y="260" width="12" height="3" rx="1.5" fill="white" opacity="0.08"/>
      <rect x="54" y="290" width="12" height="3" rx="1.5" fill="white" opacity="0.08"/>
      <rect x="54" y="320" width="12" height="3" rx="1.5" fill="white" opacity="0.08"/>
      <rect x="54" y="350" width="12" height="3" rx="1.5" fill="white" opacity="0.08"/>
      <!-- canopy layers -->
      <ellipse cx="60" cy="160" rx="55" ry="80" fill="white" opacity="0.06"/>
      <ellipse cx="60" cy="120" rx="45" ry="65" fill="white" opacity="0.07"/>
      <ellipse cx="60" cy="85" rx="35" ry="55" fill="white" opacity="0.08"/>
      <ellipse cx="60" cy="55" rx="25" ry="40" fill="white" opacity="0.09"/>
      <!-- side branches -->
      <path d="M52 220 Q30 210 15 200" stroke="white" stroke-width="2" opacity="0.1" fill="none"/>
      <path d="M68 240 Q90 228 105 215" stroke="white" stroke-width="2" opacity="0.1" fill="none"/>
      <path d="M52 270 Q28 260 12 248" stroke="white" stroke-width="1.5" opacity="0.08" fill="none"/>
    </svg>
  </div>

  <div class="container hero-content">
    <p class="hero-eyebrow">Shelton, Washington</p>
    <h1>Compassionate Counsel<br/>for Life's Most<br/>Important Moments</h1>
    <p class="hero-sub">
      Birch Street Law PLLC guides families through probate, guardianship, 
      estate planning, trust disputes, and mediation — with clarity, care, and experience.
    </p>
    <div class="hero-actions">
      <a href="/contact" class="btn btn-light">Schedule a Consultation</a>
      <a href="/practice-areas" class="btn btn-outline-light">Our Practice Areas</a>
    </div>
  </div>
</section>

<!-- ── Brief intro ── -->
<section class="section">
  <div class="container">
    <div class="intro-grid">
      <div class="intro-text">
        <h2>A Firm You Can Rely On</h2>
        <p>
          Founded with a commitment to accessible, thoughtful legal services, Birch Street Law PLLC serves 
          individuals and families navigating some of life's most challenging transitions. Whether you've 
          lost a loved one, need to plan for the future, or find yourself in a difficult dispute, we are 
          here to help you find a path forward.
        </p>
        <p>
          Our attorneys bring a depth of courtroom experience and a collaborative, holistic philosophy — 
          always looking for resolutions that minimize cost, conflict, and stress.
        </p>
        <a href="/about" class="btn btn-primary mt-3">Meet Our Attorneys</a>
      </div>
      <div class="intro-values">
        <div class="value-item">
          <div class="value-icon">
            <!-- Scale icon -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M12 3v18M3 12h18M5.6 7.2l12.8 9.6M18.4 7.2L5.6 16.8"/>
            </svg>
          </div>
          <div>
            <h4>Experienced</h4>
            <p>Decades of combined experience in courts across Washington State.</p>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">
            <!-- Heart icon -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/>
            </svg>
          </div>
          <div>
            <h4>Compassionate</h4>
            <p>We understand the human side of every legal matter and treat clients accordingly.</p>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">
            <!-- Handshake icon -->
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 0 0 1.946-.806 3.42 3.42 0 0 1 4.438 0 3.42 3.42 0 0 0 1.946.806 3.42 3.42 0 0 1 3.138 3.138 3.42 3.42 0 0 0 .806 1.946 3.42 3.42 0 0 1 0 4.438 3.42 3.42 0 0 0-.806 1.946 3.42 3.42 0 0 1-3.138 3.138 3.42 3.42 0 0 0-1.946.806 3.42 3.42 0 0 1-4.438 0 3.42 3.42 0 0 0-1.946-.806 3.42 3.42 0 0 1-3.138-3.138 3.42 3.42 0 0 0-.806-1.946 3.42 3.42 0 0 1 0-4.438 3.42 3.42 0 0 0 .806-1.946 3.42 3.42 0 0 1 3.138-3.138z"/>
            </svg>
          </div>
          <div>
            <h4>Collaborative</h4>
            <p>Holistic problem-solving that seeks resolution over prolonged conflict.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<BirchDivider />

<!-- ── Practice Areas Summary ── -->
<section class="section section--alt">
  <div class="container">
    <div class="text-center mb-4">
      <h2>How We Can Help</h2>
      <p class="text-muted">Areas of law we handle with depth and dedication.</p>
    </div>

    <div class="grid-3">
      {#each [
        { icon: '⚖️', title: 'Probate', desc: 'Guiding families through the probate process efficiently and with care.' },
        { icon: '🛡️', title: 'Guardianship', desc: 'Protecting vulnerable individuals through legal guardianship proceedings.' },
        { icon: '📜', title: 'Estate Planning', desc: 'Wills, trusts, and plans crafted to protect your family and your wishes.' },
        { icon: '⚡', title: 'TEDRA / Trust Disputes', desc: 'Experienced litigation for trust and estate disputes under Washington\'s TEDRA.' },
        { icon: '🏠', title: 'Real Estate', desc: 'Easements, boundary disputes, and real estate transaction support.' },
        { icon: '🤝', title: 'Mediation', desc: 'Neutral, confidential mediation to resolve disputes without the cost of trial.' },
      ] as area}
        <a href="/practice-areas" class="practice-card-link">
          <div class="practice-card">
            <span class="practice-emoji">{area.icon}</span>
            <h3>{area.title}</h3>
            <p class="text-muted">{area.desc}</p>
          </div>
        </a>
      {/each}
    </div>

    <div class="text-center mt-4">
      <a href="/practice-areas" class="btn btn-primary">View All Practice Areas</a>
    </div>
  </div>
</section>

<BirchDivider />

<!-- ── CTA Banner ── -->
<section class="section section--dark">
  <div class="container text-center">
    <h2>Ready to Talk?</h2>
    <p style="color: var(--green-light); max-width: 560px; margin-inline: auto; margin-top: 0.75rem;">
      Legal questions rarely wait. Reach out today to speak with an attorney about your situation.
      We'll listen carefully and let you know how we can help.
    </p>
    <div class="cta-actions mt-4">
      <a href="tel:13603587445" class="btn btn-light">(360) 358-7445</a>
      <a href="/contact" class="btn btn-outline-cream">Contact Us</a>
    </div>
  </div>
</section>

<style>
  /* ── Hero ── */
  .hero {
    position: relative;
    background-color: var(--green-deep);
    color: var(--white);
    padding-block: 6rem 5rem;
    overflow: hidden;
  }

  .hero-tree {
    position: absolute;
    right: -20px;
    top: 0;
    bottom: 0;
    width: 280px;
    pointer-events: none;
  }

  .hero-tree svg {
    width: 100%;
    height: 100%;
  }

  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 680px;
  }

  .hero-eyebrow {
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--green-light);
    margin-bottom: 1rem;
  }

  .hero h1 {
    color: var(--white);
    margin-bottom: 1.5rem;
  }

  .hero-sub {
    font-size: 1.1rem;
    color: rgba(255,255,255,0.8);
    max-width: 540px;
    margin-bottom: 2.5rem;
    line-height: 1.8;
  }

  .hero-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .btn-outline-light {
    display: inline-block;
    padding: 0.75rem 1.75rem;
    border-radius: var(--radius);
    font-family: var(--font-sans);
    font-size: 0.9rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all var(--transition);
    text-decoration: none !important;
    background-color: transparent;
    color: var(--white);
    border: 2px solid rgba(255,255,255,0.5);
  }

  .btn-outline-light:hover {
    background-color: rgba(255,255,255,0.12);
    border-color: var(--white);
    color: var(--white);
  }

  /* ── Intro ── */
  .intro-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }

  @media (max-width: 768px) {
    .intro-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
  }

  .value-item {
    display: grid;
    grid-template-columns: 40px 1fr;
    gap: 1rem;
    align-items: start;
    margin-bottom: 1.5rem;
  }

  .value-item:last-child { margin-bottom: 0; }

  .value-icon {
    width: 40px;
    height: 40px;
    color: var(--green-mid);
    margin-top: 2px;
  }

  .value-icon svg {
    width: 100%;
    height: 100%;
  }

  .value-item h4 {
    margin-bottom: 0.25rem;
  }

  .value-item p {
    font-size: 0.9rem;
    color: var(--gray-warm);
    margin: 0;
  }

  /* ── Practice cards ── */
  .practice-card-link {
    text-decoration: none !important;
    color: inherit;
  }

  .practice-emoji {
    font-size: 1.75rem;
    display: block;
    margin-bottom: 0.75rem;
  }

  .practice-card h3 {
    font-size: 1.05rem;
    margin-bottom: 0.5rem;
  }

  .practice-card p {
    font-size: 0.875rem;
    margin: 0;
  }

  /* ── CTA ── */
  .cta-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: center;
  }

  .btn-outline-cream {
    display: inline-block;
    padding: 0.75rem 1.75rem;
    border-radius: var(--radius);
    font-family: var(--font-sans);
    font-size: 0.9rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all var(--transition);
    text-decoration: none !important;
    background-color: transparent;
    color: var(--cream);
    border: 2px solid rgba(245, 240, 232, 0.5);
  }

  .btn-outline-cream:hover {
    background-color: rgba(245,240,232,0.12);
    border-color: var(--cream);
    color: var(--cream);
  }
</style>
