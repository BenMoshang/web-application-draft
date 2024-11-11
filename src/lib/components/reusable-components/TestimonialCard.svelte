<script>
  /**
   * @typedef {Object} Props
   * @property {string} [name]
   * @property {string} [position]
   * @property {string} [pfpSrc]
   * @property {string} [companySrc]
   * @property {string} [description]
   */

  /** @type {Props} */
  let {
    name = $bindable(""),
    position = "",
    pfpSrc = "",
    companySrc = "",
    description = "",
  } = $props();
  name = name.toUpperCase();
  position = position.toUpperCase();
</script>

<article class="card">
  <header class="card__header">
    <img src={pfpSrc} alt={name} class="card__pfp" />
    <div class="card__title-wrapper">
      <h4 class="global__card-heading--sm">{name}</h4>
      <h5 class="card__position global__card-subheading">{position}</h5>
    </div>
    {#if companySrc}
      <img src={companySrc} alt={position} class="card__company" />
    {/if}
  </header>
  <p class="card__body global__card-body--xs">
    "{description}"
  </p>
</article>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    @include flex-column-jus-center;
    @include card-styling;
    @include card-border;
    min-inline-size: 17.5rem; //for mobile responsiveness
    block-size: 100%;
    inline-size: 100%;

    &__header {
      @include flex-center;
      margin-bottom: $spacing-less-related;
    }

    /* --------------------------------------------------
       image styles
-------------------------------------------------- */

    &__company,
    &__pfp {
      border-radius: $br-default;
    }

    &__pfp {
      $size: 3.75rem;

      inline-size: $size;
      block-size: $size;
      margin-right: $spacing-semi-related;
    }
    // makes it to the right
    &__company {
      $size: 3.125rem;
      inline-size: $size;
      block-size: $size;
      margin-left: auto;
    }

    /* --------------------------------------------------
       body styles
-------------------------------------------------- */

    &__position {
      font-size: $fsz-4xs;
      color: $text-tertiary;
      letter-spacing: 0.04em;
      line-height: $lh-lg;
    }
    &__body {
      box-shadow: $shadow-sm-inset;
      padding: $card-inner-padding;
      border-radius: $br-default;
      background: $color-card-bg-secondary;
      font-weight: $fw-regular;
      color: $text-secondary;
    }
  }
</style>
