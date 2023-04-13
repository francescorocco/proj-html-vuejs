<script>
    import CardBlueBorder from './CardBlueBorder.vue';

    export default{
        name: "DescriptionCards",

        components:{
            CardBlueBorder
        },
        data(){
            return{
                decriptionsCard:[
                {
                    icon:'fa-people-group',
                    title:"Team training",
                    subtitle:"Find a partner",
                    text:"Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.",
                    link:"Find a partner"    
                },
                {
                    icon:'fa-dumbbell',
                    title:"Crossfit workout",
                    subtitle:"Push your limits",
                    text:"Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.",
                    link:"Lear about Crossfit"
                },
                {
                    icon:'fa-person-circle-minus',
                    title:"Weight loss plan",
                    subtitle:"Shed those pounds",
                    text:"At laoreet senectus volutpat diam vel sed sed amet pellentesque. Lobortis ut aliquam risus purus. A tellus ut etiam.",    
                    link:"Schedule a workout"    
                }
            ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="container">
            <div class="card-wrapper"  v-for="(element,i) in decriptionsCard" :key="i">
                <CardBlueBorder
                :icon="element.icon"
                :title="element.title"
                :subtitle="element.subtitle"
                :text="element.text"
                :link="element.link"    
                ></CardBlueBorder>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    section{
        background-color: var(--dark-bg-color);
        padding: 110px 0 120px ;
    }

    .container{
        @include mixins.container;
        @include mixins.d-flex-space-between;
    }

    .card-wrapper{
        width: calc(100% / 3 - 50px);
    }
</style>