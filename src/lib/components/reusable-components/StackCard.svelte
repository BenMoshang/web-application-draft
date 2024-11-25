<script>
  import ContactSection from "./../section-components/ContactSection.svelte";
  /**
   * @typedef {Object} Props
   * @property {string} [imageSrc]
   * @property {string} [title]
   * @property {string} [useCase]
   * @property {string} [description]
   */

  /** @type {Props} */
  let {
    imageSrc = "",
    title = $bindable(""),
    useCase = $bindable(""),
    description = "",
  } = $props();
  title = title.toUpperCase();
  useCase = useCase.toUpperCase();
</script>

<article class="card">
  <img src={imageSrc} alt={title} class="card__image" />
  <section class="card__content">
    <h4 class="card__content-heading global__card-heading--md">
      {title}
    </h4>
    <h5 class="card__content-use-case global__card-heading--sm">
      {useCase}
    </h5>
    <p class="card__content-body global__card-body--sm">
      {description}
    </p>
  </section>
</article>

<style lang="scss">
  @use "../../SCSS/index.scss" as *;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  $card-gap: clamp(1.25rem, 1.127rem + 0.41vw, 1.5rem); //20 - 24px

  .card {
    @include flex-center;
    inline-size: fit-content;
    overflow: hidden;

    &__content {
      @include flex-center;
      inline-size: 100%;

      &-heading {
      }

      &-body {
      }
    }

    & img {
      //TODO: PUT A BACKGROUND HERE
      $image-size: 2.875rem;
      max-inline-size: $image-size;
      max-block-size: $image-size;
      object-fit: contain;
      will-change: transform;

      &:hover {
        transform: scale(1.05);
      }
    }
  }
  // @container (max-width: 475px) {
  //   .card {
  //     flex-direction: column;
  //   }

  //   .card__image-wrapper {
  //     width: 100%;
  //   }

  //   .card__image {
  //     margin-inline: auto;
  //   }
  // }
</style>
