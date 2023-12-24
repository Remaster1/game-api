
<script setup>
defineProps({
    game: {
        type: Object,
        default:{
            id: 1,
            title: "Game",
            short_description: "Yea",
            release_date: "11.02.23",
            platform: "Windows",
            thumbnail : "https://img.freepik.com/free-photo/collage-with-mountains-in-city_23-2150385874.jpg?w=740&t=st=1702831724~exp=1702832324~hmac=f4a6d32738fc3a7e5fb7aa3c2ce92d4aba5101c5926fc6def5f4cd83cda55907"
        }
    }
});
</script>


<template>
    <div>
        <img :src="game.thumbnail"/>
        <h1>{{game.title}}</h1>
        <p>{{game.short_description}}</p>
        <nav>
           <i class="fas fa-desktop"></i>
           <h4>{{ game.platform }}</h4>
        </nav>
        <nav>
           <i class="far fa-clock"></i>
           <h4>{{ game.release_date }}</h4>
        </nav>
        <router-link :to="{
            name: 'detail', 
            params: {
            id: game.id
            }
        }">Подробнее</router-link>
    </div>
</template>

<style scoped>
    div{
        width: 100%;
        padding: 18px;
        display: flex;
        flex-direction: column;
        color: white;
        background-color: #2f2f2f;
        border-radius: 10px;
    }
    img{
        width: 100%;
        aspect-ratio: 16/9;
        border-radius: 5px;
    }
    h1{
        font-size: 30px;
        margin-top: 20px;
    }
    p {
        font-size: 20px;
        margin-top: 20px;
        line-height: 120%;
    }

    nav{
        display: flex;
        margin-top: 20px;
        flex-direction: row;
    }
    h4{
        font-size: 20px;
        margin-right: 10px;
    }
    a{
        background-color: #4779eb;
        font-size: 24px;
        padding: 18px 28px;
        color: white;
        margin-left: auto;
        border-radius: 5px;
        text-decoration: none;
    }
</style>