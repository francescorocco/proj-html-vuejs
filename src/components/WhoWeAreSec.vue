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
                
                	<!-- Qua vengono gestite le 3 immagini in primo piano -->

                <cardImg v-for="(element,i) in cardList" :key="i" 
                :imgUrl="element.imgUrl"
                :cardTitle="element.cardTitle"
                :cardSubtitle="element.cardSubtitle"
                ></cardImg>
            </div>

            <article>"How you respond to the challenge in the second half <br> will determine what you become after the game,<br> whether you are a winner or a loser."</article>

            <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
            
                    <!-- Qua viene gestrita la card contenente l'autore della citazione -->
            <div class="small-card">
                <div class="circular-img-wrapper">
                    <img class="circular-img" src="../assets/avatar-1-2x.jpg" alt="Brand Johnson">
                </div>
                <div class="name-box">Brand Johnson</div>
                <div class="place-box">Las Vegas</div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";


    section{
        background: linear-gradient(157deg, var(--section-dark-color) 0%, var(--section-mid-color) 61%, var(--section-light-color) 100%);
        height: 1120px;
    }

    .container{
        @include mixins.container;
        position: relative;
    }

    .img-wrapper{
        @include mixins.d-flex-space-between;
        margin-top:-50px;
    }

    article{
        text-align: center;
        margin-top: 150px;
        color: var(--light-text-color);
        font-size: 50px;
        font-weight: 500;
        line-height: 70px;
    }

    .underline{
        color: var(--underline-color);
        text-align: center;
        margin-top: 60px;
        font-size: 35px;
    }

    .underline i {
        margin-right: -6px;
    }

    .circular-img-wrapper{
        width: 60px;
        height: 60px;
        border-radius: 50%;
        object-fit: contain;
        
    }

    .circular-img{
        width: 100%;
        height: 100%;
        border-radius: 50%;
    }

    .small-card{
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 20px;
        font-weight: 500;
    }

    .name-box{
        color: var(--light-text-color);
        padding: 0 20px;
    }

    .place-box{
        color: var(--unselected-text-color);
    }
</style>