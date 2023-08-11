<script setup>
import { ref } from 'vue';
import { Head, Link, router } from '@inertiajs/vue3';
import { TrophyIcon, TicketIcon, HomeIcon, UserGroupIcon, PuzzlePieceIcon, UserIcon } from '@heroicons/vue/24/outline'
import RoundButton from "@/Components/RoundButton.vue";
import IconButton from "@/Components/IconButton.vue";

defineProps({
    title: String,
});

const logout = () => {
    router.post(route('logout'));
};
</script>

<template>
    <div class="container">
        <header class="header">
            <RoundButton href="">
                <TrophyIcon />
            </RoundButton>
            <RoundButton href="">
                <TicketIcon />
            </RoundButton>
        </header>
        <slot></slot>
        <footer class="footer">
            <IconButton href="home">
                <HomeIcon />
            </IconButton>
            <IconButton href="">
                <UserGroupIcon />
            </IconButton>
            <IconButton href="">
                <PuzzlePieceIcon />
            </IconButton>
            <IconButton href="">
                <UserIcon />
            </IconButton>
        </footer>
    </div>
</template>

<style>
.container {
    display: flex;
    flex-direction: column;
    max-width: 425px;
    min-height: 100vh;
    margin: 0 auto;
    background-color: var(--main-bg-color);
}

.header {
    display: flex;
    justify-content: space-between;
    padding: 32px;
}

.footer {
    display: flex;
    justify-content: space-between;
    border-radius: 18px;
    position: sticky;
    bottom: 32px;
    width: calc(100% - 64px);
    margin: auto 32px 0;
    padding: 20px 32px;
    background-color: var(--secondary-color);
}
</style>
