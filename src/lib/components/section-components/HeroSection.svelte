<script>
  let label = $state("establish your".toUpperCase());
  let title = $state("Modernized <br /> Web Presence".toUpperCase());
  let buttonText = $state("Get Started");
  let footerLocation = $state("New York, NY");

  let description = $state(`Web Development`);
  let subdescription = $state(`& Design`);
</script>

<section class="hero-section">
  <header class="hero-section__header">
    <h2 class="global__label">{label}</h2>
    <h1 class="global__display--xl">{@html title}</h1>
  </header>
  <button
    class="hero-section__button global__button--solid"
    aria-label="Get Started"
  >
    {buttonText}
  </button>
  <footer class="hero-section__content-container">
    <small>
      <span class="hero-section__content-container__location global__label"
        >{footerLocation}</span
      >
    </small>
    <small>
      <span class="hero-section__content-container__description global__label"
        >{description}</span
      >
      <span
        class="hero-section__content-container__sub-description global__label"
        >{subdescription}</span
      >
    </small>
  </footer>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
    /* Remove or comment out in production */
    outline: 1px dashed red;
  }

  .hero-section {
    width: 100%;
    height: 90vh;
    display: grid;
    grid-template-rows: 1fr auto auto;
    grid-template-areas: "header" "button" "footer";

    &__header {
      grid-area: header;
      @include flex-column-center;
      text-align: center;
    }

    &__button {
      grid-area: button;
      cursor: pointer;
    }

    &__content-container {
      @include flex-center-between;
      grid-area: footer;
    }
  }

  .hero-section__content-container {
    @extend .global__label;
    color: red;
  }
</style>
