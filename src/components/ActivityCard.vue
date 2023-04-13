<script>
    export default {
        name:"ActivityCard",

        props: {
            img: String,
            text: String,
            link: String
        }
    }
</script>

<template>
    <div class="card">
        <div class="img-wrapper">
            <img :src=img alt="">
        </div>
        <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
        <div class="text">{{ text }}</div>
        <a href="#">{{ link }} <i class="fa-solid fa-chevron-right"></i></a>
    </div>
</template>


<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    .card{
        text-align: center;
        padding: 100px 20px 150px;
    }

    img{
        width: 60%;
    }

    .underline{
        color: var(--button-blue-background-color);
        text-align: center;
        margin-top: 20px;
        font-size: 25px;
        padding-bottom: 20px;
    }

    .underline i {
        margin-right: -5px;
    }

    .text{
        line-height: 30px;
        font-size: 18px;
        padding-bottom: 20px;
    }

    a{
        text-decoration: none;
        font-weight: 600;
        color: black;
    }
</style>