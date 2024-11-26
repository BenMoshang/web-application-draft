<script>
  import UiTransformCard from "../reusable-components/UiTransformCard.svelte";
  import UITransformFooter from "./UITransformFooter.svelte";
  import UiTransformHeader from "./UITransformHeader.svelte";
  import UITransformWindowHead from "./UITransformWindowHead.svelte";
  //injectable
  let linkText = $state("Continue Reading".toUpperCase());
  let isHovered = $state(true);
  let companyName = $state("Your Business");

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

<!-- false mouse out 
 false blur -->

<main
  on:focus={() => (isHovered = true)}
  on:mouseover={() => (isHovered = true)}
  on:mouseout={() => (isHovered = true)}
  on:blur={() => (isHovered = true)}
  class:is-hovered={isHovered}
  class="main-container"
>
  <UITransformWindowHead />
  <h1 class="main-container__title"
    >The One Web Design Secret That Generates Revenue!</h1
  >
  <!-- <aside class:is-hovered={isHovered} class="sidebar">
    <h2>User Menu</h2>
    <button>Dashboard</button>
    <button>Settings</button>
    <button>Logout</button>
  </aside> -->
  <section class:is-hovered={isHovered} class="content-container">
    <UiTransformHeader />

    <article class="card-container__card">
      <UiTransformCard />
    </article>
    <!-- <article class="card-container__card">
        <div>
          <h2>{@html cardContent[0].title}</h2>
          <p>{@html cardContent[0].description}</p>

          <a
            href="https://www.forbes.com/advisor/business/software/website-statistics/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Forbes Website Statistics"
          >
            {linkText}
            <svg
              stroke-width="2"
              stroke="currentColor"
              viewBox="0 0 24 24"
              fill="none"
              class="h-6 w-6"
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

        <figure>
          <img
            src="../../../static/assets/UITransformSection/UI-image.webp"
            alt="A Representative of how your website is lossed in the internet"
            class="card__image"
            loading="lazy"
            role="presentation"
            width="100%"
            height="auto"
          />
        </figure>
      </article> -->
    <!-- TODO: PUT DIGITAL STORE FRONT 3D WEB ASSET HERE  -->

    <!-- <article class="card-container__card">
        <figure>
          <img
            src="../../../static/assets/UITransformSection/digital-storefront.webp"
            alt="A Representative of how your website is lossed in the internet"
            class="card__image"
            loading="lazy"
            role="presentation"
            width="100%"
            height="100%"
          />
        </figure>
        <div>
          <h2>
            A Website is a Business's <strong class="shine-animation"
              >Digital Storefront</strong
            >
          </h2>
          <p>
            A <em>well-designed and optimized website</em> serves
            <strong> as the digital storefront of your brand. </strong>

            Every click, scroll, and interaction reflects how your audience
            perceives your business. If your website is
            <em>slow, unresponsive, or outdated</em>, it can tarnish your
            reputation and drive potential customers away.
          </p> -->
    <!-- TODO: PROPERLY USE STRONG AND EM TAGS IN THIS PARAGRAPH
           TODO: USE THE @INJECTABLE FOR BETTER MANAGEMENT OF THE TEXT -->
    <!-- <p>
            <em>Remember the reach you have is endless... </em>
            <strong>
              However, to stand out among the billions of websites, it's vital
              to implement robust SEO strategies, maintain mobile-friendly
              design, and prioritize user experience (UX)</strong
            >. These factors not only boost your visibility on search engines
            like Google but also build trust with your audience, encouraging
            repeat visits and conversions.
          </p> -->
    <!-- <p>
            Remember, your website is often the first impression a customer has
            of your business. Make it count by investing in its design, speed,
            content quality, and functionality. A strong digital presence can
            turn visitors into loyal customers and set you apart in a crowded
            online marketplace.
          </p> -->
    <!-- <a
            href="https://www.forbes.com/advisor/business/software/website-statistics/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Forbes Website Statistics"
          >
            {linkText}
            <svg
              stroke-width="2"
              stroke="currentColor"
              viewBox="0 0 24 24"
              fill="none"
              class="h-6 w-6"
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
      </article>
      <article class="card-container__card">
        <div>
          <h2>
            The secret to <strong class="shine-animation"
              >Maximizing Your Reach</strong
            >
          </h2>
          <p>
            Did you know that only <strong
              >"3% of websites are accessible."</strong
            >
            Being left out of the 97% is detrimental for your business. This is why
            you must prioritize <strong>web accessibility</strong> as a crucial part
            of your digital strategy.
          </p> -->

    <!-- <p>
            Accessibility ensures that all users, including those with
            disabilities, can interact with your website seamlessly. It not only
            fosters inclusivity but also improves your site's usability for
            everyone.
          </p>
          <p>
            Making your website accessible isn't just about <em>compliance;</em>
            it's a business opportunity. Studies show that businesses with accessible
            websites gain access to a larger audience, enhance user experience, and
            even improve SEO performance. By addressing accessibility, you're not
            just accommodating a need; you're unlocking potential.
          </p> -->
    <!-- <p>
            Additionally, accessibility compliance can help your business avoid
            costly lawsuits. With increasing legal regulations such as the
            Americans with Disabilities Act (ADA), ensuring your website meets
            accessibility standards is more important than ever.
          </p> -->
    <!-- <a
            href="https://www.audioeye.com/post/accessibility-statistics/#:~:text=What%20we%20found%20is%20that,but%20for%20businesses%20as%20well."
            target="_blank"
            rel="noopener noreferrer"
            aria-label="AudioEye Accessibility Statistics"
          >
            {linkText}
            <svg
              stroke-width="2"
              stroke="currentColor"
              viewBox="0 0 24 24"
              fill="none"
              class="h-6 w-6"
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
        <figure>
          <img
            src="../../../static/assets/UITransformSection/UI-image.webp"
            alt="A Representative of how your website is lossed in the internet"
            class="card__image"
            role="presentation"
            loading="lazy"
            width="100%"
            height="100%"
          />
        </figure>
      </article>
    </section> -->

    <UITransformFooter />
  </section>
</main>

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
