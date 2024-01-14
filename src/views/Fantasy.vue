<script setup>
import GameCard from '@/components/GameCard.vue';
import * as api from '../api/api.js'
import { onMounted, ref } from 'vue';

const games = ref();
onMounted(async () => {
    games.value = await api.GamesCategory('fantasy');
    
})
</script>
<template>
    <section>
        <h1 class="title">Fantasy</h1>
        <div class="block">
            <GameCard v-for="(item, index) in games" :game="item" :key="index" />
        </div>
    </section>
    
</template>


<style scoped>
.title{
    font-size: 48px;
    text-align: center;
    margin: 28px 0;
    color: white;
}

.block{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    grid-gap: 25px;
    padding-left: 10px;
    padding-right: 10px;
}

</style>