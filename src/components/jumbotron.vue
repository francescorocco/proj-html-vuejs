<script>
    import playButton from "./playButton.vue"
    export default {
        name: 'jumbotron',

        components:{
            playButton,
        }
    }
</script>

<template>
        <div class="hero">
            <div class="container">
                <h4>Certified fitness professional</h4>
                <h1>Take control of your health</h1>
                <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
                <div class="quote">Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</div>
                <div class="button-wrap">
                    <div class="button-blue">
                        <i class="fa-brands fa-youtube"></i>Visit my YouTube channel
                    </div>
                    <div class="button">
                        Buy Avada today <i class="fa-solid fa-right-long"></i>
                    </div>
                </div>
                <div class="playButton">
                    <playButton></playButton>
                </div>
            </div>
        </div>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";
    .hero{
        background-image: linear-gradient(to left, rgba(0, 0, 0, 0) 20%, rgba(0, 0, 0, 1) 60%,rgba(0, 0, 0, 1) 100%), url(../assets/slider82x-scaled.jpg);
        height: 675px;
        background-position: top;
        background-size: cover;
        font-family: 'Marsden Narrow', sans-serif;
        position: relative
    }

    .container{
        @include mixins.container;
        display: flex;
        height: 90%;
        flex-direction: column;
        justify-content: center;
        color:whitesmoke
    }

    h4{
        color: var(--red-text-color);
        font-size: 27px;
        font-weight: 500;
    }

    h1{
        padding: 10px 0;
        font-size: 70px;
        font-weight: 500;
    }

    .underline{
        color: var(--underline-color);
        padding: 20px 0; 
    }

    .underline i{
        margin-right: -7px;
        font-size: 30px;
    }

    .quote{
        font-size: 22px;
        color: var(--unselected-text-color);
    }

    .button-wrap{
        display: flex;
        padding: 40px 0;
    }

    .button, .button-blue{
        @include mixins.big-button;
        font-size: 18px;
    }

    .button{
        border: 3px solid var(--border-transparent-button);
    }

    .button-blue{
        @include mixins.blue-button;
        margin-right: 15px;
        font-weight: 500;
    }

    .button-blue i{
        margin-right: 10px;
        line-height: 26px;
    }

    .playButton{
        position: absolute;
        right: 400px;
        top: 35%;
    }

</style>