<script>
  import Footer from "../lib/layout/Footer.svelte";
  import Header from "../lib/layout/Header.svelte";

  // Using $props to manage children as a snippet
  let { children: childContent } = $props();
</script>

<!-- <Header /> -->
<main class="layout__main">
  {@render childContent()}
</main>
<Footer />

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  .layout__main {
    display: flex;
    flex-direction: column;
    width: 100%;
    min-height: 100vh;
    max-width: $content-max-width;
    box-sizing: border-box;
    margin: 0 auto;
    gap: 1.875rem;
    overflow: visible;
    // & > *:not(:first-child) {
    //   padding-inline: 0.5rem;
    // }
  }
</style>
