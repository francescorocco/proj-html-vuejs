<script>
    export default {
        name:"BannerBuySec",
    }
</script>

<template>
    <section>
        <div class="container">
            <div class="wrapper">
                <h2>"l've failed over and over again in my life. And that is why I succeed."</h2>
                <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
                
                <div class="text">Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed massa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis</div>
                <div class="button">Buy Avada today <i class="fa-solid fa-chevron-right"></i></div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    section{
        background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0) 20%, rgba(0, 0, 0, 1) 100%,rgba(0, 0, 0, 1) 100%), url(src/assets/banner2-2x.jpg);
        height: 780px;
        background-size: cover;
        background-repeat: no-repeat;
    }

    .container{
        @include mixins.d-flex-center-center;
        height: 100%;
        text-align: center;
        color: var(--light-text-color);
    }

    .wrapper{
        width: 800px;
    }

    h2{
        font-size: 50px;
        font-weight: 500;
        padding-bottom: 30px;
    }

    .underline{
        color: var(--underline-color);
        padding-bottom: 30px;
        font-size: 30px;
    }

    .underline i:not(:first-of-type){
        margin-left: -6px;
    }
    .text{
        font-size: 20px;
        line-height: 33px
    }

    .button{
        @include mixins.blue-button;
        @include mixins.big-button;
        display: inline-block;
        margin-top: 50px;
        font-size: 18px;
    }

    .button i{
        font-size: 14px;
    }
</style>