<!-- here the UI is going to transform from an ui shitty one to a glass morphism aesthetic -->
<script>
  let isTransformed = false;
  let isHovered = $state(false);
</script>

<main
  onfocus={() => (isHovered = true)}
  onmouseover={() => (isHovered = true)}
  onmouseout={() => (isHovered = false)}
  onblur={() => (isHovered = false)}
  class:active={isHovered}
  class="ui-main-container"
>
  <aside class="ui__sidebar"> </aside>
  <section class="ui__container">
    <header class="ui__header">
      <h2 class="ui__header-heading">Transforming UI</h2>
      <nav class="ui__nav">
        <a href="HeroSection.svelte">Home</a>
        <a href="AboutSection.svelte">About</a>
        <a href="ServicesSection.svelte">Services</a>
      </nav>
    </header>

    <section class="ui__card-container">
      <button class="ui__button">Transform</button>

      <article class="ui__card">
        <h2 class="ui__card-heading"
          >Your presence is defined by your Website</h2
        >
        <p class="ui__card-body">
          With the growth of the internet, "1.09 billion websites are on the
          internet." It is <strong>crucial</strong> to ensure that your digital
          presence is not a needle in a haystack. Not only does it need to be
          <em>visually appealing and be viewed on all devices...</em>but also is
          essential to be<em><strong> HIGHLY </strong>optimized </em>for search
          engines to hit your target audience.</p
        >
        <a
          href="https://www.forbes.com/advisor/business/software/website-statistics/"
          target="_blank">Forbes Website Statistics</a
        >
      </article>
      <article class="ui__card">
        <h2 class="ui__card-heading">Accessibility is key</h2>
        <p class="ui__card-body">
          Did you know that only <strong
            >"3% of websites are accessible."</strong
          ></p
        >
        <a
          href="https://www.audioeye.com/post/accessibility-statistics/#:~:text=What%20we%20found%20is%20that,but%20for%20businesses%20as%20well."
          target="_blank">AudioEye Accessibility Statistics</a
        >
      </article>
    </section>
    <footer class="ui__footer">
      <p>Copyright &copy; 2024</p>
    </footer>
  </section>
</main>

<!-- TODO: JUST MAKE AN ACTIVE for new version CLASS -->

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  * {
    box-sizing: border-box;
  }

  .ui-main-container {
    position: relative;
    height: 100vh;
    width: 100%;
    display: flex;

    @include card-border;
  }

  .ui {
    $header-background: green;

    &__container {
      width: 100%;
      height: 100%;
      font-family: $ff-old;
      @include flex($direction: column, $justify: flex-start, $align: stretch);
    }

    &__header {
      //   styling
      width: 100%;
      height: $header-height;
      padding: $spacing-md;
      background-color: $header-background;
      @include flex($direction: row, $justify: space-between);
      &-heading {
      }
    }
    &__nav {
      @include flex;
      gap: $spacing-closely-related;
    }

    &__sidebar {
      display: none;
    }

    &__card-container {
      flex: 1;
      @include flex($direction: column, $justify: flex-start, $align: stretch);
      @include section-inner-gap;
      @include section-padding-inline;
      width: 100%;
      height: 100%;
    }

    &__card {
      padding: $card-padding;

      &-heading {
        margin-bottom: $spacing-semi-related;
      }
      &-body {
        margin-bottom: $spacing-less-related;
      }
    }
    // !TODO: MAKE THIS BUTTON HUGE AT THE TOP AND A COLOR TO MAKE THEM CLICK IT
    &__button {
      background: lime;
      width: fit-content;
    }
    &__footer {
      //   styling
      width: 100%;
      height: 3.25rem;
      background-color: darkgreen;
    }
  }

  @media (min-width: $desktop-breakpoint) {
    .ui {
      &__sidebar {
        display: block;
      }
    }
  }
  /*=====================================
New ui styles
======================================*/

  //   this is for the new ui styling
  .active {
  }
</style>
