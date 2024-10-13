<script>
import '../../global-css/utils.css';

export let imageSrc = '';
export let title = '';
export let useCase = '';
export let description = '';
title = title.toUpperCase();
useCase = useCase.toUpperCase();
</script>

<figure class="card br p-xl bg-white-200 shadow-md">
    <img src={imageSrc} alt={title} class="card__image" />

    <figcaption class="card__caption">
        <h4 class="card__title  ff-bold fw-bold fsz-lg text-black-800 lh-lg">{title}</h4>
        <h5 class="caption__useCase  ff-bold fw-bold fsz-3xs  text-800 lh-3xs ">({useCase})</h5>
        <p class="card__description ff-bold fw-medium fsz-xs text-600 lh-md">{description}</p>
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
    border: 0.625rem solid var(--color-text-400);
    justify-content: center;
    width: 100%;
    height: 100%;
    overflow: hidden;
    max-width: 28.125rem;

    gap: var(--fsz-md);

    & .card__counter {

        letter-spacing: 0.15rem;
        line-height: 1;
        margin-bottom: -0.125rem;

    }

    & .card__title {

        display: flex;
        align-content: center;
        align-items: center;
        width: 100%;
        gap: var(--spacing-sm);
        letter-spacing: -0.0125em;
        text-transform: capitalize;
    }

}
</style>
