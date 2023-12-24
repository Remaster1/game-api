
<script setup>
import GameCard from '@/components/GameCard.vue';
</script>
<template>
    <section>
        <h1 class="title">Fantasy</h1>
        <div class="block">
            <GameCard v-for="{item, index} in 3" :key="index"/>
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
    grid-gap: 50px;
}

</style>