<!-- TODO: MAKE TITLE POSITION STICKY ON DESKTOP -->
<script>
  let title = $state(`motivation`.toUpperCase());
  let description = `Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae
  consequatur est eligendi repellat ducimus quod at eaque. Fugit voluptates
  recusandae veniam autem quia molestiae quidem nobis similique dolores
  laborum.       <br />
      <br />
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum, vitae consequatur
      est eligendi repellat ducimus quod at eaque. Fugit voluptates recusandae veniam
      autem quia molestiae quidem nobis similique dolores laborum.`;
</script>

<!-- TODO: ADD SIGNATURES -->
<section class="motivation__container">
  <h3 class="motivation__container-heading global__heading--sm">
    {title}
  </h3>

  <p class="global__body--md">
    {@html description}
  </p>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .motivation__container {
    @include section-padding-inline;
    @include flex-column-jus-center;
    @include section-heading-content-gap;
    padding-top: clamp(80px, 3.769rem + 4.15vw, 120px);
    position: relative;
    overflow-y: visible;
    inline-size: 100%;
    height: 100%;
    & p {
      max-inline-size: 50ch;
    }
  }

  .motivation__container-heading {
    position: sticky;
    top: 0; // Adjust as needed for larger offset
    height: min-content;
  }

  /* this is 45px */
  @media (min-width: $tablet-breakpoint) {
    .motivation__container {
      gap: unset;
      justify-content: unset;
      flex-direction: row;
      justify-content: space-between;
    }
  }
</style>
