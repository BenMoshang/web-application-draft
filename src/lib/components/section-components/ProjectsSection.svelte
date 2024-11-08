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
<section class="projects">
  <header class="projects__header">
    <h3 class="projects__heading global__display--lg">
      {@html title}
    </h3>
    <p class="projects__body global__body--md">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae
      consequatur est eligendi repellat ducimus quod at eaque. Fugit voluptates
      recusandae veniam autem quia molestiae quidem nobis similique dolores
      laborum.
    </p>
  </header>
  <section class="projects__container">
    {#each projectsData as { imageSrc, title, description, label }}
      <ImageCard {title} {description} {imageSrc} {label} />
    {/each}
  </section>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;
  /* ===============================================
                    Variables
=============================================== */
  $header-padding-top: clamp(60px, 0.323rem + 11.54vw, 140px);
  $container-inline-padding: clamp(20px, 1.127rem + 0.41vw, 24px);
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .projects {
    padding-top: $header-padding-top;
    width: 100%;
    display: flex;
    flex-direction: column;
    @include section-heading-content-gap;

    &__header {
      @include flex-column-jus-center;
    }

    &__heading {
      text-align: center;
    }

    &__body {
      display: none;
      max-inline-size: 50ch;
    }

    &__container {
      padding-inline: $container-inline-padding;

      width: 100%;
      height: fit-content;
      display: grid;

      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      place-items: center;

      @include section-inner-gap;
    }
  }
  @media (min-width: 475px) {
    .projects {
      &__container {
        grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      }
    }
  }
  @media (min-width: 1440px) {
    .projects {
      &__heading {
        text-align: left;
      }

      &__header {
        all: unset;
        @include flex-center-between;
        padding-inline: $container-inline-padding;
      }

      &__body {
        display: inline-flex;
      }

      &__container {
        grid-template-columns: repeat(auto-fill, minmax(500px, 1fr));
      }
    }
  }
</style>
