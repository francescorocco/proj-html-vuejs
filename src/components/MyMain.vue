<script>
    import WhoWeAreSec from "./WhoWeAreSec.vue"
    import VisitUsSec from "./VisitUsSec.vue"
    export default {
        name: 'MyMain',

        components: {
            WhoWeAreSec,
            VisitUsSec,
        }
    }
</script>

<template>
    <main>
        <WhoWeAreSec></WhoWeAreSec>
        <VisitUsSec></VisitUsSec>
    </main>
</template>

<style scoped lang="scss">
    main{
        font-family:  'Marsden Narrow','Yantramanav', sans-serif;
    }
</style>