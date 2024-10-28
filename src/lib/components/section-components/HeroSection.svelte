<script>
  let label = $state("establish your".toUpperCase());
  let title = $state("Modernized <br /> Web Presence".toUpperCase());
  let buttonText = $state("Get Started");
  let footerText = $state("Guaranteed");
</script>

<section class="hero-section">
  <header class="hero-section__header">
    <h2 class="global__label">{label}</h2>
    <h1 class="global__display--xl">{@html title}</h1>
  </header>
  <button class="global__button--solid">{buttonText}</button>
  <footer class="hero-section__content">
    <small>
      <span>{footerText}</span>
    </small>
  </footer>
</section>

<style lang="scss">
  @use "../../SCSS/index.scss" as *;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .hero-section {
    width: 100%;
    height: 90dvh;
    display: grid;
    grid-template-rows: 1fr auto;
    grid-template-areas: "header" "button" "";

    &__header {
      @include flex-column-center;
      text-align: center;
    }
  }
</style>
