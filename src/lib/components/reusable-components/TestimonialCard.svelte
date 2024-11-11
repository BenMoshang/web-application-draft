<script>
  /**
   * @typedef {Object} Props
   * @property {string} [name]
   * @property {string} [position]
   * @property {string} [pfpSrc]
   * @property {string} [companySrc]
   * @property {string} [description]
   */

  /** @type {Props} */
  let {
    name = $bindable(""),
    position = "",
    pfpSrc = "",
    companySrc = "",
    description = "",
  } = $props();
  name = name.toUpperCase();
</script>

<article class="card">
  <header class="card__header">
    <img src={pfpSrc} alt={name} class="card__pfp" />
    <div class="card__title">
      <h4 class="ff-bold fw-medium fsz-sm text-800 lh-sm">{name}</h4>
      <h5 class="ff-regular fw-medium fsz-xs text-800 lh-sm">
        {position}
      </h5>
    </div>
    <img src={companySrc} alt={position} class="card__company" />
  </header>
  <p
    class="card__description ff-regular fw-medium fsz-xs text-800 lh-2xl p-base bg-white-100 border br"
  >
    "{description}"
  </p>
</article>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    @include flex-column-jus-center;
    @include card-styling;
    min-width: 17.5rem; //for mobile responsiveness

    max-height: 18.375rem;
    height: 100%;
    width: 100%;

    &__ & .card__title {
      display: flex;
      align-self: center;
      flex-direction: column;
    }

    & .card__company {
      margin-left: auto;
    }
  }
</style>
