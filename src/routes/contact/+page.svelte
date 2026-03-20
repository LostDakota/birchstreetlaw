<!--
  contact/+page.svelte — Contact page (phone + email only, no form)
-->
<svelte:head>
  <title>Contact Birch Street Law PLLC — Shelton, Washington</title>
  <meta name="description" content="Contact Birch Street Law PLLC by phone or email. Located in Shelton, Washington." />
</svelte:head>

<!-- Page Hero -->
<div class="page-hero">
  <div class="container">
    <h1>Contact Us</h1>
    <p>We'd be glad to discuss your situation and how we may be able to help.</p>
  </div>
</div>

<section class="section">
  <div class="container">
    <div class="contact-grid">

      <!-- Phone -->
      <div class="contact-card">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12 19.79 19.79 0 0 1 1.62 3.45 2 2 0 0 1 3.59 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.78a16 16 0 0 0 6.29 6.29l1.58-1.58a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/>
          </svg>
        </div>
        <h3>Phone</h3>
        <p class="contact-detail">
          <a href="tel:13603587445">(360) 358-7445</a>
        </p>
        <p class="contact-note">Call during business hours to speak with our office or to leave a message. We'll return calls as soon as possible.</p>
      </div>

      <!-- Location -->
      <div class="contact-card">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
            <circle cx="12" cy="10" r="3"/>
          </svg>
        </div>
        <h3>Location</h3>
        <p class="contact-detail">Shelton, Washington</p>
        <p class="contact-note">We serve clients throughout Mason County and the surrounding region. In-person and remote appointments available.</p>
      </div>

      <!-- Mediation -->
      <div class="contact-card">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
            <circle cx="9" cy="7" r="4"/>
            <path d="M23 21v-2a4 4 0 0 0-3-3.87"/>
            <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
          </svg>
        </div>
        <h3>Mediation Scheduling</h3>
        <p class="contact-detail">
          <a href="tel:13603587445">(360) 358-7445</a>
        </p>
        <p class="contact-note">To schedule mediation with Rebekah Zinn, please call our office. In-person at Birch Street Law or via Zoom.</p>
      </div>

    </div>

    <!-- Separator + additional info -->
    <div class="info-box mt-4">
      <h3>What to Expect</h3>
      <p>
        When you contact our office, you'll have an opportunity to briefly describe your situation. 
        We'll let you know whether we can help and, if so, discuss next steps. There's no pressure 
        and no commitment required to reach out.
      </p>
      <p>
        <em>Please note: Contacting Birch Street Law PLLC does not create an attorney-client relationship. 
        Do not send confidential information in your initial inquiry.</em>
      </p>
    </div>
  </div>
</section>

<style>
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem;
  }

  .contact-card {
    background: var(--white);
    border-radius: var(--radius);
    padding: 2rem;
    box-shadow: var(--shadow-sm);
    border-top: 3px solid var(--gold);
  }

  .contact-icon {
    width: 44px;
    height: 44px;
    color: var(--gold);
    margin-bottom: 1rem;
  }

  .contact-icon svg {
    width: 100%;
    height: 100%;
  }

  .contact-card h3 {
    margin-bottom: 0.5rem;
  }

  .contact-detail {
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
    color: var(--navy);
  }

  .contact-detail a {
    color: var(--navy);
    text-decoration: none;
  }

  .contact-detail a:hover {
    color: var(--gold);
    text-decoration: underline;
  }

  .contact-note {
    font-size: 0.875rem;
    color: var(--gray-warm);
    margin: 0;
    line-height: 1.6;
  }

  .info-box {
    background: var(--cream-dark);
    border-radius: var(--radius);
    padding: 2rem;
    border-left: 4px solid var(--gold);
    max-width: 700px;
  }

  .info-box h3 {
    margin-bottom: 0.75rem;
  }

  .info-box p {
    font-size: 0.9rem;
    color: var(--gray-dark);
  }

  .info-box em {
    font-size: 0.85rem;
    color: var(--gray-warm);
  }
</style>
