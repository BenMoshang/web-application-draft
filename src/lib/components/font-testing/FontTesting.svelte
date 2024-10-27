<script>
</script>

<div class="font-testing">
  <h1 class="global__display--xl">DISPLAY XL</h1>
  <h2 class="global__display--lg">DISPLAY LG</h2>

  <h3 class="global__heading--md">HEADING MD</h3>
  <h4 class="global__heading--sm">HEADING SM</h4>

  <p class="global__body--lg">BODY LG</p>
  <p class="global__body--md">BODY MD</p>
  <p class="global__body--sm">BODY SM</p>

  <h5 class="global__card-heading--lg">CARD HEADING LG</h5>
  <h5 class="global__card-heading--md">CARD HEADING MD</h5>
  <h5 class="global__card-heading--sm">CARD HEADING SM</h5>

  <h6 class="global__card-subheading">CARD SUBHEADING</h6>

  <p class="global__card-body">CARD BODY</p>
  <p class="global__card-label">CARD LABEL</p>
  <p class="global__card-label--bg">2024</p>
</div>

<style lang="scss">
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .font-testing {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;

    & > * {
      border: 1px solid red;
      margin: 0;
    }
  }
</style>
