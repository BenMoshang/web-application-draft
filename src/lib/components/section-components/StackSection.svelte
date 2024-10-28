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

<section class="stack__container">
  <article class="stack__content">
    <h2 class="stack__title global__title--md">FAVORITE STACK</h2>
    <div class="content__cards-container">
      {#each stackData as { imageSrc, title, useCase, description }}
        <StackCard {imageSrc} {title} {useCase} {description} />
      {/each}
    </div>
  </article>
</section>

<style lang="scss">

  .stack__container {
    width: 100%;
    padding-inline: var(--pinline-section);
    container: stack-section / inline-size;
  }
  .stack__content {
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      "title"
      "cards";
    gap: var(--dynamic-3xl);

    & .stack__title {
      grid-area: title;
    }

    & .content__cards-container {
      grid-area: cards;

      gap: var(--dynamic-md);
    }
  }
  @container stack-section (min-width: 24.3125rem) {
    .stack__content {
      grid-template-columns: 1fr 1fr;
      grid-template-areas: "title cards";
    }

    .stack__title {
      position: sticky;
    }
  }
</style>
