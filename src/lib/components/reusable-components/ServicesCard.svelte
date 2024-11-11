<script>
  /**
   * @typedef {Object} Props
   * @property {string} [title]
   * @property {string} [description]
   * @property {string} [counter]
   * @property {string} [label]
   */

  /** @type {Props} */
  let {
    title = $bindable(""),
    description = "",
    counter = "",
    label = $bindable(""),
  } = $props();
  title = title.toUpperCase();
  label = label.toUpperCase();
</script>

<!-- TODO: NEED TO FIX SVG SIZE SO CROSS NOT FAT-->
<article class="card">
  <button
    class="card__button"
    type="button"
    aria-label="Expand service details"
  >
    <svg
      class="card__icon"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 448 512"
      aria-hidden="true"
      focusable="false"
      ><path
        d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 144L48 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l144 0 0 144c0 17.7 14.3 32 32 32s32-14.3 32-32l0-144 144 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l-144 0 0-144z"
      /></svg
    >
  </button>

  <div class="card__content">
    {#if counter}
      <p
        class="card__counter global__card-heading--sm"
        aria-label="Service count"
      >
        ({counter})
      </p>
    {/if}
    <div class="card__heading">
      <h3 class="global__card-heading--lg">
        {title}
      </h3>
      {#if label}
        <span class="global__card-label--bg">{label}</span>
      {/if}
    </div>

    <p class="card__body global__card-body">
      {description}
    </p>
  </div>
</article>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  h3 {
    @include shine-animation-text;
  }

  .card {
    @include flex-column-jus-center;
    @include card-styling;
    flex: 1 1 calc(33.33% - $section-inner-gap); // to account for that ghap in the container
    max-height: 18.375rem;
    height: 100%;
    min-width: 17.5rem; //for mobile responsiveness
    width: 100%;

    &__heading {
      margin-top: $spacing-semi-related;
      display: flex;
      align-content: center;
      align-items: center;
      width: 100%;
      gap: $spacing-closely-related;
    }
    &__body {
      margin-top: $spacing-closely-related;
      max-inline-size: 50ch;
    }
    &__button {
      @include flex-center;
      $icon-size: 2.25rem;
      $bg-size: 3.125rem;
      border: none;
      margin-left: auto;
      width: $bg-size;
      height: $bg-size;
      border-radius: $br-rounded;
      cursor: pointer;
      background: $color-secondary;
      box-shadow:
        inset $shadow-sm,
        $shadow-sm;
      &:hover {
        & svg {
          transform: rotate(90deg);
        }
      }

      & svg {
        transition: transform 0.2s ease-in-out;
        width: $icon-size;
        height: $icon-size;

        & path {
          fill: $color-gray-md;
        }
      }
    }
  }
</style>
