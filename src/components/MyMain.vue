<script>
    import WhoWeAreSec from "./WhoWeAreSec.vue"
    export default {
        name: 'MyMain',

        components: {
            WhoWeAreSec,
        }
    }
</script>

<template>
    <main>
        <WhoWeAreSec></WhoWeAreSec>
    </main>
</template>

<style scoped lang="scss">
    main{
        font-family:  'Marsden Narrow','Yantramanav', sans-serif;
    }
</style>