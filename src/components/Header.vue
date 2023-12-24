<template>
    <header>
        <router-link to='/'>Main</router-link>
        <router-link to='/fantasy'>Fantasy</router-link>
        <router-link to='/royale'>Royale</router-link>
        <router-link to='/rpg'>RPG</router-link>
        <router-link to='/shooter'>Shooter</router-link>
        <router-link to='/strategy'>Strategy</router-link>
    </header>
</template>

<style scoped>
    header {
        display: flex;
        justify-content: space-evenly;
        padding: 20px;
        color: #aaa;
        font-size: 30px;
        background: #1f1f1f;
    }
    a {
        text-decoration: none;
        color: inherit;
        transition: .5s ease-in-out;
        position: relative;
        z-index: 0;
        padding: 30px;
    }
    a::before{
        position: absolute;
        content: " ";
        background-color: #ffeb00;
        top: 0;
        left: 50%;
        right: 50%;
        height: 100%;
        transition: .3s ease-in-out;
        z-index: -1;
    }
    a:hover{
        color: #3f3f3f;
    }
    a:hover::before{
        left: 0;
        right: 0;
    
    }

    .router-link-active{
        color: white; 
    }
</style>