<script setup>
import { Link } from '@inertiajs/vue3';

const props = defineProps({
    href: { type: String, default: null },
});
</script>

<template>
    <Link :href="href ? route(href) : ''" :class="href ? route().current(href) ? 'btn_icon active' : 'btn_icon' : 'btn_icon'">
        <slot>
        </slot>
    </Link>
</template>

<style>


.btn_icon {
    color: var(--light-color);
}

.btn_icon.active {
    color: var(--accent-color);
}

.btn_icon > svg {
    height: 24px;
}

</style>
