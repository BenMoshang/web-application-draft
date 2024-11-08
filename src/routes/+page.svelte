<script>
  import FontTesting from "../lib/components/font-testing/FontTesting.svelte";
  import FaqSection from "../lib/components/section-components/FaqSection.svelte";
  import HeroSection from "../lib/components/section-components/HeroSection.svelte";
  import MotivationSection from "../lib/components/section-components/MotivationSection.svelte";
  import ProjectsSection from "../lib/components/section-components/ProjectsSection.svelte";
  import ServicesSection from "../lib/components/section-components/ServicesSection.svelte";
  import StackSection from "../lib/components/section-components/StackSection.svelte";
  import TestimonialSection from "../lib/components/section-components/TestimonialSection.svelte";
  // Define visibility of sections with $state for reactivity
  let showFontTesting = $state(false);
  let showHero = $state(false);
  let showMotivation = $state(true);
  let showProjects = $state(true);
  let showServices = $state(true);
  let showStack = $state(false);
  let showTestimonials = $state(false);
  let showFaq = $state(false);
</script>

<svelte:head>
  <title>My Modern Site</title>
  <meta
    name="description"
    content="Refresh your web presence with our expert web development services tailored for B2B enterprises. Our agency specializes in creating modern, scalable, and innovative digital solutions to drive your business forward. Partner with us for expert web design, development, and digital marketing strategies that deliver measurable results."
  />
</svelte:head>
<!-- TODO: WE NEED A COMPOENT TO EXPLAIN THE PROBLEM AND WHY THEY WOULD USE US AS A SERVICE-->

{#if showHero}
  <HeroSection />
{/if}

{#if showMotivation}
  <MotivationSection />
{/if}

{#if showProjects}
  <ProjectsSection />
{/if}

{#if showServices}
  <ServicesSection />
{/if}

{#if showStack}
  <StackSection />
{/if}

{#if showTestimonials}
  <TestimonialSection />
{/if}

{#if showFaq}
  <FaqSection />
{/if}

<!-- Render sections conditionally using $state visibility flags -->
{#if showFontTesting}
  <FontTesting />
{/if}

<style global lang="scss">
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
