<script>
    export default {
        name: 'cardImg',

        props:{
            imgUrl: String,
            cardTitle: String,
            cardSubtitle: String,

        }
    }
</script>

<template>
    <div class="img-wrapper">
        <img :src=imgUrl alt="">
        <div class="text-area">
            <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
            <h2>{{ cardTitle }}</h2>
            <h3>{{ cardSubtitle }}</h3>    
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";
    .img-wrapper {
        width: 410px;
        height: 435px;
        object-fit: contain;
        position: relative;
    }

    img{
        width: 100%;
        height: 100%;
        border-radius: 5px 5px 50px;
    }

    .img-wrapper:after{
        content: '';
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        border-radius: 5px 5px 50px;
        background: linear-gradient(0deg, black 0%, transparent 40%);
    }

    .text-area{
        position: absolute;
        bottom: 50px;
        left: 50px;
        z-index: 90;
    }

    .underline i{
        color: var(--light-text-color);
        margin-right: -3px;
        font-size: 18px;
    }

    h2{
        color: var(--light-text-color);
        font-weight: 500;
        font-size: 35px;
    }

    h3{
        color: var(--news-tag-bg-color);
        font-weight: 500;
        font-size: 25px;
    }

</style>