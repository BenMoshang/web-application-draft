<script>
  import ServicesCard from "../reusable-components/ServicesCard.svelte";

  let title = `OUR<br/> EXPERTISE`;

  const servicesData = [
    {
      counter: " 01 ",
      title: "Business",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: " 02 ",
      title: "Technology",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: " 03 ",
      title: "Marketing",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: " 04 ",
      title: "Design",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "PRO",
    },
    {
      counter: " 05 ",
      title: "Consulting",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
  ];
</script>

<!-- TODO: MAYBE FIND A WAY TO INCORPORATE THE GRADIENT TEXT INTO THE HEADING -->
<section class="services-section">
  <h3 class="global__display--lg services-section__heading">
    {@html title}
  </h3>
  <section class="services-section__container">
    {#each servicesData as { counter, title, description, label }}
      <ServicesCard {counter} {title} {description} {label} />
    {/each}
  </section>
</section>

<style lang="scss">
  @use "./src/lib/SCSS/index.scss" as *;
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  /* ===============================================
 Section Component Styles
=============================================== */
  $header-padding-top: 1.875rem;
  .services-section {
    padding-top: $header-padding-top;

    @include section-padding-inline;
    @include flex-column-jus-center;
    @include section-heading-content-gap;

    &__container {
      @include section-inner-gap;
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      width: 100%;
      height: 80%;
    }
  }
</style>
