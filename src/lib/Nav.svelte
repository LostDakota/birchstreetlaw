<!-- 
  Nav.svelte
  Responsive top navigation with mobile hamburger toggle.
  Uses Svelte 5 runes syntax ($state, $props).
-->
<script>
  import { page } from '$app/stores';

  let menuOpen = $state(false);

  const links = [
    { href: '/',                label: 'Home' },
    { href: '/about',           label: 'About' },
    { href: '/practice-areas',  label: 'Practice Areas' },
    { href: '/mediation',       label: 'Mediation' },
    { href: '/contact',         label: 'Contact' },
  ];

  function toggleMenu() {
    menuOpen = !menuOpen;
  }

  function closeMenu() {
    menuOpen = false;
  }
</script>

<header class="site-header">
  <div class="container nav-inner">
    <!-- Logo / wordmark -->
    <a href="/" class="logo" onclick={closeMenu}>
      <!-- Small inline birch tree mark -->
      <svg width="28" height="36" viewBox="0 0 28 36" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <rect x="12" y="18" width="4" height="18" rx="1" fill="#8ab89a"/>
        <path d="M14 18 Q6 12 8 4 Q14 8 14 18Z" fill="#4a7c59"/>
        <path d="M14 18 Q22 12 20 4 Q14 8 14 18Z" fill="#2c4a35"/>
        <path d="M14 14 Q8 10 10 3 Q14 7 14 14Z" fill="#4a7c59" opacity="0.6"/>
        <!-- bark marks -->
        <rect x="12.5" y="22" width="3" height="1" rx="0.5" fill="#2c4a35" opacity="0.3"/>
        <rect x="12.5" y="27" width="3" height="1" rx="0.5" fill="#2c4a35" opacity="0.3"/>
        <rect x="12.5" y="32" width="3" height="1" rx="0.5" fill="#2c4a35" opacity="0.3"/>
      </svg>
      <span class="logo-text">
        <span class="logo-name">Birch Street Law</span>
        <span class="logo-sub">PLLC</span>
      </span>
    </a>

    <!-- Desktop nav -->
    <nav class="desktop-nav" aria-label="Main navigation">
      {#each links as link}
        <a
          href={link.href}
          class="nav-link"
          class:active={$page.url.pathname === link.href}
          aria-current={$page.url.pathname === link.href ? 'page' : undefined}
        >
          {link.label}
        </a>
      {/each}
    </nav>

    <!-- CTA button (desktop) -->
    <a href="/contact" class="btn btn-primary nav-cta">Get in Touch</a>

    <!-- Hamburger (mobile) -->
    <button
      class="hamburger"
      onclick={toggleMenu}
      aria-label={menuOpen ? 'Close menu' : 'Open menu'}
      aria-expanded={menuOpen}
    >
      <span class="bar" class:open={menuOpen}></span>
      <span class="bar" class:open={menuOpen}></span>
      <span class="bar" class:open={menuOpen}></span>
    </button>
  </div>

  <!-- Mobile nav drawer -->
  {#if menuOpen}
    <div class="mobile-nav" role="navigation" aria-label="Mobile navigation">
      {#each links as link}
        <a
          href={link.href}
          class="mobile-link"
          class:active={$page.url.pathname === link.href}
          onclick={closeMenu}
        >
          {link.label}
        </a>
      {/each}
      <a href="/contact" class="btn btn-primary mobile-cta" onclick={closeMenu}>Get in Touch</a>
    </div>
  {/if}
</header>

<style>
  .site-header {
    position: sticky;
    top: 0;
    z-index: 100;
    background: var(--white);
    border-bottom: 1px solid var(--cream-dark);
    box-shadow: var(--shadow-sm);
  }

  .nav-inner {
    display: flex;
    align-items: center;
    gap: 2rem;
    height: var(--nav-height);
  }

  /* Logo */
  .logo {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    text-decoration: none !important;
    flex-shrink: 0;
  }

  .logo-text {
    display: flex;
    flex-direction: column;
    line-height: 1.1;
  }

  .logo-name {
    font-family: var(--font-serif);
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--green-deep);
    white-space: nowrap;
  }

  .logo-sub {
    font-family: var(--font-sans);
    font-size: 0.65rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gray-warm);
  }

  /* Desktop nav */
  .desktop-nav {
    display: flex;
    align-items: center;
    gap: 0.25rem;
    flex: 1;
  }

  .nav-link {
    padding: 0.4rem 0.75rem;
    font-size: 0.875rem;
    font-weight: 500;
    color: var(--gray-dark);
    border-radius: var(--radius);
    transition: color var(--transition), background-color var(--transition);
    text-decoration: none !important;
  }

  .nav-link:hover,
  .nav-link.active {
    color: var(--green-deep);
    background-color: var(--cream);
  }

  .nav-link.active {
    font-weight: 600;
  }

  /* CTA */
  .nav-cta {
    flex-shrink: 0;
    font-size: 0.8rem;
    padding: 0.5rem 1.1rem;
  }

  /* Hamburger */
  .hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0.5rem;
    margin-left: auto;
  }

  .bar {
    display: block;
    width: 24px;
    height: 2px;
    background-color: var(--green-deep);
    border-radius: 2px;
    transition: all 0.25s ease;
  }

  /* Animated hamburger → X */
  .hamburger[aria-expanded="true"] .bar:nth-child(1) {
    transform: translateY(7px) rotate(45deg);
  }
  .hamburger[aria-expanded="true"] .bar:nth-child(2) {
    opacity: 0;
  }
  .hamburger[aria-expanded="true"] .bar:nth-child(3) {
    transform: translateY(-7px) rotate(-45deg);
  }

  /* Mobile nav */
  .mobile-nav {
    display: flex;
    flex-direction: column;
    padding: 1rem 1.5rem 1.5rem;
    border-top: 1px solid var(--cream-dark);
    gap: 0.25rem;
    background: var(--white);
  }

  .mobile-link {
    padding: 0.7rem 0.5rem;
    font-size: 1rem;
    font-weight: 500;
    color: var(--gray-dark);
    border-bottom: 1px solid var(--cream-dark);
    text-decoration: none !important;
  }

  .mobile-link.active,
  .mobile-link:hover {
    color: var(--green-deep);
  }

  .mobile-cta {
    margin-top: 1rem;
    text-align: center;
  }

  /* Responsive breakpoint */
  @media (max-width: 768px) {
    .desktop-nav,
    .nav-cta {
      display: none;
    }

    .hamburger {
      display: flex;
    }
  }
</style>
