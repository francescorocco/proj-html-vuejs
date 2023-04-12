<script>
 import cardImg from "./cardImg.vue"

    export default {
        name: "WhoWeAreSec",

        components: {
            cardImg,
        },
        data(){
            return{
                cardList:[
                    {
                        imgUrl:"src/assets/service6-2x.jpg",
                        cardTitle:"Crosfit workout",
                        cardSubtitle: "Push your limits",
                    },
                    {
                        imgUrl:"src/assets/box1-2x.jpg",
                        cardTitle:"New gym apparel",
                        cardSubtitle: "Look good, feel good",
                    },
                    {
                        imgUrl:"src/assets/box3-2x.jpg",
                        cardTitle:"Team training",
                        cardSubtitle: "Find a partner",
                    }
                ]
            }
        }
        
    }
</script>


<template>
    <section>
        <div class="container">
            <div class="img-wrapper">
                <cardImg v-for="(element,i) in cardList" :key="i" 
                :imgUrl="element.imgUrl"
                :cardTitle="element.cardTitle"
                :cardSubtitle="element.cardSubtitle"
                ></cardImg>
                
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";


    section{
        background: linear-gradient(157deg, var(--section-dark-color) 0%, var(--section-mid-color) 61%, var(--section-light-color) 100%);
        height: 1020px;
    }

    .container{
        @include mixins.container;
        position: relative;
    }

    .img-wrapper{
        @include mixins.d-flex-space-between;
        margin-top:-50px;
    }
</style>