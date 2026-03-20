<!-- 
  +layout.svelte
  Root layout: imports global CSS, wraps every page with Nav + Footer.
-->
<script>
  import '../lib/styles/global.css';
  import Nav from '../lib/Nav.svelte';
  import Footer from '../lib/Footer.svelte';

  let { children } = $props();
</script>

<Nav />

<main>
  {@render children()}
</main>

<Footer />
