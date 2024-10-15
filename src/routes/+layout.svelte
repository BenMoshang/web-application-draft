<script>
  import "../app.css";
  import "../lib/global-css/global.classes.css";
  import "../lib/global-css/utils.css";
  import Footer from "../lib/layout/Footer.svelte";
  import Header from "../lib/layout/Header.svelte";
</script>

<section class="layout">
  <Header />

  <main class="layout__main">
    <slot />
  </main>

  <Footer />
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  .layout {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    height: 100dvh;
    width: 100%;
    height: 100%;

    & .layout__main {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      max-width: 120rem;
      box-sizing: border-box;
      padding: 0 0.5rem;
      margin: 0 auto;
    }
  }
</style>
