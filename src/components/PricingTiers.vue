<template>
    <div class="pricing-plans">
        <div class="tier | padding-36">
            <h2 class="tier__title | fw-bold clr-primary-400">Free</h2>
            <ul class="tier__feature-list">
                <li class="tier__list-item">1 domain</li>
                <li class="tier__list-item">5GB of bandwidth</li>
                <li class="tier__list-item">1GB of diskspace</li>
                <li class="tier__list-item">5,000 monthly uniques</li>
            </ul>
            <p class="tier__price | fs-800 fw-bold">
                $0<span class="fs-600 fw-regular">/mo</span>
            </p>
            <ThemeButton>Get started</ThemeButton>
        </div>
        <div class="tier | padding-36 bg-primary-400 clr-neutral-100">
            <h2 class="tier__title | fw-bold clr-neutral-100">Tiny</h2>
            <ul class="tier__feature-list">
                <li class="tier__list-item">5 domain</li>
                <li class="tier__list-item">250GB of bandwidth</li>
                <li class="tier__list-item">5GB of diskspace</li>
                <li class="tier__list-item">15,000 monthly uniques</li>
            </ul>
            <p class="tier__price | fs-800 fw-bold">
                $19<span class="fs-600 fw-regular">/mo</span>
            </p>
            <ThemeButton inverted>Get started</ThemeButton>
        </div>
        <div class="tier | padding-36">
            <h2 class="tier__title | fw-bold clr-primary-400">Large</h2>
            <ul class="tier__feature-list">
                <li class="tier__list-item">15 domain</li>
                <li class="tier__list-item">750GB of bandwidth</li>
                <li class="tier__list-item">20GB of diskspace</li>
                <li class="tier__list-item">50,000 monthly uniques</li>
            </ul>
            <p class="tier__price | fs-800 fw-bold">
                $49<span class="fs-600 fw-regular">/mo</span>
            </p>
            <ThemeButton>Get started</ThemeButton>
        </div>
    </div>
</template>

<script setup>
import ThemeButton from './ThemeButton.vue';
</script>

<style lang="scss" scoped>
@use "../sass/abstracts" as *;

.pricing-plans {
    border: size(8) solid clr(primary, 400);
    display: flex;
}

.tier {
    flex: 1;

    display: grid;
    gap: size(20);

    &__title {
        text-transform: uppercase;
    }

    &__feature-list {
        list-style: none;
    }

    &__list-item {
        &:not(:last-child)::after {
            content: "";
            display: block;
            height: 1px;
            margin-block: size(20);
            background-color: clr(neutral, 900);
            opacity: 0.2;
        }
    }
}
</style>