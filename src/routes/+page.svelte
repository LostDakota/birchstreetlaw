<!--
  +page.svelte — Home Page
  Hero → intro → practice areas summary → CTA
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
      <rect x="52" y="200" width="16" height="200" rx="4" fill="white" opacity="0.10"/>
      <!-- bark marks -->
      <rect x="54" y="230" width="12" height="3" rx="1.5" fill="white" opacity="0.07"/>
      <rect x="54" y="260" width="12" height="3" rx="1.5" fill="white" opacity="0.07"/>
      <rect x="54" y="290" width="12" height="3" rx="1.5" fill="white" opacity="0.07"/>
      <rect x="54" y="320" width="12" height="3" rx="1.5" fill="white" opacity="0.07"/>
      <rect x="54" y="350" width="12" height="3" rx="1.5" fill="white" opacity="0.07"/>
      <!-- canopy layers -->
      <ellipse cx="60" cy="160" rx="55" ry="80" fill="white" opacity="0.05"/>
      <ellipse cx="60" cy="120" rx="45" ry="65" fill="white" opacity="0.06"/>
      <ellipse cx="60" cy="85" rx="35" ry="55" fill="white" opacity="0.07"/>
      <ellipse cx="60" cy="55" rx="25" ry="40" fill="white" opacity="0.08"/>
      <!-- side branches -->
      <path d="M52 220 Q30 210 15 200" stroke="white" stroke-width="2" opacity="0.08" fill="none"/>
      <path d="M68 240 Q90 228 105 215" stroke="white" stroke-width="2" opacity="0.08" fill="none"/>
      <path d="M52 270 Q28 260 12 248" stroke="white" stroke-width="1.5" opacity="0.06" fill="none"/>
    </svg>
  </div>

  <div class="container hero-content">
    <p class="hero-eyebrow">Serving Mason and Thurston Counties</p>
    <h1>Birch Street Law PLLC</h1>
    <p class="hero-tagline">Compassionate Counsel for Life's Most Important Moments</p>
    <p class="hero-sub">
      The attorneys at Birch Street Law provide legal services to help guide individuals through 
      some of life's most sensitive legal matters — with clarity and compassion.
    </p>
    <div class="hero-actions">
      <a href="/contact" class="btn btn-gold">Schedule a Consultation</a>
      <a href="/practice-areas" class="btn btn-outline-light">Our Practice Areas</a>
    </div>
  </div>
</section>

<!-- ── Intro text (exact client copy) ── -->
<section class="section">
  <div class="container">
    <div class="intro-grid">
      <div class="intro-text">
        <h2>How We Can Help</h2>
        <p>
          The attorneys at Birch Street Law provide legal services to help guide individuals through 
          some of life's most sensitive legal matters—probate, guardianship, trust and estate dispute 
          resolution (including TEDRA petitions), estate planning, elder and vulnerable adult protection 
          (including VAPOs), and real estate issues—with clarity and compassion.
        </p>
        <p>
          Our attorneys strive to resolve conflicts efficiently and respectfully, helping parties find 
          common ground to avoid the expense, uncertainty, and stress of litigation.
        </p>
        <p>
          Attorney Rebekah Zinn's experience as a Court Commissioner (retired) enables her to help 
          parties resolve disputes outside of court as a mediator by facilitating open dialogue and 
          finding fair, mutually agreeable solutions.
        </p>
        <div class="intro-actions">
          <a href="/about" class="btn btn-primary">Meet Our Attorneys</a>
          <a href="/mediation" class="btn btn-outline">Mediation Services</a>
        </div>
      </div>
      <div class="intro-values">
        <div class="value-item">
          <div class="value-icon">
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
      <h2>Practice Areas</h2>
      <p class="text-muted">Areas of law we handle with depth and dedication.</p>
    </div>

    <div class="grid-3">
      {#each [
        { title: 'Probate', desc: 'Guiding families through the probate process efficiently and with care.' },
        { title: 'Guardianship', desc: 'Protecting vulnerable individuals through legal guardianship proceedings.' },
        { title: 'Estate Planning', desc: 'Wills, trusts, and plans crafted to protect your family and your wishes.' },
        { title: 'Trust & Estate Disputes (TEDRA)', desc: 'Experienced litigation for trust and estate disputes under Washington\'s TEDRA.' },
        { title: 'Elder & Vulnerable Adult Protection', desc: 'Vulnerable Adult Protection Orders (VAPOs) and advocacy for those at risk.' },
        { title: 'Real Estate', desc: 'Easements, boundary disputes, and real estate transaction support.' },
      ] as area}
        <a href="/practice-areas" class="practice-card-link">
          <div class="practice-card">
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
    <p class="cta-sub">
      Legal questions rarely wait. Reach out today to speak with an attorney about your situation.
      We'll listen carefully and let you know how we can help.
    </p>
    <div class="cta-actions mt-4">
      <a href="tel:13603587445" class="btn btn-gold">(360) 358-7445</a>
      <a href="/contact" class="btn btn-outline-cream">Contact Us</a>
    </div>
  </div>
</section>

<style>
  /* ── Hero ── */
  .hero {
    position: relative;
    background-color: var(--navy);
    color: var(--white);
    padding-block: 6rem 5rem;
    overflow: hidden;
    border-bottom: 4px solid var(--gold);
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
    color: var(--gold-light);
    margin-bottom: 1rem;
  }

  .hero h1 {
    color: var(--white);
    margin-bottom: 0.5rem;
    font-size: clamp(2.2rem, 5vw, 3.5rem);
  }

  .hero-tagline {
    font-family: var(--font-serif);
    font-size: clamp(1.1rem, 2.5vw, 1.5rem);
    color: var(--gold-light);
    margin-bottom: 1.5rem;
    font-style: italic;
    font-weight: 400;
  }

  .hero-sub {
    font-size: 1rem;
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

  .btn-gold {
    display: inline-block;
    padding: 0.75rem 1.75rem;
    border-radius: var(--radius);
    font-family: var(--font-sans);
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all var(--transition);
    text-decoration: none !important;
    background-color: var(--gold);
    color: var(--navy);
    border: 2px solid var(--gold);
  }

  .btn-gold:hover {
    background-color: var(--gold-light);
    border-color: var(--gold-light);
    color: var(--navy);
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

  .intro-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 1.5rem;
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
    color: var(--gold);
    margin-top: 2px;
  }

  .value-icon svg {
    width: 100%;
    height: 100%;
  }

  .value-item h4 {
    margin-bottom: 0.25rem;
    color: var(--navy);
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

  .practice-card h3 {
    font-size: 1.05rem;
    margin-bottom: 0.5rem;
    color: var(--navy);
  }

  .practice-card p {
    font-size: 0.875rem;
    margin: 0;
  }

  /* ── CTA ── */
  .cta-sub {
    color: var(--gold-light);
    max-width: 560px;
    margin-inline: auto;
    margin-top: 0.75rem;
  }

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
