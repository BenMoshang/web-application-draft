<script>
  import ImageCard from "../reusable-components/ImageCard.svelte";

  let title = `FEATURED<br/> PROJECTS`;

  const projectsData = [
    {
      imageSrc: "https://via.placeholder.com/400",
      title: "Business",
      description: "Lorem ",
      label: "2024",
    },
    {
      imageSrc: "https://via.placeholder.com/400",
      title: "Technology",
      description: "Lorem",
      label: "2024",
    },
    {
      imageSrc: "https://via.placeholder.com/400",
      title: "Marketing",
      description: "Lorem",
      label: "2024",
    },
  ];
</script>

<!-- TODO: NEED TO FIX GRID AND RESPONSIVENESS
 TODO: MAKE THE P TAG APPEAR FOR TABLETS AND DESKTOPS -->
<section class="projects pinline-lg">
  <h1 class="projects__title global__title--md">
    {@html title}
  </h1>
  <p class="projects__description global__paragraph--sm">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae
    consequatur est eligendi repellat ducimus quod at eaque. Fugit voluptates
    recusandae veniam autem quia molestiae quidem nobis similique dolores
    laborum.
  </p>
  <section class="projects__container">
    {#each projectsData as { imageSrc, title, description, label }}
      <ImageCard {title} {description} {imageSrc} {label} />
    {/each}
  </section>
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .projects {
    width: 100%;
    padding-top: var(--fsz-lg);
    display: flex;
    flex-direction: column;
    gap: var(--spacing-2xl);

    & .projects__title {
      text-transform: capitalize;
      text-align: center;
    }

    & .projects__description {
      display: none;
    }

    & .projects__container {
      width: 100%;
      height: fit-content;
      display: grid;

      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      place-items: center;

      gap: var(--fsz-md);
    }
  }
</style>
