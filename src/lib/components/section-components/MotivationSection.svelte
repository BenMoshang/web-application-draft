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
<section class="motivation">
  <h3 class="motivation__heading global__heading--sm">
    {title}
  </h3>

  <p class=" motivation__body global__body--md">
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

  .motivation {
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

    &__body {
      @include paragraph-ch-inline;
    }
  }

  /* this is 45px */
  @media (min-width: $tablet-breakpoint) {
    .motivation {
      gap: unset;
      flex-direction: row;
      justify-content: space-between;
      &__heading {
        padding-right: $spacing-less-related;
      }
    }
  }
</style>
