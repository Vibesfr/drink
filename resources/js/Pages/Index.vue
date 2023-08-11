<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
</script>

<template>
    <AppLayout>
        <section class="profile">
            <img :src="$page.props.auth.user.profile_photo_url" alt="profile picture" class="profile_image">
            <div class="profile_text">
                <h3 class="profile_name">{{ $page.props.auth.user.name }}</h3>
                <div class="profile_badges">
                    <span class="badge" style="background-color: #FCE588; color: #8D2B0B">Golden drinker</span>
                    <span class="badge">2586 Gorgées</span>
                </div>
            </div>
        </section>

        <section class="most_played_game">
            <h3 class="section_title">Jeux les plus joués</h3>
            <div class="games_list">
                <div class="game">
                    <p class="game_name">Blitz Battle</p>
                    <div class="game_count">56 Parties</div>
                </div>
                <div class="game">
                    <p class="game_name">Blitz Battle</p>
                    <div class="game_count">56 Parties</div>
                </div>
                <div class="game">
                    <p class="game_name">Blitz Battle</p>
                    <div class="game_count">56 Parties</div>
                </div>
                <div class="game">
                    <p class="game_name">Blitz Battle</p>
                    <div class="game_count">56 Parties</div>
                </div>
                <div class="game">
                    <p class="game_name">Blitz Battle</p>
                    <div class="game_count">56 Parties</div>
                </div>
            </div>
        </section>

        <section class="quick_game_section">
            <h3 class="section_title">Parties Rapides</h3>
            <div class="quick_games_list">
                <div class="quick_game">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU" alt="" class="game_image">
                    <p class="game_name">Blitz Battle</p>
                </div>
                <div class="quick_game">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU" alt="" class="game_image">
                    <p class="game_name">Blitz Battle</p>
                </div>
                <div class="quick_game">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU" alt="" class="game_image">
                    <p class="game_name">Blitz Battle</p>
                </div>
                <div class="quick_game">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU" alt="" class="game_image">
                    <p class="game_name">Blitz Battle</p>
                </div>
                <div class="quick_game">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU" alt="" class="game_image">
                    <p class="game_name">Blitz Battle</p>
                </div>
            </div>
        </section>
    </AppLayout>
</template>

<style>
.profile {
    display: flex;
    justify-content: center;
    background-color: var(--secondary-color);
    border-radius: 18px;
    margin: 0 32px;
    padding: 18px 0;
}

.profile_image {
    height: 64px;
    border-radius: 50%;
    margin-right: 24px;
}

.profile_text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-family: 'Jost', sans-serif;
    font-weight: bold;
    font-size: 16px;
    color: var(--light-color);
    text-transform: capitalize;
}

.profile_badges {
    display: flex;
    margin-top: 4px;
    gap: 4px;
}

.badge {
    display: block;
    font-size: 9px;
    font-weight: bold;
    padding: 4px 9px;
    border-radius: 4px;
    background-color: #E4E7EB;
    color: #1F2933;
}

.most_played_game {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: var(--secondary-color);
    border-radius: 18px;
    margin: 18px 32px 0;
    padding: 18px;
    color: var(--light-color);
}

.section_title {
    font-size: 16px;
    font-weight: bold;
    color: var(--light-color);
}

.games_list {
    display: flex;
    overflow-x: auto;
    gap: 12px;
    margin-top: 12px;
}

.games_list::-webkit-scrollbar {
    display: none;
}

.game {
    display: flex;
    flex: 0 0 auto;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    height: 64px;
    width: 64px;
    background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBe5oKl-_iLejmm5uQv6y8MYeba7MIAcLuog&usqp=CAU");
    background-size: cover;
    border-radius: 12px;
}

.game_name {
    font-size: 10px;
    font-weight: bold;
}

.game_count {
    font-size: 8px;
    margin-top: 4px;
}

.quick_game_section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-radius: 18px;
    margin: 18px 32px 0;
    color: var(--light-color);
}

.quick_games_list {
    display: flex;
    overflow-x: auto;
    gap: 12px;
    margin-top: 12px;
}

.quick_games_list::-webkit-scrollbar {
    display: none;
}

.quick_game {
    display: flex;
    flex: 0 0 auto;
    flex-direction: column;
    justify-content: center;
    text-align: center;
}

.game_image {
    height: 64px;
    width: 64px;
    border-radius: 12px;
    margin-bottom: 8px;
}
</style>
