<script>
  let label = $state("establish your".toUpperCase());
  let titleFirst = $state("Modernized".toUpperCase());
  let titleSecond = $state("Web Presence".toUpperCase());
  let buttonText = $state("Get Started".toUpperCase());
  let footerLocation = $state("New York, NY".toUpperCase());

  let description = $state(`Web Development`.toUpperCase());
  let subdescription = $state(`& Design`.toUpperCase());
</script>

<section class="hero-section">
  <header class="hero-section__header">
    <h2 class="hero-section__header__label global__label">{label}</h2>
    <h1 class="global__display--xl">
      <span>{@html titleFirst}</span><br />
      <span>{@html titleSecond}</span>
    </h1>
    <button
      class="hero-section__button global__button--solid"
      aria-label="Get Started"
    >
      {buttonText}
    </button>
  </header>
  <!-- TODO: MOVE SECTION BELOW TO HEADER -->
  <!-- TODO: FOR HEADER [LOCATION] [BURGER] [WHAT WEDO] -->
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
    @include flex-column-center;
    align-items: unset;

    &__header {
      grid-area: header;
      @include flex-column-center;

      & > * {
        flex: 1;
        text-align: center;
        text-wrap: nowrap;
      }
      &__label {
        font-family: $ff-bold;
        font-size: $fsz-xs;
        color: $text-tertiary;
        letter-spacing: $ls-normal;
        margin-bottom: $spacing-semi-related;
      }

      & h1:nth-child(2) {
        margin-bottom: $spacing-less-related;
      }
    }

    &__button {
      cursor: pointer;
    }

    &__content-container {
      @include flex-center-between;
      grid-area: footer;
    }
  }

  .hero-section__content-container {
    &__location,
    &__description {
      color: $color-tertiary;

      font-weight: $fw-medium;
    }

    &__sub-description {
      font-weight: $fw-medium;
    }
  }
</style>
