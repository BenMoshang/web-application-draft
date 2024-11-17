<script>
  let title = "More <br> ABOUT US".toUpperCase();
  let body =
    "We are committed to delivering the best services to our clients, ensuring excellence in every project we undertake.";
  let buttonText = $state("Download Resume".toUpperCase());
</script>

<section class="about">
  <header class="about__header">
    <h2 class="about__title global__display--lg">{@html title}</h2>
  </header>
  <figure class="about__image--wrapper"></figure>
  <p class="about__body global__body--lg">
    {@html body}
  </p>
  <button
    class="about__button global__button--outline"
    aria-label="Transform my brand - Get Started"
    tabindex="0"
  >
    <span class="button-text">{buttonText}</span>
    <img
      src="/assets/icons/resume-icon.svg"
      alt="download our resume"
      class="icon"
    />
  </button>
</section>

<style lang="scss">
  @use "../../SCSS/index.scss" as *;

  /*==========================================
  Variables
===========================================*/
  // Container Padding
  $main-container-inline-padding: clamp(1.25rem, -0.596rem + 6.22vw, 5rem);

  /*====================================
About Section
===========================================*/
  .about {
    @include flex-column-center;
    padding-inline: $main-container-inline-padding;

    // &__header {
    // }

    &__title {
      text-align: center;
    }

    &__image--wrapper {
      width: 21.875rem;
      height: 37.375rem;
      border-radius: 62.5rem;
      @include parallax-section(
        "https://fakeimg.pl/1200x800/?text=Background+Image",
        800px
      );

      &:hover .about__image {
        transform: scale(1.05);
      }
    }

    &__image {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    &__body {
      @include paragraph-ch-inline;
      text-align: center;
    }
  }
</style>
