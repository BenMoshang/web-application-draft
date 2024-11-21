<script>
  let isHovered = false;
  let linkText = "Continue Reading".toUpperCase();
</script>

<!-- false mouse out 
 false blur -->
<main
  on:focus={() => (isHovered = true)}
  on:mouseover={() => (isHovered = true)}
  on:mouseout={() => (isHovered = false)}
  on:blur={() => (isHovered = false)}
  class:is-hovered={isHovered}
  class="main-container"
>
  <header class="winhead">
    <section class="winhead__button-container">
      <div class="close"></div>
      <div class="min"></div>
      <div class="max"></div>
    </section>
    <h2 class:is-hovered={isHovered} class="page-name">HOVER ME</h2>
  </header>
  <aside class:is-hovered={isHovered} class="sidebar">
    <h2>User Menu</h2>
    <button>Dashboard</button>
    <button>Settings</button>
    <button>Logout</button>
  </aside>
  <section class:is-hovered={isHovered} class="content-container">
    <header class="content-container__header" class:is-hovered={isHovered}>
      <h2 class="header__title">Your Website</h2>
      <nav class="header__nav">
        <a class="header__nav-link" href="#">Home</a>
        <a class="header__nav-link" href="#">Services</a>
        <a class="header__nav-link" href="#">Contact</a>
      </nav>
    </header>

    <section class:is-hovered={isHovered} class="card-container">
      <h1>The One Web Design Secret That Generates Revenue!</h1>
      <article class="card-container__card">
        <div>
          <h2>Your Presence is Defined by Your Website</h2>
          <p>
            With the growth of the internet, "1.09 billion websites are on the
            internet." It is <strong>crucial</strong> to ensure that your
            digital presence is not a needle in a haystack. Not only does it
            need to be
            <em>visually appealing and viewable on all devices...</em>
            but it is also essential to be
            <em><strong>HIGHLY</strong> optimized</em> for search engines to reach
            your target audience.
          </p>
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
      </article>
      <article class="card-container__card">
        <figure>
          <img
            src="../../../static/assets/UITransformSection/UI-image.webp"
            alt="A Representative of how your website is lossed in the internet"
            class="card__image"
            loading="lazy"
            role="presentation"
            width="100%"
            height="100%"
          />
        </figure>
        <div>
          <h2>A website is a Business's Digital Storefront</h2>
          <p>
            A <em>well-designed and optimized website</em> serves
            <strong> as the digital storefront of your brand. </strong>

            Every click, scroll, and interaction reflects how your audience
            perceives your business. If your website is
            <em>slow, unresponsive, or outdated</em>, it can tarnish your
            reputation and drive potential customers away.
          </p>
          <!-- TODO: PROPERLY USE STRONG AND EM TAGS IN THIS PARAGRAPH
           TODO: USE THE @INJECTABLE FOR BETTER MANAGEMENT OF THE TEXT -->
          <p>
            <em>Remember the reach you have is endless... </em>
            <strong>
              However, to stand out among the billions of websites, it's vital
              to implement robust SEO strategies, maintain mobile-friendly
              design, and prioritize user experience (UX)</strong
            >. These factors not only boost your visibility on search engines
            like Google but also build trust with your audience, encouraging
            repeat visits and conversions.
          </p>
          <!-- <p>
            Remember, your website is often the first impression a customer has
            of your business. Make it count by investing in its design, speed,
            content quality, and functionality. A strong digital presence can
            turn visitors into loyal customers and set you apart in a crowded
            online marketplace.
          </p> -->
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
      </article>
      <article class="card-container__card">
        <div>
          <h2>The secret to Maximizing Your Reach</h2>
          <p>
            Did you know that only <strong
              >"3% of websites are accessible."</strong
            >
            Being left out of the 97% is detrimental for your business. This is why
            you must prioritize <strong>web accessibility</strong> as a crucial part
            of your digital strategy. Accessibility ensures that all users, including
            those with disabilities, can interact with your website seamlessly. It
            not only fosters inclusivity but also improves your site's usability
            for everyone.
          </p>
          <p>
            Making your website accessible isn't just about <em>compliance;</em>
            it's a business opportunity. Studies show that businesses with accessible
            websites gain access to a larger audience, enhance user experience, and
            even improve SEO performance. By addressing accessibility, you're not
            just accommodating a need; you're unlocking potential.
          </p>
          <!-- <p>
            Additionally, accessibility compliance can help your business avoid
            costly lawsuits. With increasing legal regulations such as the
            Americans with Disabilities Act (ADA), ensuring your website meets
            accessibility standards is more important than ever.
          </p> -->
          <a
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
    </section>
    <footer class="footer">
      <p>&copy; 2024 Your Company. All rights reserved.</p>
    </footer>
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
    outline: 1px dashed red;
  }
  /*===========================================
    Old UI VARIABLES 
=========================================== */
  $header-background: red;
  $footer-background: darkred;
  /*===========================================
    NEW UI VARIABLES 
=========================================== */
  /*------HEADER -------*/
  $header-content-gap: 2rem;
  //this is for the before class in the header if you wanted to use AN ICON next to the title
  $my-modern-icon: url("../../../static/assets/icons/page/our-logo-icon.png");
  $header-first-icon: url("../../../static/assets/icons/page/home-icon.svg");
  $header-second-icon: url("../../../static/assets/icons/page/services-icon.svg");
  $header-third-icon: url("../../../static/assets/icons/page/contact-icon.svg");
  $hovered-header-background: color-with-opacity(800, 0.03);
  /*------CARD-------*/
  $card-image-content-gap: 2rem;
  /*===========================================
    Windows Bar
=========================================== */

  img {
    transition: all 0.4s ease-in-out;
  }

  a,
  svg {
    transition: all 0.2s ease-in-out;
  }
  .winhead {
    grid-area: winhead;
    width: 100%;
    height: 2.25rem;
    background: rgb(244, 244, 244);
    border-bottom: 0.5px solid rgba(162, 163, 164, 0.4);
    border-top-left-radius: 0.25rem;
    border-top-right-radius: 0.25rem;
    display: flex;
    align-items: center;
    position: relative;
    & div {
      width: 0.75rem;
      height: 0.75rem;
      margin-left: $spacing-closely-related;
      background: rgb(199, 199, 199);
      border: 0.025rem solid rgb(169, 169, 169);
      border-radius: 50%;
      &:hover {
        filter: brightness(0.8);
        cursor: pointer;
      }
    }
    &__button-container {
      display: flex;
      align-items: center;
      z-index: 9;
      & .close {
        background: rgb(231, 69, 70);
        border: 0.5px solid rgb(208, 67, 67);
      }

      & .min {
        background: rgb(246, 180, 39);
        border: 0.5px solid rgb(212, 154, 58);
      }

      & .max {
        background: rgb(86, 202, 53);
      }
    }
  }
  // tab name
  .page-name {
    align-self: center;
    position: absolute;
    inset: 0;
    margin-inline: auto;
    width: fit-content;
    font-family: $ff-old;

    &.is-hovered {
      @include global__heading;

      font-size: $fsz-2xs;
    }
  }

  /*===========================================
    Windows Bar
=========================================== */
  .main-container {
    @include card-border;
    transition: all 0.5s ease-in-out;
    border-radius: $br-default;

    display: grid;
    grid-template-areas:
      "winhead"
      "container"
      "footer";
    grid-template-columns: 1fr;
    grid-template-rows: auto auto 1fr auto;

    height: calc(100% - $header-height);
    width: 100%;
    position: relative;

    transform: skew(-5deg) scale(0.9);
    transition:
      transform 0.8s cubic-bezier(0.17, 0.55, 0.55, 1),
      opacity 0.6s ease;

    &.is-hovered {
      transform: skew(0deg) scale(1);
      box-shadow: $shadow-lg;
    }
    @media (min-width: $desktop-breakpoint) {
      grid-template-areas:
        "winhead winhead"
        "sidebar container"
        "sidebar footer";
      grid-template-columns: auto 1fr;
      grid-template-rows: auto auto 1fr auto;
    }
  }

  .sidebar {
    grid-area: sidebar;
    display: none;

    @media (min-width: $desktop-breakpoint) {
      // shows on breakpoint
      @include section-padding-inline;

      @include flex(column, flex-start, stretch);
      gap: $spacing-closely-related;
      inline-size: 100%;

      & h2 {
        text-wrap: nowrap;
      }

      // new ui styling
      &.is-hovered {
        padding: unset; // TODO: MAKE THIS THE SIZE OF THE ICONS THAT YOU WANT TO SHOW SO ON HOVER IT EXPANDS ETC
        overflow-x: hidden;
        inline-size: 0%;
        max-inline-size: fit-content;

        &:hover {
          @include section-padding-inline;
          inline-size: 100%;
        }
      }
    }
  }

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
    grid-area: header;
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

      margin-top: $spacing-less-related;

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
    width: 100%;
    height: 100%;

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
    // new ui styles
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
          box-shadow: $shadow-md;

          & img {
            display: inline-flex;
            object-fit: cover;
            width: 100%;
            height: 100%;
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

          font-family: $ff-regular;
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
          margin-right: $spacing-closely-related;
          &:hover {
            color: $link-color;
            filter: brightness(0.8);
            & svg {
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
            display: inline;
          }
        }

        // select second card
        &:nth-child(3) {
          @include card-styling;
          box-shadow: $shadow-lg;
          & figure {
            inline-size: 100%;
            block-size: 100%;
          }
          p {
            color: $text-primary;
            // select third and fourth paragraphs
            &:nth-child(3),
            &:nth-child(4) {
              font-size: $fsz-xs;
              line-height: 1.65;
            }
          }
        }
        // select second card
        &:nth-child(4) {
          & figure {
            inline-size: 100%;
            block-size: 100%;
          }
          p {
            color: $text-primary;
            // select third and fourth paragraphs
            &:nth-child(3),
            &:nth-child(4) {
              font-size: $fsz-xs;
              line-height: 1.65;
            }
          }
        }
      }
    }
    // select all cards
  }

  .footer {
    width: 100%;
    height: 3.25rem;
    background-color: $footer-background;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
