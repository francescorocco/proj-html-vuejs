<script>
    export default {
        name: "CardBlueBorder",

        props:{
            icon: String,
            title: String,
            subtitle: String,
            text: String,
            link: String,
        }
    }
</script>

<template>
    <div class="card">
        <div class="icon"><i class="fa-solid" :class="icon"></i></div>
        <h2 class="title">{{ title }}</h2>
        <h3 class="subtitle">{{ subtitle }}</h3>
        <div class="text">{{ text }}</div>
        <a href="#" class="link">{{ link }}<i class="fa-solid fa-chevron-right"></i></a>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    .card{
        text-align: center;
        color: var(--light-text-color);
        border: 5px solid var(--card-border);
        padding: 60px;
        padding-bottom: 70px;
        border-radius: 5px;
    }

    .icon{
        font-size: 60px;
        padding-bottom: 20px;
    }

    .title{
        padding-bottom: 10px;
        font-weight: 500;
    }

    .subtitle{
        color: var(--underline-color);
        font-size: 22px;
        font-weight: 500;
        padding-bottom: 50px;
    }

    .text{
        line-height: 30px;
        color: var(--unselected-text-color);
        padding-bottom: 50px;
        font-size: 18px;
    }

    .link{
        text-decoration: none;
        color: var(--light-text-color);
        font-weight: 500;
        font-size: 18px;
    }

    .link i{
        padding-left: 5px;
        font-size: 14px;
    }
</style>