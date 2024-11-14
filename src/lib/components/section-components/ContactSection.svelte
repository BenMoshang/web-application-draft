<script>
  let title = "Let's Build Your Next Success Story".toUpperCase();
  let body =
    "We are committed to delivering the best services to our clients, ensuring excellence in every project we undertake.";
  let buttonText = $state("Transform my brand".toUpperCase());

  const navLinks = [
    {
      name: "Facebook",
      icon: "../../static/assets/icons/social/facebook-icon.svg",
      href: "/#",
    },
    {
      name: "Instagram",
      icon: "../../static/assets/icons/social/instagram-icon.svg",
      href: "/#",
    },

    {
      name: "LinkedIn",
      icon: "../../static/assets/icons/social/linkedin-icon.svg",
      href: "/#",
    },
    {
      name: "Github",
      icon: "../../static/assets/icons/social/github-icon.svg",
      href: "/#",
    },
  ];
  navLinks.forEach((link) => {
    link.name = link.name.toUpperCase();
  });
</script>

<section class="contact">
  <header class="contact__header">
    <h2 class="contact__title global__display--lg">{@html title}</h2>
    <button
      class="contact__button global__button--solid"
      aria-label="Transform my brand - Get Started"
      tabindex="0"
    >
      <span class="button-text">{buttonText}</span>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="12"
        width="12"
        viewBox="0 0 512 512"
        aria-hidden="true"
        focusable="false"
        role="img"
      >
        <path
          fill="#ffffff"
          d="M498.1 5.6c10.1 7 15.4 19.1 13.5 31.2l-64 416c-1.5 9.7-7.4 18.2-16 23s-18.9 5.4-28 1.6L284 427.7l-68.5 74.1c-8.9 9.7-22.9 12.9-35.2 8.1S160 493.2 160 480l0-83.6c0-4 1.5-7.8 4.2-10.8L331.8 202.8c5.8-6.3 5.6-16-.4-22s-15.7-6.4-22-.7L106 360.8 17.7 316.6C7.1 311.3 .3 300.7 0 288.9s5.9-22.8 16.1-28.7l448-256c10.7-6.1 23.9-5.5 34 1.4z"
        />
      </svg>
    </button>
  </header>
  <figure class="contact__image--wrapper"></figure>
  <p class="contact__body global__body--lg">
    {@html body}
  </p>

  <nav class="contact__nav">
    {#each navLinks as link}
      <a class="contact__nav--link global__links" href={link.href}>
        <img
          src={link.icon}
          alt="{link.name} icon"
          class="contact__nav--icon"
        />
        {link.name}
      </a>
    {/each}
  </nav>
</section>

<style lang="scss">
  @use "../../SCSS/index.scss" as *;

  /*==========================================
  Variables
===========================================*/
  // Container Padding
  $main-container-inline-padding: clamp(1.25rem, -0.596rem + 6.22vw, 5rem);

  /*====================================
contact Section
===========================================*/
  .contact {
    @include flex-column-center;
    padding-inline: $main-container-inline-padding;
    gap: $section-inner-gap-lg;

    // &__header {
    // }
    &__header {
      @include flex-column-center;
      gap: $spacing-less-related;
    }
    &__title {
      text-align: center;
    }

    &__image--wrapper {
      width: 21.875rem;
      height: 37.375rem;
      border-radius: 62.5rem;
      @include parallax-section(
        "https://fakeimg.pl/1200x800/?text=Background+Image",
        800px
      );

      &:hover .contact__image {
        transform: scale(1.05);
      }
    }
    &__button {
    }
    &__image {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    &__body {
      @include paragraph-ch-inline;
      text-align: center;
    }

    &__nav {
      @include flex-center;
      gap: $spacing-less-related;

      &--link {
        @include flex-center;
        color: $text-secondary;
        gap: $spacing-most-related;
        transition: transform 0.2s ease-in-out;
        &:hover {
          transform: scale(1.05);
          text-shadow: $shadow-sm;

          & svg,
          & img {
            filter: drop-shadow($shadow-sm);

            animation: icon-float-and-replace 0.5s ease-in-out forwards;
          }
        }
      }
      &--icon {
        inline-size: $fsz-xs;
        block-size: $fsz-xs;
      }
    }
  }
</style>
