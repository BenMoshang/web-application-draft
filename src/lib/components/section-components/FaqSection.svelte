<script>
  import FaqCard from "../reusable-components/FaqCard.svelte";
</script>

<section class="faqs">
  <FaqCard
    question="What industries do you specialize in?"
    answer="I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations."
  />
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  .faqs {
    display: flex;
    flex-direction: column;
    gap: var(--static-sm);
  }
</style>
