<script>
  import Footer from "../lib/layout/Footer.svelte";
  import Header from "../lib/layout/Header.svelte";
  /**
   * @typedef {Object} Props
   * @property {import('svelte').Snippet} [children]
   */

  /** @type {Props} */
  let { children } = $props();
</script>

<Header />

{@render children?.()}

<Footer />

<style>

 
</style>
