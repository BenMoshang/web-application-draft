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
    @include flex-column-center;

    &__header {
      grid-area: header;
      margin-bottom: 1rem;
      place-self: center;

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
        margin-bottom: $dynamic-spacing-xs;
      }
    }

    &__button {
      place-self: center;
      grid-area: button;
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
