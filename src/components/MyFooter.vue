<script>
    export default {
        name: 'footer',

        props: {
            footerMenuVoice: Array,
        },
    }
</script>

<template>
    <footer>
        <div class="container">
            <div class="upper-footer">
                <ul class="left-list">
                    <li class="logo">
                        <img :src="footerMenuVoice[0].logo" alt="">
                    </li>
                    
                    <li>
                        <div class="paragraph">{{ footerMenuVoice[0].paragraph }}</div>
                    </li>

                    <li class="icons">
                        <i v-for="(elements, i) in footerMenuVoice[0].icons" class="fa-brands" :class="elements" :key="i"></i>
                    </li>
                </ul>

                <ul class="center-list">
                    <li>{{ footerMenuVoice[1].headerMenu }}</li>
                    <li class="link-to" v-for="(elements, i) in footerMenuVoice[1].listMenu" :key="i"><i class="fa-solid fa-chevron-right"></i>{{elements}}</li>
                </ul>

                <ul class="right-list">
                    <li>{{ footerMenuVoice[2].headerMenu }}</li>
                    <li class="addres">{{ footerMenuVoice[2].addres }}</li>
                    <li class="number">Mobile: {{footerMenuVoice[2].mobile}}</li>
                    <li class="email">Email: {{footerMenuVoice[2].headerMenu}}</li>
                </ul>
            </div>
        </div>
        <div>
            <hr>

            <div class="lower-footer">
                <div class="copyright">© Copyright 2012 - 2020 | Avada theme by <span>ThemeFusion</span> | All rights reserved | Powered by <span>WordPress</span></div>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    footer{
        background-color: var(--dark-bg-color);
        color: var(--light-text-color);
        padding: 150px 0 50px;
        font-family:  'Marsden Narrow','Yantramanav', sans-serif;

    }

    .container{
        @include mixins.container;
    }

    .upper-footer{
        display: flex;
        justify-content: space-evenly;
    }

    ul{
        max-width: calc(100% / 3);
        text-align: center;
        list-style: none;
        font-size: 18px;
    }

    li{
        width: 370px;
        line-height:32px;
    }

    li:first-child{
        padding-bottom:30px;
        font-size: 18px;
        font-weight: 500;
    }

    .icons{
        color: var(--red-text-color);
        padding-top: 40px;
    }

    .icons i{
        padding: 10px;
    }

    .center-list li{
        padding-bottom: 20px;
    }

    .link-to i{
        padding-right: 5px;
        font-size: 14px;
    }

    .addres{
        padding-bottom: 20px;
        color: var(--unselected-text-color);
    }

    .number, .email{
        font-weight: 500;
    }

    hr{
        border: none;
        height: 1px;
        background-color: var(--border-transparent-button);
        margin: 50px 0;
    }

    .lower-footer{
        text-align: center;
        color: var(--unselected-text-color);
    }

    .lower-footer span{
        color: var(--light-text-color);
        font-weight: 500;
    }
</style>