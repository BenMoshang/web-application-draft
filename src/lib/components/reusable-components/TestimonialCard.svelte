<script>
  import "../../global-css/utils.css";

  export let name = "";
  export let position = "";
  export let pfpSrc = "";
  export let companySrc = "";
  export let description = "";
  name = name.toUpperCase();
</script>

<article class="card br p-base bg-white-200 border">
  <div class="card__header">
    <img src={pfpSrc} alt={name} class="card__pfp br" />
    <div class="card__title">
      <h4 class="ff-bold fw-medium fsz-sm text-800 lh-sm">{name}</h4>
      <h5 class="ff-regular fw-medium fsz-xs text-800 lh-sm">
        {position}
      </h5>
    </div>
    <img src={companySrc} alt={position} class="card__company" />
  </div>
  <p
    class="card__description ff-regular fw-medium fsz-xs text-800 lh-2xl p-base bg-white-100 border br"
  >
    "{description}"
  </p>
</article>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    display: flex;
    flex-direction: column;
    border: 0.625rem solid var(--gray-trans-md-alt);
    justify-content: between;
    width: 100%;
    max-width: 35.625rem;
    overflow: hidden;
    gap: var(--fsz-md);

    & .card__header {
      display: flex;
      gap: 1.375rem;
    }

    & .card__title {
      display: flex;
      align-self: center;
      flex-direction: column;
    }

    & .card__company {
      margin-left: auto;
    }
  }

  .border {
    border: 0.0625rem solid var(--border-trans-light);
  }
</style>
