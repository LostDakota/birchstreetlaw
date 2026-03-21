<!-- Footer.svelte — Site-wide footer -->
<script>
  const year = new Date().getFullYear();
</script>

<footer>
  <div class="container">
    <div class="footer-grid">
      <!-- Brand -->
      <div>
        <p class="footer-brand">Birch Street Law PLLC</p>
        <p class="footer-tagline">Compassionate counsel for life's most important moments.</p>
      </div>

      <!-- Navigation -->
      <div>
        <h4 class="footer-heading">Navigation</h4>
        <ul class="footer-links">
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
          <li><a href="/practice-areas">Practice Areas</a></li>
          <li><a href="/mediation">Mediation</a></li>
          <li><a href="/contact">Contact</a></li>
        </ul>
      </div>

      <!-- Contact -->
      <div>
        <h4 class="footer-heading">Contact</h4>
        <ul class="footer-links">
          <li>
            <a href="tel:13603587445">(360) 358-7445</a>
          </li>
          <li>236 W. Birch Street, Shelton, WA 98584</li>
        </ul>
      </div>
    </div>

    <div class="footer-bottom">
      <p>© {year} Birch Street Law PLLC. All rights reserved. &nbsp;·&nbsp; Attorney Advertising. This website is for informational purposes only and does not constitute legal advice.</p>
    </div>
  </div>
</footer>

<style>
  .footer-brand {
    font-family: var(--font-serif);
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 0.4rem;
  }

  .footer-tagline {
    font-size: 0.85rem;
    color: var(--gold-light);
    font-style: italic;
    max-width: 220px;
  }

  .footer-heading {
    font-family: var(--font-sans);
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--gold);
    margin-bottom: 0.75rem;
  }

  .footer-links {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
  }

  .footer-links li {
    font-size: 0.9rem;
    color: var(--cream-dark);
  }

  .footer-links a {
    color: var(--cream-dark);
    transition: color var(--transition);
    text-decoration: none;
  }

  .footer-links a:hover {
    color: var(--gold-light);
  }
</style>
