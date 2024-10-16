<script>
  import ImageCard from "../lib/components/reusable-components/ImageCard.svelte";
  import HeroSection from "../lib/components/section-components/HeroSection.svelte";
  import ProjectsSection from "../lib/components/section-components/ProjectsSection.svelte";
  import ServicesSection from "../lib/components/section-components/ServicesSection.svelte";
  import StackSection from "../lib/components/section-components/StackSection.svelte";
  import TestimonialSection from "../lib/components/section-components/TestimonialSection.svelte";
</script>

<svelte:head>
  <title>My Modern Site</title>
  <meta
    name="description"
    content="Refresh your web presence with our expert web development services tailored for B2B enterprises. Our agency specializes in creating modern, scalable, and innovative digital solutions to drive your business forward. Partner with us for expert web design, development, and digital marketing strategies that deliver measurable results."
  />
</svelte:head>
<main class="layout__main">
  <HeroSection />
  <ProjectsSection />
  <ServicesSection />
</main>

<!-- <StackSection /> -->
<!-- <TestimonialSection /> -->
<style>
  .layout__main {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    max-width: 120rem;
    box-sizing: border-box;
    padding: 0 0.5rem;
    margin: 0 auto;

    & > * {
      flex: 1;
    }
  }
</style>
