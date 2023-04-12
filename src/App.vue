<script>
  import MyHeader from './components/MyHeader.vue';
  import jumbotron from './components/jumbotron.vue';
  import MyMain from './components/MyMain.vue';


    export default {
        components: {
            MyHeader,
            jumbotron,
            MyMain,
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
    <MyMain></MyMain>
</template>

<style lang="scss">
    @use "./style/general.scss";
</style>
