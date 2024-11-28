<script>
  let {
    title = $bindable(``),
    description = $bindable(``),
    imageSrc = $bindable(""),
    imageAlt = $bindable("Card Image"),
    linkHref = $bindable("#"),
    linkText = $bindable("Continue Reading"),
    linkAriaLabel = $bindable("Continue Reading Link"),
  } = $props();
</script>

<article class="card">
  <section class="card__content">
    <h2 class="card__title">{@html title}</h2>
    <!-- The slot allows for custom content to be inserted into the card. 
         If no content is provided, "Default content goes here." will be displayed. -->
    <p>{@html description}</p>
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
  </section>
  {#if imageSrc}
    <img src={imageSrc} alt={imageAlt} class="card__image" loading="lazy" />
  {/if}
</article>

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
<style lang="scss" scoped>
  @use "./src/lib/SCSS/index.scss" as *;
  *,
  *::after,
  *::before {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  $new-p-line-height: 1.65;

  $card-image-content-gap: 2rem;

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
  .is-hovered {
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
</style>
