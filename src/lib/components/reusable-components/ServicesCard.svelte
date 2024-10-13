<script>
import '../../global-css/utils.css';

export let title = '';
export let description = '';
export let counter = '';
export let label = '';
title = title.toUpperCase();
label = label.toUpperCase();
</script>

<article class="card shadow-md br bg-text-200">
    <i class="fa-solid fa-xmark"></i>

    {#if counter}
    <p class="card__counter ">{counter}</p>
    {/if}
    <h4 class="header__title  ff-bold fw-semibold fsz-sm text-900 lh-2xl">{title}
    {#if label} <span  class="label">{label}</span>{/if}
    </h4>
    <p class="header__description ff-bold fw-medium fsz-xs text-700 lh-xs">{description}</p>
</article>

<style>
*,
*::before,
*::after {
    box-sizing: border-box;

}

.card {
    display: flex;
    flex-direction: column;
    border: 0.625rem solid var(--color-text-0);
    justify-content: center;
    width: 100%;
    height: 100%;
    overflow: hidden;
    max-width: 28.125rem;
    background-color: hsl(240, 11%, 96%);
    border-color: hsla(0, 0%, 0%, 0.04);

}

.card__counter{




}



.header__title {

    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;

    width: 100%;
    border-style: solid;
    border-top-width: 1px;
    text-transform: capitalize;
}
</style>
