<script>
    import ArticleCard from './ArticleCard.vue';
    export default {
        name:"ArticlesList",

        components:{
            ArticleCard,
        },

        data(){
            return{
                articleList:[
                    {
                        img:"src/assets/blog4-2x-400x258.jpg",
                        title:"The best protein shake",
                        from: "By admin | November 26th, 2019 | Gym",
                    },
                    {
                        img: "src/assets/blog1-2x-400x258.jpg",
                        title:"Ultimate cardio workout",
                        from: "By admin | November 26th, 2019 | Gym",
                    },
                    {
                        img:"src/assets/blog3-2x-400x258.jpg",
                        title:"New juices available now",
                        from: "By admin | November 26th, 2019 | Gym",
                    }
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="container top">
            <span class="sec-title">Latest articles</span>
            <span class="other-articles">Read all articles <i class="fa-solid fa-chevron-right"></i></span>
        </div>
        <div class="container">
            <div class="card-wrapper" v-for="(element, i) in articleList" :key="i">
                <ArticleCard 
                :img="element.img"
                :title="element.title"
                :from="element.from"
                ></ArticleCard>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    section{
        padding: 130px 0;
    }

    .container{
        @include mixins.container;
        display: flex;
        justify-content: space-between;
    }

    .card-wrapper{
        width: calc(100% /3);
    }

    .top{
        padding-bottom: 50px;
    }

    .other-articles{
        padding-right: 80px;
        font-weight: 500;
    }

    .other-articles i{
        font-size: 14px;
    }

    .sec-title{
        font-size: 28px;
    }
</style>