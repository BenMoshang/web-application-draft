<script>
  let phrase = $state("establish your".toUpperCase());
  let title = $state("Modernized <br /> Web Presence".toUpperCase());
  let buttonText = $state("Get Started");
  title = title.toUpperCase();
</script>

<section class="hero-section">
  <header class="hero-section__header">
    <h1>
      <span class="hero-section__phrase">{phrase}</span>
      <span class="global__display--xl">{@html title}</span>
    </h1>
  </header>
  <button class="global__button--solid">{buttonText}</button>
</section>

<style lang="scss">
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .hero-section {
    width: 100%;
    height: 90dvh;

    &__header {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      & > * {
        display: block;
      }
    }
  }
</style>
