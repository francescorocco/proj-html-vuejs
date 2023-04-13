<script>
    import WhoWeAreSec from "./WhoWeAreSec.vue"
    import VisitUsSec from "./VisitUsSec.vue"
    import NewsLetters from "./NewsLetters.vue"
    import DescriptionCards from "./DescriptionCards.vue"
    import ArticlesList from "./ArticlesList.vue"

    export default {
        name: 'MyMain',

        components: {
            WhoWeAreSec,
            VisitUsSec,
            NewsLetters,
            DescriptionCards,
            ArticlesList,
        }
    }
</script>

<template>
    <main>
        <WhoWeAreSec></WhoWeAreSec>
        <VisitUsSec></VisitUsSec>
        <NewsLetters></NewsLetters>
        <DescriptionCards></DescriptionCards>
        <ArticlesList></ArticlesList>
    </main>
</template>

<style scoped lang="scss">
    main{
        font-family:  'Marsden Narrow','Yantramanav', sans-serif;
    }
</style>