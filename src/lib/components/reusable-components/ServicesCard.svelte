<script>
  import "../../global-css/utils.css";

  export let title = "";
  export let description = "";
  export let counter = "";
  export let label = "";
  title = title.toUpperCase();
  label = label.toUpperCase();
</script>

<article class="card br p-xl bg-white-200 shadow-md">
  <div class="icon--wrapper">
    <svg
      class="card__icon"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 448 512"
      ><path
        fill="#d6d6d7"
        d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 144L48 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l144 0 0 144c0 17.7 14.3 32 32 32s32-14.3 32-32l0-144 144 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l-144 0 0-144z"
      /></svg
    >
  </div>
  <div>
    {#if counter}
      <p class="card__counter ff-bold fw-bold fsz-3xs text-800 lh-3xs">
        ({counter})
      </p>
    {/if}
    <h4 class="card__title ff-bold fw-bold fsz-lg text-black-800 lh-lg">
      {title}
      {#if label}
        <span class="label">{label}</span>{/if}
    </h4>
  </div>
  <p class="card__description ff-bold fw-medium fsz-xs text-600 lh-md">
    {description}
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
    border: 0.625rem solid var(--color-text-400);
    justify-content: center;
    width: 100%;
    overflow: hidden;
    /* max-width: 28.125rem; */

    gap: var(--fsz-md);

    & .card__counter {
      letter-spacing: 2.4px;
      line-height: 1;
      
    }

    & .card__title {
      letter-spacing: -2.3px;
margin-top: 1.125rem;
      display: flex;
      align-content: center;
      align-items: center;
      width: 100%;
      gap: var(--spacing-sm);
      letter-spacing: -0.2px;
      text-transform: capitalize;
    }
  }

  .icon--wrapper {
    margin-left: auto;
    cursor: pointer;
    --size: 2.25rem;
    --bg-size: 3.125rem;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    width: var(--bg-size);
    height: var(--bg-size);
    background: var(--color-black-500);
    border-radius: 50%;
    border: 0.0625rem solid var(--color-black-200);
    box-shadow:
      var(--shadow-sm),
      inset var(--shadow-sm);

    &:hover {
      & svg {
        transform: rotate(90deg);
      }
    }

    & svg {
      transition: transform 0.2s ease-in-out;
      width: var(--size);
      height: var(--size);
      position: relative;
    }
  }
</style>
