<script>
  import "../../global-css/utils.css";

  export let question = "";
  export let answer = "";
  question = question.toUpperCase();
</script>

<label class="card bg-white-100 br p-base border-gray">
  <input type="checkbox" name="tab" id={question} />

  <section class="card__header" for={question}>
    <h2 class="question global__paragraph--xsb">{question}</h2>
    <img src="/chevron-arrow.svg" alt="Chevron Arrow" width="48" height="48" />
  </section>

  <section class="card__content">
    <hr />
    <p class="global__paragraph--xs">{answer}</p>
  </section>
</label>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .card {
    display: flex;
    flex-direction: column;
    user-select: none;
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

  .card:has(input:checked) .card__content {
    max-height: 50rem;
  }

  .card:has(input:checked) {
    background-color: #fafafa;
  }

  .card:has(input:checked) .card__header img {
    transform: rotate(45deg) scale(1.1);
    filter: brightness(0);
    stroke-width: 2px;
  }

  .card__content {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease-out;
  }

  label {
    display: flex;
    justify-content: space-between;
    cursor: pointer;
  }

  input {
    position: absolute;
    opacity: 0;
    z-index: -1;
  }

  hr {
    border: none;
    height: 1px;
    width: 100%;
    margin-block: 1rem 1.5rem;
    background-color: var(--color-black-100);
  }

  img {
    transition: all 0.3s ease-out;
  }
</style>
