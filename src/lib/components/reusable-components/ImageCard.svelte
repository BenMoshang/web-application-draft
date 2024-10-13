<script>
import '../../global-css/utils.css';

export let title = '';
export let description = '';
export let imageSrc = '';
export let label = '';
title = title.toUpperCase();
label = label.toUpperCase();
</script>

<figure class="card shadow-md br bg-white-200 border-black-100">
    {#if imageSrc}
    <img src={imageSrc} alt={title} class="card__image" />
    {/if}
    <figcaption class="card__content pblock-base pinline-lg  bg-white-200 ">
        <header class="content__header">
            <h4
                class="header__title  ff-bold fw-semibold fsz-sm text-200 lh-xl">{title}</h4>
            <p class="header__description ff-bold fw-medium fsz-xs text-600 lh-2xs">{description}</p>
        </header>
        {#if label}
        <p  class="label">{label}</p>
        {/if}
    </figcaption>
</figure>

<style>
*,
*::before,
*::after {
    box-sizing: border-box;

}

.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: auto;
    overflow: hidden;
    max-width: 28.125rem;

    & .card__image {

        width: 100%;
        height: 100%;
        object-fit: fill;

        transition: transform 0.3s ease-in-out;
        isolation: isolate;
        z-index: var(--z-1);

        &:hover {
            transform: scale(1.1);
        }
    }
}

.card__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;

    width: 100%;

    flex-wrap: nowrap;
    border-color: #0000000a;
    border-style: solid;
    border-top-width: 1px;
    z-index: var(--z-2);

}

.content__header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: var(--space-xs);

}

.header__title {
    text-transform: capitalize;
}
</style>
