<script>
    import ActivityCard from "./ActivityCard.vue"
    export default{
        name: "ActivitiesSec",

        components:{
            ActivityCard
        },

        data(){
            return {
                activitiesList: [
                {
                    img:"src/assets/sponsor-1-2x-200x103.png",
                    text: "Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.",
                    link:"Visit Yoga Studio"
                },
                {
                    img: "src/assets/sponsor-2-2x-200x103.png",
                    text:"Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.",
                    link:"Join Fitness Center"
                },
                {
                    img: "src/assets/sponsor-3-2x-200x103.png",
                    text:"Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et sagittis imperdiet.",
                    link:"Learn about FC"
                },
                {
                    img: "src/assets/sponsor-4-2x-200x103.png",
                    text:"Proin in viverra maecenas et mattis ut nibh enim. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.",
                    link:"Visit Power Gym"
                }
            ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="container">
            <div class="card-wrapper" v-for="(element,i) in activitiesList" :key="i">
                <ActivityCard
                :img="element.img"
                :text="element.text"
                :link="element.link"
                ></ActivityCard>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    .container{
        @include mixins.container;
        @include mixins.d-flex-space-between;
    }

    .card-wrapper{
        width: calc((100% / 4) - 10px);
    }
</style>