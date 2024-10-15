<script>
  import "../../global-css/utils.css";

  export let imageSrc = "";
  export let title = "";
  export let useCase = "";
  export let description = "";
  title = title.toUpperCase();
  useCase = useCase.toUpperCase();
</script>

<div class="card__wrapper">
  <figure class="card br p-base bg-white-200 border">
    <div class="card__image-wrapper bg-white-100 br border">
      <img
        src={imageSrc}
      alt={title}
        class="card__image"
      />
    </div>

    <figcaption class="card__content p-base bg-white-100 br border">
      <h4 class="card__title ff-bold fw-bold fsz-md text-800 lh-md">{title}</h4>
      <h5 class="card__useCase ff-bold fw-bold fsz-xs text-800 lh-xs">
        {useCase}
      </h5>
      <p class="card__description ff-regular fw-medium fsz-xs text-gray lh-2xl">
        {description}
      </p>
    </figcaption>
  </figure>
</div>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card__wrapper {
    container-type: inline-size;
  }

  .card {
    display: flex;
    border: 0.625rem solid var(--color-text-400);
    justify-content: between;
    width: fit-content;
    overflow: hidden;
    gap: var(--fsz-md);

    & .card__title {
      display: flex;
      align-content: center;
      align-items: center;
      width: 100%;
      gap: var(--spacing-sm);
      letter-spacing: -0.2px;
      text-transform: capitalize;
    }

    & .card__content {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    & .card__image-wrapper {
      align-self: start;
      flex-shrink: 0;
      padding: 0.875rem;
    }
  }

  .border {
    border: 2px solid #00000008;
  }

  .text-gray {
    color: #1d1d1fb3;
  }

  @container (max-width: 475px) {
    .card {
      flex-direction: column;
    }

    .card__image-wrapper {
      width: 100%;
    }

    .card__image {
      margin-inline: auto;
    }
  }
</style>
