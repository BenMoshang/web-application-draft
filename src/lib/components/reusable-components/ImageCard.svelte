<script lang="ts">
  let {
    title = $bindable("") as string,
    description = "" as string,
    imageSrc = "" as string,
    label = $bindable("") as string,
  } = $props();

  let isHovered = $state(false);
</script>

<figure class="card">
  {#if imageSrc}
    <img
      onfocus={() => (isHovered = true)}
      onmouseover={() => (isHovered = true)}
      onmouseout={() => (isHovered = false)}
      onblur={() => (isHovered = false)}
      src={imageSrc}
      alt={title}
      class="card__image"
    />
  {/if}
  <figcaption class="card__content">
    <footer class="content__footer">
      <h4 class="header__title global__card-heading--sm">{title}</h4>

      <p class="global__card-subheading">
        {description}
      </p>
    </footer>
    {#if label}
      <div class="global__card-label--bg">
        <p class:active={isHovered}>{label}</p>
      </div>
    {/if}
  </figcaption>
</figure>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    @include card-styling;
    @include flex-column-jus-center;
    padding: unset;
    height: 100%;
    width: 100%;
    &__title {
      color: $text-primary;
    }
    &__image {
      width: 100%;
      height: 100%;
      max-height: 42.5rem;

      object-fit: fill;
      transition: transform 0.2s ease-in-out;
      isolation: isolate;
      cursor: pointer;
      &:hover {
        transform: scale(1.1);
      }
    }

    &__content {
      @include flex-center-between;
      padding-block: 0.625rem;
      padding-inline: 1.25rem;
      background: $color-card-bg;
      z-index: 2;
    }
  }

  /* This is for the label  */
  .active {
    @include animation-float-and-replace;
  }
</style>
