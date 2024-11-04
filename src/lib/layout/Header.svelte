<script>
</script>

<header>
  <div class="burger">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>

  <nav>
    <a href="/">Home</a>
    <a href="/">About</a>
    <a href="/">Services</a>
    <a href="/">Contact</a>
  </nav>
</header>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  /* ===============================================
Header
=============================================== */
  header {
    z-index: 10000;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 3.25rem;
    backdrop-filter: blur(12px);

    border-bottom: 0.0625rem solid $color-border;

    & .burger {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      left: 50%;
      transform: translateY(-50%) translateX(-50%);
    }
  }
  @media (min-width: 48rem) {
    header {
      display: grid;
      grid-template-columns: repeat(3, auto);
      & .location,
      & .sub-description,
      & .description {
        display: unset;
      }
    }
  }

  /* ===============================================
Burger styling
=============================================== */
  .burger {
    will-change: transform;
    // structure
    display: grid;
    grid-template-columns: repeat(2, auto);
    grid-template-rows: repeat(2, auto);
    gap: 0.5rem;
    transition: transform 0.3s ease-in-out;
    // styling
    cursor: pointer;
    &:hover {
      transform: translateY(-50%) translateX(-50%) rotate(90deg);
    }
    // animation

    // dots
    & span {
      width: 0.25rem;
      height: 0.25rem;
      background-color: $color-primary;

      border-radius: 50%;
    }
  }

  /* ===============================================
Navigation Styling
=============================================== */
  nav {
    display: none;
  }
</style>
