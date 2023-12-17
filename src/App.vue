<script setup>
import Header from './components/Header.vue'
import GameCard from './components/GameCard.vue'
import { RouterView } from 'vue-router';
</script>

<template>

 
 <div class="app">
    <GameCard/>
    <RouterView></RouterView>
 </div>
</template>

<style scoped>
    .app{
        width: 100%;
        min-height: 100vh;
        background-color: #1f1f1f;
    }
</style>
