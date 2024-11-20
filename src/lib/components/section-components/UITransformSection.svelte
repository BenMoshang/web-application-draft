<script>
  let isHovered = false;
</script>

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
    <h2 class="page-name">HOVER ME</h2>
  </header>
  <aside class="sidebar">
    <h2>User Menu</h2>
    <button>Dashboard</button>
    <button>Settings</button>
    <button>Logout</button>
  </aside>
  <section class="container">
    <header class="header" class:is-hovered={isHovered}>
      <h2 class="header__title" class:global__heading--sm={isHovered}>
        Your Website
      </h2>
      <nav class="nav">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
      </nav>
    </header>

    <section class="card-container">
      <article class="card">
        <h2>Your Presence is Defined by Your Website</h2>
        <p>
          With the growth of the internet, "1.09 billion websites are on the
          internet." It is <strong>crucial</strong> to ensure that your digital
          presence is not a needle in a haystack. Not only does it need to be
          <em>visually appealing and viewable on all devices...</em>
          but it is also essential to be
          <em><strong>HIGHLY</strong> optimized</em> for search engines to reach
          your target audience.
        </p>
        <p>
          A well-designed and optimized website serves as the digital storefront
          of your brand. Every click, scroll, and interaction reflects how your
          audience perceives your business. If your website is slow,
          unresponsive, or outdated, it can tarnish your reputation and drive
          potential customers away.
        </p>
        <p>
          To stand out among the billions of websites, it's vital to implement
          robust SEO strategies, maintain mobile-friendly design, and prioritize
          user experience (UX). These factors not only boost your visibility on
          search engines like Google but also build trust with your audience,
          encouraging repeat visits and conversions.
        </p>
        <p>
          Remember, your website is often the first impression a customer has of
          your business. Make it count by investing in its design, speed,
          content quality, and functionality. A strong digital presence can turn
          visitors into loyal customers and set you apart in a crowded online
          marketplace.
        </p>
        <a
          href="https://www.forbes.com/advisor/business/software/website-statistics/"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Forbes Website Statistics"
        >
          Explore more website statistics on Forbes.
        </a>
      </article>

      <article class="card">
        <h2>Accessibility is Key</h2>
        <p>
          Did you know that only <strong
            >"3% of websites are accessible."</strong
          > Being left out of the 97% is detrimental for your business. This is why
          you must prioritize web accessibility as a crucial part of your digital
          strategy. Accessibility ensures that all users, including those with disabilities,
          can interact with your website seamlessly. It not only fosters inclusivity
          but also improves your site's usability for everyone.
        </p>
        <p>
          Making your website accessible isn't just about compliance; it's a
          business opportunity. Studies show that businesses with accessible
          websites gain access to a larger audience, enhance user experience,
          and even improve SEO performance. By addressing accessibility, you're
          not just accommodating a need; you're unlocking potential.
        </p>
        <p>
          Additionally, accessibility compliance can help your business avoid
          costly lawsuits. With increasing legal regulations such as the
          Americans with Disabilities Act (ADA), ensuring your website meets
          accessibility standards is more important than ever.
        </p>
        <a
          href="https://www.audioeye.com/post/accessibility-statistics/#:~:text=What%20we%20found%20is%20that,but%20for%20businesses%20as%20well."
          target="_blank"
          rel="noopener noreferrer"
          aria-label="AudioEye Accessibility Statistics"
        >
          Learn more about the importance of accessibility with AudioEye's
          latest statistics.
        </a>
      </article>
    </section>
    <footer class="footer">
      <p>&copy; 2024 Your Company. All rights reserved.</p>
    </footer>
  </section>
</main>

<style lang="scss" scoped>
  *,
  *::after,
  *::before {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    transition: all 0.5s ease-in-out;
  }
  /*===========================================
    Old UI VARIABLES 
=========================================== */
  $header-background: red;
  $footer-background: darkred;
  /*===========================================
    NEW UI VARIABLES 
=========================================== */
  $hovered-header-background: blue;
  /*===========================================
    Windows Bar
=========================================== */
  .winhead {
    grid-area: winhead;
    width: 100%;
    height: 2.1875rem;
    background: rgb(244, 244, 244);
    border-bottom: 0.5px solid rgba(162, 163, 164, 0.4);
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    display: flex;
    align-items: center;
    position: relative;
    & div {
      width: 0.75rem;
      height: 0.75rem;
      margin-left: $spacing-closely-related;
      background: rgb(199, 199, 199);
      border: 0.5px solid rgb(169, 169, 169);
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
  .page-name {
    align-self: center;
    position: absolute;
    inset: 0;
    margin-inline: auto;
    width: fit-content;
    font-family: $ff-old;
    &.is-hovered {
      color: $hovered-header-background;
    }
  }
  .main-container {
    @include card-border;
    border-radius: $br-default;

    display: grid;
    grid-template-areas:
      "winhead"
      "header"
      "container"
      "footer";
    grid-template-columns: 1fr;
    grid-template-rows: auto auto 1fr auto;

    height: calc(80vh - $header-height);
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
        "sidebar header"
        "sidebar container"
        "sidebar footer";
      grid-template-columns: 1fr;
      grid-template-rows: auto auto 1fr auto;
    }
  }

  .sidebar {
    grid-area: sidebar;
    display: none;

    @media (min-width: $desktop-breakpoint) {
      @include section-padding-inline;
      @include flex(column, flex-start, stretch);
      gap: $spacing-closely-related;
    }
  }

  .container {
    grid-area: container;
    width: 100%;
    height: 100%;
    font-family: $ff-old;
    @include flex(column, flex-start, stretch);
  }
  /*===========================================
    header styles
=========================================== */
  .header {
    @include flex(row, space-between);
    grid-area: header;
    width: 100%;
    height: $header-height;
    padding: $spacing-md;
    background-color: $header-background;
    &.is-hovered {
      background-color: $hovered-header-background;
    }
    /* --------------------------------------------------
    header title styles
-------------------------------------------------- */
    &__title {
      /* !new ui style for heading h2 */

      &.global__heading--sm {
        font-size: $fsz-sm;
      }
    }
  }

  .nav {
    @include flex;
    gap: $spacing-closely-related;
  }

  .card-container {
    flex: 1;
    @include flex(column, flex-start, stretch);
    @include section-inner-gap;
    @include section-padding-inline;
    width: 100%;
    height: 100%;

    h1 {
      @include section-padding-inline;
      font-size: $fsz-lg;
    }
  }

  .card {
    padding: $card-padding;

    h2 {
      margin-bottom: $spacing-semi-related;
    }

    p {
      margin-bottom: $spacing-less-related;
    }

    a {
      &:hover {
        text-decoration: underline;
      }
    }
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
