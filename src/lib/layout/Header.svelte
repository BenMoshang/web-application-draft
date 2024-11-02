<script>
  let location = $state("Baltimore, MD".toUpperCase());
  let description = $state(`Web Development`.toUpperCase());
  let subdescription = $state(`& Design`.toUpperCase());
</script>

<header>
  <small class="location-wrapper">
    <span class="location global__label">{location}</span>
  </small>
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
  <small class="description-wrapper">
    <span class="description global__label">{description}</span>
    <span class="sub-description global__label">{subdescription}</span>
  </small>
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
    /* ----------------------------------------
    Location, Sub-description, Description styling
    ---------------------------------------- */
    & .location,
    & .sub-description,
    & .description {
      display: none; //turns on in tablet and desktop
      font-weight: $fw-medium;
      font-size: $fsz-3xs;
    }

    & .location,
    & .description {
      color: $color-tertiary;
    }

    & .sub-description {
      color: $color-quaternary;
    }
    /* ----------------------------------------
   Positioning
    ---------------------------------------- */
    & .description-wrapper,
    & .burger,
    & .location-wrapper {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
    }
    & .burger {
      left: 50%;
      transform: translateY(-50%) translateX(-50%);
    }

    & .description-wrapper {
      right: $spacing-xs;
    }

    & .location-wrapper {
      left: $spacing-xs;
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
