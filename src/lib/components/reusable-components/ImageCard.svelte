<script>
  import "../../global-css/utils.css";

  export let title = "";
  export let description = "";
  export let imageSrc = "";
  export let label = "";
  title = title.toUpperCase();
  label = label.toUpperCase();

  let isHovered = false;
</script>

<figure class="card shadow-md br bg-white-200 border-black-100">
  {#if imageSrc}
    <img
      on:focus={() => (isHovered = true)}
      on:mouseover={() => (isHovered = true)}
      on:mouseout={() => (isHovered = false)}
      on:blur={() => (isHovered = false)}
      src={imageSrc}
      alt={title}
      class="card__image"
    />
  {/if}
  <figcaption class="card__content pblock-base pinline-lg bg-white-200">
    <header class="content__header">
      <h4 class="header__title global__card-title--sm">{title}</h4>

      <p class="header__description global__description--xs">
        {description}
      </p>
    </header>
    {#if label}
      <div class="header__label">
        <p class="label__text" class:active={isHovered}>{label}</p>
      </div>
    {/if}
  </figcaption>
</figure>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100%;
    overflow: hidden;

    & .card__image {
      width: 100%;
      height: 100%;
      object-fit: cover;

      transition: transform 0.25s ease-in-out;
      isolation: isolate;
      z-index: var(--z-1);
      cursor: pointer;
      &:hover {
        transform: scale(1.1);
      }
    }
  }

  .header__label {
    background-color: var(--color-black-0);
    border: 0.0625rem solid var(--border-black-100);
    border-radius: var(--rounded-border-radius);
    padding-block: 0.625rem;
    padding-inline: 1.25rem;
    box-shadow: inset var(--shadow-sm);
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;

    & .label__text {
      will-change: transform;
      display: flex;
      letter-spacing: 0.05em;
      text-transform: capitalize;
      font-family: var(--ff-bold);
      font-size: var(--fsz-3xs);
      font-weight: var(--fw-semibold);
      line-height: var(--lh-xs);
      color: var(--text-black-900);
      position: relative;
    }
  }
  .active {
    animation: moveUp 0.3s ease-in-out forwards;

    &::after {
      content: "2024";
      position: absolute;
      inset: 0;
      margin: auto;
      width: 100%;
      height: 100%;
      transform: translateY(200%);
      background-color: var(--color-black-0);
      animation: replaceAfter 0.3s ease-in-out;
      animation-delay: 0.3s;
      z-index: var(--z-2);
    }
  }

  @keyframes moveUp {
    0% {
      transform: translateY(0);
    }
    100% {
      transform: translateY(-200%);
    }
  }

  @keyframes replaceAfter {
    0% {
      transform: translateY(200%);
    }
    100% {
      transform: translateY(0);
    }
  }

  .card__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    padding: 1.625rem;
    width: 100%;
    flex-wrap: nowrap;
    border-color: #0000000a;
    border-style: solid;
    border-top-width: 0.0625rem;
    z-index: var(--z-2);
  }

  .content__header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 0.375rem;

    & .header__title {
      text-transform: capitalize;
    }
  }
</style>
