<script>
  import "../app.css";
  import "../lib/global-css/global.classes.css";
  import "../lib/global-css/utils.css";
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
