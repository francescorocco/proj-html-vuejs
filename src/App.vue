<script>
  import MyHeader from './components/MyHeader.vue';
  import jumbotron from './components/jumbotron.vue';


    export default {
        components: {
            MyHeader,
            jumbotron,
        },
        data(){
            return{
                headerMenuVoice:['Home','Services','About','Videos','Blog','Store'],
            }
        }
    }
</script>

<template>
    <MyHeader :headerMenuVoice="this.headerMenuVoice"></MyHeader>
    <jumbotron></jumbotron>
</template>

<style lang="scss">
    @use "./style/general.scss";
</style>
