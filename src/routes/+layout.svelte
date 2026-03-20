<!-- 
  +layout.svelte
  Root layout: imports global CSS, wraps every page with Nav + Footer.
-->
<script>
  import '../lib/styles/global.css';
  import Nav from '../lib/Nav.svelte';
  import Footer from '../lib/Footer.svelte';
  import { afterNavigate } from '$app/navigation';

  let { children } = $props();

  afterNavigate(() => {
    // Scroll to top on page navigation
    window.scrollTo({ top: 0, behavior: 'instant' });
  });
</script>

<Nav />

<main>
  {@render children()}
</main>

<Footer />
