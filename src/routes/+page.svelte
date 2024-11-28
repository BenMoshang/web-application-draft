<script>
  import FontTesting from "../lib/components/font-testing/FontTesting.svelte";
  import AboutSection from "../lib/components/section-components/AboutSection.svelte";
  import ContactSection from "../lib/components/section-components/ContactSection.svelte";
  import FaqSection from "../lib/components/section-components/FaqSection.svelte";
  import HeroSection from "../lib/components/section-components/HeroSection.svelte";
  import MotivationSection from "../lib/components/section-components/MotivationSection.svelte";
  import ProjectsSection from "../lib/components/section-components/ProjectsSection.svelte";
  import ServicesSection from "../lib/components/section-components/ServicesSection.svelte";
  import StackSection from "../lib/components/section-components/StackSection.svelte";
  import TestimonialSection from "../lib/components/section-components/TestimonialSection.svelte";
  import UITransformSection from "../lib/components/ui-transform/UITransformSection.svelte";
  import UiTransformCard from "./../lib/components/reusable-components/UiTransformCard.svelte";
  // Font testing
  let showFontTesting = $state(true);
  // Sections
  let showHero = $state(true);
  let showUITransform = $state(true);
  let showServices = $state(true);
  let showProjects = $state(true);

  let showAbout = $state(true);
  let showMotivation = $state(true);
  let showStack = $state(true);
  let showTestimonials = $state(true);
  let showFaq = $state(false);
  let showContact = $state(true);
</script>

<svelte:head>
  <title>My Modern Site</title>
  <meta
    name="description"
    content="Refresh your web presence with our expert web development services tailored for B2B enterprises. Our agency specializes in creating modern, scalable, and innovative digital solutions to drive your business forward. Partner with us for expert web design, development, and digital marketing strategies that deliver measurable results."
  />
</svelte:head>
<!-- TODO: WE NEED A COMPOENT TO EXPLAIN THE PROBLEM AND WHY THEY WOULD USE US AS A SERVICE w a stepper-->

{#if showHero}
  <HeroSection />
{/if}

<!-- {#if showUITransform}
  <UITransformSection />
{/if} -->

<UiTransformCard />

{#if showServices}
  <ServicesSection />
{/if}
{#if showProjects}
  <ProjectsSection />
{/if}
{#if showStack}
  <StackSection />
{/if}
{#if showTestimonials}
  <TestimonialSection />
{/if}

{#if showAbout}
  <AboutSection />
{/if}

{#if showMotivation}
  <MotivationSection />
{/if}

{#if showFaq}
  <FaqSection />
{/if}

{#if showContact}
  <ContactSection />
{/if}

<!-- Render sections conditionally using $state visibility flags -->
{#if showFontTesting}
  <FontTesting />
{/if}

<style global lang="scss">
  @import "./src/lib/SCSS/index.scss";

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
    /* & > *:not(:first-child) {
      padding-inline: 0.5rem;
    } */
  }
</style>
