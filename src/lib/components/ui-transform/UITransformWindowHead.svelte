<script>
  let title = "Hover Me";
  let isHovered = true;
</script>

<header class="winhead">
  <section class="winhead__button-container">
    <div class="close"></div>
    <div class="min"></div>
    <div class="max"></div>
  </section>
  <h2 class:is-hovered={isHovered} class="page-name">HOVER ME</h2>
</header>

<style lang="scss" scoped>
  @use "./src/lib/SCSS/index.scss" as *;
  .winhead {
    width: 100%;
    height: 2.25rem;
    background: rgb(244, 244, 244);
    border-bottom: 0.5px solid rgba(162, 163, 164, 0.4);
    border-top-left-radius: 0.25rem;
    border-top-right-radius: 0.25rem;
    display: flex;
    align-items: center;
    position: relative;
    & div {
      width: 0.75rem;
      height: 0.75rem;
      margin-left: $spacing-closely-related;
      background: rgb(199, 199, 199);
      border: 0.025rem solid rgb(169, 169, 169);
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
  // tab name
  .page-name {
    align-self: center;
    position: absolute;
    inset: 0;
    margin-inline: auto;
    width: fit-content;
    font-family: $ff-old;

    &.is-hovered {
      @include global__heading;

      font-size: $fsz-2xs;
    }
  }
</style>
