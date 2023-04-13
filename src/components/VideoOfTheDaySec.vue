<script>
import playButton from "./playButton.vue"
    export default{
        name:"VideoOfTheDaySec",

        components:{
            playButton
        },
    }
</script>

<template>
    <section>
        <div class="container">
            <div>
                <div class="play">
                    <playButton></playButton>
                </div>
                <h2>Crossfit workout of the day</h2>
                <div class="date">November 15th, 2019</div>
                <a href="#">View all videos<i class="fa-solid fa-arrow-right-long"></i></a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";
    
    section{
        background-image: linear-gradient(to top left, rgba(212, 0, 255, 0.3) 0%, rgba(10, 1, 255, 0.5) 80%), url(src/assets/banner14-2x.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        height: 650px;
        filter:brightness(0.7);
    }


    .container{
        @include mixins.container;
        @include mixins.d-flex-center-center;
        text-align: center;
        height: 100%;
    }

    .play{
        display: flex;
        justify-content: center;
        padding-bottom: 20px;
    }

    h2{
        color: var(--light-text-color);
        font-size: 50px;
        font-weight: 500;
    }

    .date{
        color: var(--underline-color);
        font-size: 30px;
        padding: 30px 0;
    }

    a{
        text-decoration: none;
        color: var(--light-text-color);
        font-size: 18px;
    }
</style>