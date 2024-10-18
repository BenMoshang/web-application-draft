<script>
  import ServicesCard from "../reusable-components/ServicesCard.svelte";

  let title = `OUR<br/> EXPERTISE`;

  const servicesData = [
    {
      counter: "01",
      title: "Business",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: "02",
      title: "Technology",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: "03",
      title: "Marketing",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
    {
      counter: "04",
      title: "Design",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "PRO",
    },
    {
      counter: "05",
      title: "Consulting",
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
      label: "",
    },
  ];
</script>

<section class="services pinline-lg">
  <h1 class="services__title ff-bold fw-bold fsz-2xl lh-3xs text-800">
    {@html title}
  </h1>
  <section class="services__container">
    {#each servicesData as { counter, title, description, label }}
      <ServicesCard {counter} {title} {description} {label} />
    {/each}
  </section>
</section>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  .services {
    padding-top: 1.875rem;
    display: flex;
    flex-direction: column;
    gap: var(--dynamic-3xl);

    & .services__title {
      text-transform: capitalize;

      letter-spacing: -2.3px;
    }

    & .services__container {
      display: flex;
      flex-flow: row wrap;
      gap: var(--static-sm);

      width: 100%;

      & > * {
        flex: 1;
        flex-basis: 450px;
      }
    }
  }

  /* .services {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1rem;
  padding: 1rem;
} */
</style>
