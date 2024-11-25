<script>
  let companyName = "Moshang";
  let isHovered = true;
</script>

<footer class:is-hovered={isHovered} class="footer">
  <div class="footer__shape">
    <svg
      data-name="Layer 1"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 1200 120"
      preserveAspectRatio="none"
    >
      <path
        d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
        class="shape-fill"
      ></path>
    </svg>
  </div>
  <p class="footer__initial-text">
    &copy; 2024 {companyName}. All rights reserved.
  </p>
  <section class="footer__container">
    <h4 class="footer__company-name">{companyName}</h4>
    <p class="footer__location">Baltimore, MD</p>
    <p class="footer__copyright">
      &copy; 2024 {companyName}. All rights reserved.
    </p>
  </section>
  <ul class="footer__container">
    <li class="container__column-title">Contact</li>
    <li class="container__item"
      ><a href="tel:410-929-4158" class="phone-number">410-929-4158</a></li
    >
    <li class="container__item"
      ><a href="mailto:moshangllc@gmail.com" class="email"
        >moshangllc@gmail.com</a
      ></li
    >
  </ul>
  <ul class="footer__container">
    <li class="container__column-title">Read More</li>
    <li class="container__item">
      <a
        href="https://www.forbes.com/advisor/business/software/website-statistics/"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="Forbes Website Statistics"
      >
        Forbes Statistics
      </a></li
    >
    <li class="container__item">
      <a
        href="https://www.audioeye.com/post/accessibility-statistics/#:~:text=What%20we%20found%20is%20that,but%20for%20businesses%20as%20well."
        target="_blank"
        rel="noopener noreferrer"
        aria-label="AudioEye Accessibility Statistics"
      >
        Accessibility Statistics
      </a></li
    >
  </ul>
</footer>

<style lang="scss" module>
  @use "./src/lib/SCSS/index.scss" as *;
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
  $footer-background: darkred;
  $hovered-footer-background: #0c2461;
  $my-modern-icon: url("../../../static/assets/icons/page/our-logo-icon.png");

  .footer {
    @include flex-center;
    width: 100%;
    min-height: 3.25rem;
    background-color: $footer-background;

    &__shape {
      display: none;
    }
    &__container {
      display: none;
    }

    /*--------------------------
    new footer styles
-------------------------- */
    &.is-hovered {
      @include flex(row, flex-start, stretch);
      $wave-height: 3rem;
      $border-radius: $br-default;
      $z-index: 1;
      $column-title-font-size: $fsz-sm;
      $title-margin-bottom: $spacing-closely-related;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: stretch;
      position: relative;
      padding: $card-padding;
      min-height: 11.25rem;
      background-color: $hovered-footer-background;
      border-bottom-left-radius: $border-radius;
      border-bottom-right-radius: $border-radius;

      & > * {
        flex: 1;
      }
      & .footer__initial-text {
        display: none;
      }
      /*------wavy border------*/
      & .footer__shape {
        display: block;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
        background: $hovered-footer-background;
        z-index: $z-index;

        & svg {
          width: 100%;
          height: $wave-height;
          & path {
            fill: white; //fills upper border to match page
          }
        }
      }

      /*------containers------*/

      & .footer__container {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: flex-start;
        z-index: $z-index;
        gap: $spacing-closely-related;
        width: 100%;
        height: 100%;
        padding-top: $wave-height;
        & > * {
          flex: 1;
        }
        & .footer__company-name {
          grid-area: header;
          @include global__heading;
          @include flex-center;
          $title-font-size: $fsz-md;
          position: relative;
          font-size: $title-font-size;
          color: $text-white-primary;

          margin-bottom: $title-margin-bottom;

          &::before {
            content: "";
            display: inline-flex;
            margin-right: $spacing-closely-related;
            inline-size: $title-font-size;
            block-size: $title-font-size;
            line-height: inherit;
            background: $my-modern-icon center/contain no-repeat;
          }
        }
        & .footer__location {
          @include global__body;
          font-size: $fsz-3xs;
          color: $text-white-tertiary;
        }
        & .footer__copyright {
          grid-area: content;
          @include global__body;
          font-size: $fsz-4xs;
          color: $text-white-tertiary;
          text-wrap: balance;
          font-weight: $fw-regular;
        }
      }

      /*------footer lists------*/
      & .container__column-title {
        @include global__heading;
        font-size: $column-title-font-size;
        color: $text-white-secondary;
        margin-bottom: $title-margin-bottom;
      }
      & a {
        @include global__links;
        $link-font-size: $fsz-3xs;
        font-size: $link-font-size;
        text-underline-offset: 0.125rem; //lowers underline
        color: $text-white-tertiary;
        font-weight: $fw-regular;
      }
    }
  }
</style>
