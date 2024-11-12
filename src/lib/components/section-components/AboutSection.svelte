<script>
  let title = "More <br> ABOUT US".toUpperCase();
  let body =
    "We are committed to delivering the best services to our clients, ensuring excellence in every project we undertake.";
</script>

<section class="about">
  <header class="about__header">
    <h2 class="about__title global__display--lg">{@html title}</h2>
    <figure class="about__image--wrapper">
      <img
        class="about__image"
        src="https://fakeimg.pl/638x400?text=picture+of+us"
        alt="ben + jacky forever"
      />
    </figure>
  </header>
  <p class="about__body global__body--lg">
    {@html body}
  </p>
</section>

<style lang="scss">
  @use "../../SCSS/index.scss" as *;

  /*==========================================
  Variables
===========================================*/
  // Container Padding
  $main-container-inline-padding: clamp(1.25rem, -0.596rem + 6.22vw, 5rem);

  // Layer Z-Indices
  $background-layer-z: -1;
  $base-layer-z: 1;
  $foreground-layer-z: 2;

  // Parallax Settings
  $parallax-height: 100vh;
  $transition-speed-back: 0.5s;
  $transition-speed-front: 0.8s;

  // Colors
  $base-color: #ffffff;
  $background-color: #6a11cb;
  $foreground-color: #2575fc;
  $text-color: #fff;

  /*==========================================
  Mixins
===========================================*/

  /* Parallax Layer Mixin */
  @mixin parallax-layer($depth) {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform: translateZ($depth * 100px) scale(1.5);
    will-change: transform;

    // Determine transition speed based on depth
    @if $depth > 1 {
      transition: transform $transition-speed-front ease-out;
    } @else {
      transition: transform $transition-speed-back ease-out;
    }
  }

  /* Main Container Mixin */
  @mixin parallax-container {
    position: relative;
    height: $parallax-height;
    overflow: hidden;
    perspective: 1px;
    transform-style: preserve-3d;
  }

  /* Layer Position Mixin */
  @mixin layer-position($zIndex) {
    position: relative;
    z-index: $zIndex;
  }

  /* Flex Center Column Mixin */
  @mixin flex-center-column {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  /* Paragraph Styling Mixin */
  @mixin paragraph-style {
    @include paragraph-ch-inline;
    color: $text-color;
  }

  /*==========================================
  About Section
===========================================*/
  .about {
    @include flex-center-column;
    padding-inline: $main-container-inline-padding;
    position: relative;
    overflow: hidden;

    &__header {
      @include parallax-container;

      &::before {
        content: "";
        @include parallax-layer(0.5);
        background-color: $background-color;
        z-index: $background-layer-z;
      }
    }

    &__title {
      @include layer-position($foreground-layer-z);
      text-align: center;
      transform: translateY(-20%) scale(1.2);
      color: $text-color;
      transition: transform $transition-speed-front ease-out;
    }

    &__image-wrapper {
      @include layer-position(1.5);
      @include parallax-layer(1.2);
      transform-style: preserve-3d;
      width: 21.875rem;
      height: 37.375rem;
      border-radius: 50%;
      overflow: hidden; /* Ensures the image doesn't overflow the wrapper */
    }

    &__image {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform $transition-speed-back ease-out;
    }

    &__body {
      @include paragraph-style;
      position: relative;
      z-index: $base-layer-z;
      /* Optional: Add parallax effect to body content */
      transform: translateY(0);
      transition: transform $transition-speed-back ease-out;
    }

    /* Hover or Scroll Effects (Optional) */
    /* Example: Scale image on hover */
    &:hover .about__image {
      transform: scale(1.05);
    }
  }

  /*==========================================
  Responsive Adjustments
===========================================*/
</style>
