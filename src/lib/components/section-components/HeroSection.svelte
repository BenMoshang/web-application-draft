<script>
  // TODO: COPYWRITE
  let label = $state("Establish Your Brand's Presence".toUpperCase());
  let title = $state("Engage".toUpperCase());
  let titlePart2 = $state(" Captivate".toUpperCase());
  let titlePart3 = $state("elevate".toUpperCase());
  let buttonText = $state("Get Started".toUpperCase());
</script>

<section class="hero-section">
  <header class="hero-section__header">
    <h2 class="hero-section__header__label global__label">{label}</h2>
    <h1 class="global__display--xl">
      <span>{@html title}</span><br />
      <span>{@html titlePart2}</span><br />
      <span>{@html titlePart3}</span>
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
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
    /* Remove or comment out in production */
    // outline: 1px dashed red;
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
  }
</style>
