<script>
  import UITransformFooter from "./UITransformFooter.svelte";
  import UITransformWindowHead from "./UITransformWindowHead.svelte";
  //injectable
  let linkText = "Continue Reading".toUpperCase();
  export let isHovered = true;
  export let companyName = "Your Business";

  let cardContent = [
    {
      title: `            Your Presence is Defined by <strong class="shine-animation"
              >Your Website</strong
            >`,
      description: `            With the growth of the internet, "1.09 billion websites are on the
            internet." It is <strong>crucial</strong> to ensure that your
            digital presence is not a needle in a haystack. Not only does it
            need to be
            <em>visually appealing and viewable on all devices...</em>
            but it is also essential to be
            <em><strong>HIGHLY</strong> optimized</em> for search engines to reach
            your target audience.`,
    },
  ];
</script>

<header class="content-container__header" class:is-hovered={isHovered}>
  <h2 class="header__title">{companyName}</h2>
  <nav class="header__nav">
    <a class="header__nav-link" href="#">Home</a>
    <a class="header__nav-link" href="#">Services</a>
    <a class="header__nav-link" href="#">Contact</a>
  </nav>
</header>

<style lang="scss" scoped>
  @use "./src/lib/SCSS/index.scss" as *;
  *,
  *::after,
  *::before {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    will-change: all;
    transition: all 0.5s ease-in-out;
  }
  $footer-shadow-color: hsl(240, 4%, 8%);
  $footer-shadow:
    0.4px 0.3px 0.4px
      hsl(
        hue($footer-shadow-color),
        saturation($footer-shadow-color),
        lightness($footer-shadow-color) / 0.88
      ),
    0.5px 0.5px 0.5px -1.2px hsl(hue($footer-shadow-color), saturation($footer-shadow-color), lightness(
            $footer-shadow-color
          ) / 0.7),
    1.4px 1.4px 1.5px -2.5px hsl(hue($footer-shadow-color), saturation($footer-shadow-color), lightness(
            $footer-shadow-color
          ) / 0.52),
    3.9px 3.8px 4.1px -3.7px hsl(hue($footer-shadow-color), saturation($footer-shadow-color), lightness(
            $footer-shadow-color
          ) / 0.35),
    8.8px 8.5px 9.2px -5px hsl(hue($footer-shadow-color), saturation($footer-shadow-color), lightness(
            $footer-shadow-color
          ) / 0.17);
  $footer-shadow-inset:
    inset $footer-shadow,
    $footer-shadow;
  /*===========================================
   header
=========================================== */
  $header-content-gap: 2rem;
  //this is for the before class in the header if you wanted to use AN ICON next to the title
  $header-first-icon: url("../../../static/assets/icons/page/home-icon.svg");
  $header-second-icon: url("../../../static/assets/icons/page/services-icon.svg");
  $header-third-icon: url("../../../static/assets/icons/page/contact-icon.svg");
  $header-background: red;
  $hovered-header-background: color-with-opacity(800, 0.03);
  /*------CARD-------*/
  $card-image-content-gap: 2rem;
  $new-p-line-height: 1.65;
  /*===========================================
    Windows Bar
=========================================== */
  $winhead-header-gap: 2rem;
  /*===========================================
   Footer
=========================================== */
  $footer-background: darkred;
  $hovered-footer-background: #0c2461;
  img {
    transition: all 0.4s ease-in-out;
  }

  a,
  svg {
    transition: all 0.2s ease-in-out;
  }

  .shine-animation {
    @include shine-animation-text;
  }

  /*===========================================
    Windows Bar
=========================================== */
  .main-container {
    @include card-border;
    transition: all 0.5s ease-in-out;
    border-radius: $br-default;

    @include flex-column-center;

    height: calc(100% - $header-height);
    width: 100%;
    position: relative;
    rotate: x 45deg;
    perspective: 1000px;
    // transform: skew(-5deg) scale(0.9);
    transition:
      transform 0.8s cubic-bezier(0.17, 0.55, 0.55, 1),
      opacity 0.6s ease;

    &.is-hovered {
      rotate: x 0deg;
      // transform: skew(0deg) scale(1);
      box-shadow: $shadow-lg;
    }
  }
  /*-----uncomment if later addition want a sidebar-----------*/
  // .sidebar {
  //   display: none;

  //   @media (min-width: $desktop-breakpoint) {
  //     // shows on breakpoint
  //     @include section-padding-inline;

  //     @include flex(column, flex-start, stretch);
  //     gap: $spacing-closely-related;
  //     inline-size: 100%;

  //     & h2 {
  //       text-wrap: nowrap;
  //     }

  //     // new ui styling
  //     &.is-hovered {
  //       overflow-x: hidden;
  //       inline-size: 0%;
  //       max-inline-size: fit-content;

  //       &:hover {
  //         @include section-padding-inline;
  //         inline-size: 100%;
  //       }
  //     }
  //   }
  // }

  .content-container {
    @include flex(column, flex-start, stretch);
    grid-area: container;
    width: 100%;
    height: 100%;
    font-family: $ff-old;

    &.is-hovered {
      @include flex-column-center;
      margin: 0 auto;
    }
  }
  /*===========================================
    header styles
=========================================== */
  .content-container__header {
    @include flex(row, space-between);
    overflow: hidden;
    width: 100%;
    height: $header-height;
    padding-block: $component-padding-2xs;
    padding-inline: $component-padding-md;
    background: $header-background;
    &__nav {
      @include flex;
      gap: $spacing-closely-related;
    }
    // new ui styling
    &.is-hovered {
      align-self: center;
      width: 90%;

      margin-top: $winhead-header-gap;

      background: $hovered-header-background;
      backdrop-filter: blur(0.75rem);
      border-radius: $br-rounded;
      border: 0.0625rem solid $color-border;
      box-shadow: $shadow-md;

      & .header__title {
        $title-font-size: $fsz-2xs;
        @include global__heading;
        font-size: $title-font-size;
        // position: relative;

        // &::before {
        //   content: "";
        //   align-self: baseline;
        //   margin-right: $spacing-closely-related;
        //   display: inline-flex;
        //   z-index: 999;
        //   inline-size: $title-font-size;
        //   block-size: $title-font-size;
        //   background-image: $my-modern-icon;
        //   background-size: contain;
        //   background-repeat: no-repeat;
        //   background-position: center;
        // }
      }

      & .header__nav {
        gap: $spacing-less-related;

        &-link {
          $icon-size: 0.75rem;
          inline-size: $icon-size;
          block-size: $icon-size;
          font-size: $icon-size;
          text-decoration: none;
          color: transparent;
          // background icon
          background-size: contain;
          background-repeat: no-repeat;
          background-position: center;

          &:nth-child(1) {
            background-image: $header-first-icon;
          }

          &:nth-child(2) {
            background-image: $header-second-icon;
          }
          &:nth-child(3) {
            background-image: $header-third-icon;
          }
        }
      }
    }
  }
  /*===========================================
    card container styles
=========================================== */
  .card-container {
    flex: 1;
    @include flex(column, flex-start, stretch);
    @include section-inner-gap-lg;
    @include section-padding-inline;
    padding-block: 1.875rem;
    inline-size: 100%;
    block-size: 100%;

    &__card {
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
  }
</style>
