<script>
  import "../../global-css/utils.css";
  import { slide, fade } from "svelte/transition";

  export let question = "";
  export let answer = "";
  question = question.toUpperCase();

  let isOpen = false;

  function toggle() {
    isOpen = !isOpen;
  }

  function slideFade(node, { duration }) {
    return {
      duration,
      css: (t) => {
        const slideStyle = slide(node, { duration }).css(t);
        const fadeStyle = fade(node, { duration }).css(t);
        return `${slideStyle} ${fadeStyle}`;
      },
    };
  }
</script>

<section
  class="card bg-white-100 br p-base border-gray"
  on:click={toggle}
  class:open={isOpen}
>
  <section class="card__header">
    <h2 class="question global__paragraph--xsb">{question}</h2>
    <img
      src="/chevron-arrow.svg"
      alt="Chevron Arrow"
      width="48"
      height="48"
      class:open={isOpen}
    />
  </section>

  {#if isOpen}
    <section class="card__content" transition:slideFade={{ duration: 150 }}>
      <hr />
      <p class="global__paragraph--xs">{answer}</p>
    </section>
  {/if}
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
    transition: all 0.3s ease-out;
  }

  .card {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 75rem;
    user-select: none;
    overflow: hidden;

    & .card__header {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &:hover {
      background-color: hsl(0, 0%, 92.5%);
    }
  }

  .card.open {
    background-color: #fafafa;
  }

  img.open {
    transform: rotate(45deg) scale(1.1);
    filter: brightness(0);
  }

  .card__content {
    text-align: left;
    overflow: hidden;
  }

  hr {
    border: none;
    height: 1px;
    width: 100%;
    margin-block: 0.5rem 0.8rem;
    background-color: var(--color-black-100);
  }
</style>
