<script setup>
import { ref } from 'vue';
import { Head, Link, router } from '@inertiajs/vue3';
import ApplicationMark from '@/Components/ApplicationMark.vue';
import Banner from '@/Components/Banner.vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';
import NavLink from '@/Components/NavLink.vue';
import ResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import { TrophyIcon, TicketIcon, HomeIcon, UserGroupIcon, PuzzlePieceIcon, UserIcon } from '@heroicons/vue/24/outline'

defineProps({
    title: String,
});

const showingNavigationDropdown = ref(false);

const logout = () => {
    router.post(route('logout'));
};
</script>

<template>
    <div class="container">
        <header class="header">
            <a href="#" class="header_button">
                <TrophyIcon />
            </a>
            <a href="#" class="header_button">
                <TicketIcon />
            </a>
        </header>
        <slot></slot>
        <footer class="footer">
            <a href="#" class="footer_button active">
                <HomeIcon />
            </a>
            <a href="#" class="footer_button">
                <UserGroupIcon />
            </a>
            <a href="#" class="footer_button">
                <PuzzlePieceIcon />
            </a>
            <a href="#" class="footer_button">
                <UserIcon />
            </a>
        </footer>
    </div>
</template>
