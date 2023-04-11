<script>
  import MyHeader from './components/MyHeader.vue';

    export default {
        components: {
            MyHeader,
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
</template>

<style lang="scss">
    @use "./style/general.scss";
</style>
