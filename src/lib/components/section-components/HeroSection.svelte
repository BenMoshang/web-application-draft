<script>
  let title = $state("Modernized <br /> Web Presence");
  title = title.toUpperCase();
</script>

<section class="hero-section">
  <h1 class="global__title--xl2">{@html title}</h1>

  <button class="global__button--solid">Get Started</button>
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .hero-section {
    width: 100%;
    height: 90dvh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
