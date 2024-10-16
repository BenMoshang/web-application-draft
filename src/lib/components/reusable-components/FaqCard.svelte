<script>
  import "../../global-css/utils.css";
  import { slide } from "svelte/transition";

  export let question = "";
  export let answer = "";
  question = question.toUpperCase();

  let isOpen = false;

  function toggle() {
    isOpen = !isOpen;
  }
</script>

<section class="card bg-white-100 br p-base border-gray" on:click={toggle}>
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
    <section class="card__content" in:slide={{ duration: 200 }}>
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
  }

  .card {
    display: flex;
    flex-direction: column;
    overflow: hidden;

    & .card__header {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &:hover {
      background-color: hsl(0, 0%, 95%);
    }
  }

  .card:has(input:checked) {
    background-color: #fafafa;
  }

  img.open {
    transform: rotate(45deg) scale(1.1);
    filter: brightness(0);
  }

  .card__content {
    overflow: hidden;
  }
  hr {
    border: none;
    height: 1px;
    width: 100%;
    margin-block: 0.5rem 0.8rem;
    background-color: var(--color-black-100);
  }
  .open {
    transform: rotate(180deg);
    transition: transform 0.3s ease-out;
  }
</style>
