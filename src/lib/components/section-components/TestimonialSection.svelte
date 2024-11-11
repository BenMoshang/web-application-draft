<script>
  import TestimonialCard from "../reusable-components/TestimonialCard.svelte";
  let heading = $state("Trusted by <br> local businesses".toUpperCase());
</script>

<section class="testimonials">
  <header class="testimonials__header">
    <h4 class="global__heading--sm">{@html heading}</h4>
  </header>
  <TestimonialCard
    name="Jun Hong"
    position="Vice President, 1stgreenhome"
    pfpSrc="https://placehold.co/80x80"
    companySrc="https://placehold.co/60x60"
    description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
  />
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  $header-padding-top: 1.875rem;
  .testimonials {
    padding-top: $header-padding-top;
    @include flex-column-jus-center;
    @include section-heading-content-gap;
    &__header {
      @include section-padding-inline;
      text-align: center;
    }
  }
</style>
