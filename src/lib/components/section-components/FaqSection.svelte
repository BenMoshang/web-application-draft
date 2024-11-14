<script>
  import FaqCard from "../reusable-components/FaqCard.svelte";

  const faqCards = [
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
    {
      question: "What industries do you specialize in?",
      answer:
        "I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations.",
    },
  ];
</script>

<section class="faqs">
  {#each faqCards as faqCard}
    <FaqCard question={faqCard.question} answer={faqCard.answer} />
  {/each}
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;
  .faqs {
    @include flex-column-center;
    gap: 1.5rem;
  }
</style>
