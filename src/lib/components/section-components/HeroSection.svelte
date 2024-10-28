<script>
  let label = $state("establish your".toUpperCase());
  let title = $state("Modernized <br /> Web Presence".toUpperCase());
  let buttonText = $state("Get Started");
  let footerLocation = $state("New York, NY");

  let description = $state(`Web Development `);
  let subdescription = $state(`& Design`);
</script>

<section class="hero-section">
  <header>
    <h2 class="global__label">{label}</h2>
    <h1 class="global__display--xl">{@html title}</h1>
  </header>
  <button class="global__button--solid">{buttonText}</button>
  <footer class="hero-section__content">
    <small>
      <span>{footerLocation}</span>
    </small>
    <small>
      <span>{description}</span>
      <span>{subdescription}</span>
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
    grid-template-rows: 1fr auto auto;
    grid-template-areas: "header" "button" "footer";

    & header {
      grid-area: header;
      @include flex-column-center;
      text-align: center;
    }

    & footer {
      grid-area: footer;
      @include flex-column-center;
    }
  }
</style>
