<script>
  import Footer from "../lib/layout/Footer.svelte";
  import Header from "../lib/layout/Header.svelte";

  // Using $props to manage children as a snippet
  let { children: childContent } = $props();
</script>

<Header />

{@render childContent()}

<Footer />

<style global lang="scss">
  
</style>
