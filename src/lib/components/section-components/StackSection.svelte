<script>
  import StackCard from "../reusable-components/StackCard.svelte";

  const stackData = [
    {
      imageSrc: "https://placehold.co/56x56",
      title: "Framer",
      useCase: "Web Design Platform",
      description:
        "The internet is your canvas. Framer is where design and code meet.",
    },
    {
      imageSrc: "https://placehold.co/56x56",
      title: "Framer",
      useCase: "Web Design Platform",
      description:
        "The internet is your canvas. Framer is where design and code meet.",
    },
    {
      imageSrc: "https://placehold.co/56x56",
      title: "Framer",
      useCase: "Web Design Platform",
      description:
        "The internet is your canvas. Framer is where design and code meet.",
    },
    {
      imageSrc: "https://placehold.co/56x56",
      title: "Framer",
      useCase: "Web Design Platform",
      description:
        "The internet is your canvas. Framer is where design and code meet.",
    },
  ];
</script>

<section class="stack">
  <h3 class="stack__heading global__heading--md">FAVORITE STACK</h3>
  <section class="stack__content">
    {#each stackData as { imageSrc, title, useCase, description }}
      <StackCard {imageSrc} {title} {useCase} {description} />
    {/each}
  </section>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .stack {
    @include section-padding-inline;
    @include flex-column-jus-center;
    @include section-heading-content-gap;
    padding-top: clamp(80px, 3.769rem + 4.15vw, 120px);
    position: relative;
    overflow-y: visible;
    inline-size: 100%;
    block-size: 100%;
    &__heading {
      position: sticky;
      top: calc($header-height + 1rem); // Adjust as needed for larger offset
      height: min-content;
    }
    &__content {
      position: sticky;
      top: calc($header-height + 1rem); // Adjust as needed for larger offset
      height: min-content;
    }
  }

  /* this is 45px */
  @media (min-width: $tablet-breakpoint) {
    .stack {
      gap: unset;
      flex-direction: row;
      justify-content: space-between;
      &__heading {
        padding-right: $spacing-less-related;
      }
    }
  }
</style>
