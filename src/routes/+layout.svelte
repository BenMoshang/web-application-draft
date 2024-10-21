<script>
  import Footer from "../lib/layout/Footer.svelte";
  import Header from "../lib/layout/Header.svelte";
</script>

<Header />

<slot />

<Footer />

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
</style>
