<script>
  // @ts-nocheck
  import { fade, slide } from "svelte/transition";
  let { question, answer } = $props();
  let isOpen = $state(false);
</script>

<button class="card" onclick={() => (isOpen = !isOpen)} class:open={isOpen}>
  <section class="card__header">
    <h2 class="card__question">{question.toUpperCase()}</h2>
    <img
      src="/chevron-arrow.svg"
      alt="Chevron Arrow"
      width="48"
      height="48"
      class:open={isOpen}
    />
  </section>

  {#if isOpen}
    <span transition:fade={{ duration: 200 }}>
      <section class="card__content" transition:slide={{ duration: 300 }}>
        <hr />
        <p class="card__answer">{answer}</p>
      </section>
    </span>
  {/if}
</button>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;

  $transition-speed: 0.3s;
  $border-color: #cececf;
  $background-color: #f5f5f5;
  $background-color-dark: #e8e8e8;
  $text-size: clamp(1rem, 0.877rem + 0.41vw, 1.25rem);
  $answer-color: #1d1d1fb3;
  $question-color: #1d1d1ff5;
  * {
    transition: $transition-speed ease-out;
  }

  .card {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 75rem;
    border: 1px solid $border-color;
    padding: 0rem 1.5rem;
    border-radius: 1rem;
    user-select: none;

    &__header {
      @include flex-center-between;
      width: 100%;
    }

    &__content {
      width: 100%;
      overflow: hidden;
    }

    &__question {
      @include global__card-heading;
      color: $question-color;
      font-size: $text-size;
    }

    &__answer {
      @include global__body;
      color: $answer-color;
      font-size: $text-size;
      text-align: left;
    }

    &:hover {
      background-color: $background-color-dark;
    }

    img.open {
      transform: rotate(45deg) scale(1.1);
      filter: brightness(0);
    }

    &.open {
      background-color: $background-color;
    }

    hr {
      border: none;
      height: 1px;
      width: 100%;
      margin-top: 0.25rem;
      background-color: $border-color;
    }
  }
</style>
