<!-- TODO: MAKE TITLE POSITION STICKY ON DESKTOP -->
<script>
  let title = `motivation`;
  let description = `Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae
  consequatur est eligendi repellat ducimus quod at eaque. Fugit voluptates
  recusandae veniam autem quia molestiae quidem nobis similique dolores
  laborum.       <br />
      <br />
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae consequatur
      est eligendi repellat ducimus quod at eaque. Fugit voluptates recusandae veniam
      autem quia molestiae quidem nobis similique dolores laborum.`;
  title = title.toUpperCase();
</script>

<section class="motivation__container">
  <article class="motivation__content">
    <h2 class="motivation__title global__title--md">
      {title}
    </h2>
    <p class="motivation__description global__paragraph--sm">
      {@html description}
    </p>
  </article>
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .motivation__container {
    width: 100%;
    padding-inline: var(--pinline-section);
    container: motivation-section / inline-size;
  }
  .motivation__content {
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      "title"
      "description";
    gap: var(--dynamic-3xl);

    & .motivation__title {
      grid-area: title;
    }

    & .motivation__description {
      grid-area: description;
    }
  }
  /* this is 45px */
  @container motivation-section (min-width: 24.3125rem) {
    .motivation__content {
      grid-template-columns: 1fr 1fr;
      grid-template-areas: "title description ";
    }

    .motivation__title {
      position: sticky;
      top: 2.5rem;
    }
  }
</style>
