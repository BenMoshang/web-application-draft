<script>
  import TestimonialCard from "../reusable-components/TestimonialCard.svelte";
  let heading = $state("Trusted by <br> local businesses".toUpperCase());
</script>

<section class="testimonials">
  <header class="testimonials__header">
    <h4 class="global__heading--sm">{@html heading}</h4>
  </header>
  <div class="marquee-wrapper">
    <div class="marquee">
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
    </div>
    <div class="marquee reverse">
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
      <TestimonialCard
        name="Jun Hong"
        position="Vice President, 1stgreenhome"
        pfpSrc="https://placehold.co/80x80"
        companySrc="https://placehold.co/60x60"
        description="I hired Modern to redesign my company's website. The process was smooth and easy. They listened to all my needs and delivered a site that exceeded my expectations."
      />
    </div>
    <div class="fade-overlay"></div>
  </div>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  $header-padding-top: clamp(60px, 0.323rem + 11.54vw, 140px);

  .testimonials {
    padding-top: $header-padding-top;
    @include flex-column-jus-center;
    @include section-heading-content-gap;
    &__header {
      @include section-padding-inline;
      text-align: center;
    }
    .marquee-wrapper {
      position: relative;
      overflow-x: hidden;
      width: 100%;

      .fade-overlay {
        content: "";
        position: absolute;
        top: 0;
        width: 5rem;
        height: 100%;
        pointer-events: none;
        z-index: 1;
        background: linear-gradient(
          to right,
          rgba(255, 255, 255, 1),
          rgba(255, 255, 255, 0)
        );
      }

      .fade-overlay::after {
        content: "";
        position: absolute;
        top: 0;
        right: 0;
        width: 3%;
        height: 100%;
        pointer-events: none;
        z-index: 1;
        background: linear-gradient(
          to left,
          rgba(255, 255, 255, 1),
          rgba(255, 255, 255, 0)
        );
      }
    }
    .marquee {
      position: relative;
      padding: 1rem;
      width: 100%;
      display: flex;
      animation: marquee 20s linear infinite;
      gap: $spacing-less-related;

      &:hover {
        animation-play-state: paused;
      }
    }
    .marquee.reverse {
      animation: marqueeReverse 30s linear infinite;
      &:hover {
        animation-play-state: paused;
      }
    }
  }
  TestimonialCard {
    flex: 0 0 auto;
  }
  @keyframes marquee {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-100%);
    }
  }
  @keyframes marqueeReverse {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(100%);
    }
  }
</style>
