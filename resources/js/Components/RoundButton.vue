<script setup>
import { Link } from '@inertiajs/vue3';

const props = defineProps({
    href: { type: String, default: null },
});
</script>

<template>
    <Link :href="href ? route(href) : ''" class="btn_rounded">
        <slot></slot>
    </Link>
</template>

<style>
.btn_rounded {
    padding: 14px;
    border-radius: 50%;
    background-color: var(--secondary-color);
}

.btn_rounded > svg {
    height: 24px;
    color: var(--light-color);
}
</style>
