<script>
  let location = $state("Baltimore, MD".toUpperCase());
  let description = $state(`Web Development`.toUpperCase());
  let subdescription = $state(`& Design`.toUpperCase());

  let label = $state("from vision to web reality".toUpperCase());
  let title = $state("Build, engage, & convert".toUpperCase());
  let buttonText = $state("Transform my brand".toUpperCase());
</script>

<main class="hero-section" role="banner" aria-labelledby="hero-title">
  <header class="hero-section__header">
    <h2 id="hero-label" class="hero-section__header__label global__label">
      {label}
    </h2>
    <h1 id="hero-title" class="hero-section__header__title global__display--xl">
      {@html title}
    </h1>
    <button
      class="hero-section__button global__button--solid"
      aria-label="Transform my brand - Get Started"
      tabindex="0"
    >
      <span class="button-text">{buttonText}</span>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="12"
        width="12"
        viewBox="0 0 512 512"
        aria-hidden="true"
        focusable="false"
        role="img"
      >
        <path
          fill="#ffffff"
          d="M498.1 5.6c10.1 7 15.4 19.1 13.5 31.2l-64 416c-1.5 9.7-7.4 18.2-16 23s-18.9 5.4-28 1.6L284 427.7l-68.5 74.1c-8.9 9.7-22.9 12.9-35.2 8.1S160 493.2 160 480l0-83.6c0-4 1.5-7.8 4.2-10.8L331.8 202.8c5.8-6.3 5.6-16-.4-22s-15.7-6.4-22-.7L106 360.8 17.7 316.6C7.1 311.3 .3 300.7 0 288.9s5.9-22.8 16.1-28.7l448-256c10.7-6.1 23.9-5.5 34 1.4z"
        />
      </svg>
    </button>
  </header>
  <footer class="hero-section__details">
    <span
      class="hero-section__details__location global__label"
      aria-label="Location: {location}">{location}</span
    >
    <span
      class="hero-section__details__description global__label"
      aria-label="Services:"
    >
      {description}
      <span class="hero-section__details__sub-description global__label">
        {subdescription}
      </span>
    </span>
  </footer>
</main>

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
    gap: $section-inner-gap;
    align-items: unset;

    &__header {
      margin-block: auto;
      @include flex-column-center;

      & > * {
        text-align: center;
      }
      &__label {
        font-family: $ff-bold;
        font-size: $fsz-hero-label;
        color: $text-tertiary;
        margin-bottom: $spacing-closely-related;
      }
      &__title {
        margin-bottom: $spacing-less-related;
        @include shine-animation;
      }
    }

    &__details {
      margin-block: auto;
      height: fit-content;
      @include flex-center-between;
      display: none;

      padding-inline: $spacing-less-related;

      &__location,
      &__description,
      &__sub-description {
        font-weight: $fw-medium;
        font-size: $fsz-hero-label;
      }
      /* ----------------------------------------
      Color changes
      ---------------------------------------- */
      &__location,
      &__description {
        color: $color-tertiary;
      }
      &__sub-description {
        color: $color-quaternary;
      }
    }
  }

  @media (min-width: $tablet-breakpoint) {
    .hero-section__details {
      display: flex;
    }
  }
</style>
