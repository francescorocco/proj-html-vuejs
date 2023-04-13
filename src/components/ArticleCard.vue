<script>
    export default {
        name: "ArticleCard",
        
        props:{
            img: String,
            title: String,
            from: String,
        }    
    }

</script>

<template>
    <div class="card">
        <img :src=img alt="{{ title }}">
        <h3>{{ title }}</h3>
        <div class="from">{{ from }}</div>
    </div>
</template>

<style scoped lang="scss">

    h3{
        padding: 20px 20px 10px;
        font-weight: 500;
        font-size: 24px;
    }

    .from{
        padding-left: 20px;
    }

    .card{
        transition: transform 0.3s linear;
    }
    .card:hover{
        transform: scale(1.1);
    }
</style>