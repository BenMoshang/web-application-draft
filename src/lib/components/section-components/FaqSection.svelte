<script>
  import FaqCard from "../reusable-components/FaqCard.svelte";
</script>

<section class="faqs">
  <FaqCard
    question="What industries do you specialize in?"
    answer="I have experience working across various industries including but not limited to technology, healthcare, fashion, hospitality, and non-profit organizations."
  />
</section>

<style lang="scss">
  @use '../../SCSS/mixins.scss' as *;

  .faqs {
    @include flex-column-center;
  }
</style>
