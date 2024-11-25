<script>
  export let title = "Default Title";
  export let imageSrc = "";
  export let imageAlt = "Card Image";
  export let linkHref = "#";
  export let linkText = "Continue Reading";
  export let linkAriaLabel = "Continue Reading Link";
</script>

<article class="card">
  <div class="card__content">
    <h2 class="card__title">{title}</h2>
    <slot name="content">Default content goes here.</slot>
    <a
      href={linkHref}
      target="_blank"
      rel="noopener noreferrer"
      aria-label={linkAriaLabel}
      class="card__link"
    >
      {linkText}
      <svg
        stroke-width="2"
        stroke="currentColor"
        viewBox="0 0 24 24"
        fill="none"
        class="card__icon"
        xmlns="http://www.w3.org/2000/svg"
        width="20px"
      >
        <path
          d="M14 5l7 7m0 0l-7 7m7-7H3"
          stroke-linejoin="round"
          stroke-linecap="round"
        ></path>
      </svg>
    </a>
  </div>
  {#if imageSrc}
    <figure class="card__figure">
      <img src={imageSrc} alt={imageAlt} class="card__image" loading="lazy" />
    </figure>
  {/if}
</article>

<style lang="scss" scoped>
  .card {
    padding: $card-padding;
    font-family: $ff-old;

    h2 {
      margin-bottom: $spacing-semi-related;
    }

    p {
      margin-bottom: $spacing-less-related;
    }

    a {
      & svg {
        display: none;
      }
    }

    img {
      display: none;
    }
  }
  /*===========================================
   NEW UI styles
=========================================== */
  &.is-hovered {
    h1,
    h2 {
      @include global__heading;
      max-inline-size: $title-max-width; //ch width
    }
    h1 {
      font-size: $fsz-xl;
      text-align: center;
      font-weight: 800;
      color: black;
      margin-inline: auto;
      margin-top: $section-inner-gap-lg;
    }
    & .card-container__card {
      max-inline-size: fit-content;
      @include flex(row, space-between, center);
      flex-wrap: wrap;
      gap: $card-image-content-gap;

      & > * {
        flex: 1;
      }

      & figure {
        overflow: hidden;
        border-radius: $br-default;

        & img {
          display: inline-flex;
          object-fit: cover;

          border-radius: inherit;

          &:hover {
            scale: 1.1;
          }
        }
      }

      h2 {
        line-height: 1.2;
        font-size: 2.5rem;
        margin-bottom: $spacing-less-related;
      }

      p {
        @include global__body;
        max-inline-size: $paragraph-max-width; //ch width
        line-height: $new-p-line-height;
        font-weight: $fw-medium;
        font-size: $fsz-sm;
        color: $text-secondary;
        margin-bottom: $spacing-semi-related;
      }

      a {
        margin-top: $spacing-closely-related;
        //this is for icon sizing too
        $link-font-size: $fsz-3xs;
        $link-color: $color-primary;
        @include global__links;
        font-size: $link-font-size;
        text-underline-offset: 0.125rem; //lowers underline

        &:hover {
          color: $link-color;
          filter: brightness(0.8);
          & svg {
            margin-left: $spacing-closely-related; //spacing from icon and text
            @include animation-float-and-replace--rotated-icon;

            & path {
              fill: $link-color;
            }
          }
        }

        & svg {
          inline-size: $link-font-size;
          height: $link-font-size;
          transform: rotate(-45deg);
          display: inline-flex;
        }
      }

      /*===========================================
  SECOND CARD
=========================================== */
      &:nth-child(3) {
        & div {
          @include card-styling;

          background: hsl(221, 100%, 86%);
          box-shadow: $shadow-md;
        }
        & figure {
          inline-size: 100%;
          block-size: 100%;
          & img {
            @include drop-shadow-md;
            inline-size: 100%;
            block-size: 100%;
            object-fit: cover;
          }
        }
        a {
          color: $text-tertiary;
        }
        p {
          color: $text-primary;
          // select third and fourth paragraphs
          &:nth-child(3),
          &:nth-child(4) {
            font-size: $fsz-xs;
          }
        }
      }
      // select 3rd card
      &:nth-child(4) {
        & figure {
          inline-size: 100%;
          block-size: 100%;
        }
        p {
          // select third and fourth paragraphs
          &:nth-child(3),
          &:nth-child(4) {
            font-size: $fsz-xs;
          }
        }
      }
    }
  }
  // select all cards
</style>
