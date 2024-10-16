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

<section class="projects pinline-lg">
  <h1 class="projects__title global__title--md">
    {@html title}
  </h1>

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
      margin-right: auto;
    }

    & .projects__container {
      width: 100%;
      height: fit-content;
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(450px, 1fr));
      gap: var(--fsz-md);
    }
  }
</style>
