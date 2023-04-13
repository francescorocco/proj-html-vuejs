<script>
  import MyHeader from './components/MyHeader.vue';
  import jumbotron from './components/jumbotron.vue';
  import MyMain from './components/MyMain.vue';
  import MyFooter from './components/MyFooter.vue';


    export default {
        components: {
            MyHeader,
            jumbotron,
            MyMain,
            MyFooter,
        },
        data(){
            return{
                headerMenuVoice:['Home','Services','About','Videos','Blog','Store'],
                
                footerMenuVoice:[
                    {
                        logo:"src/assets/logo.png",
                        paragraph:"AC aliquam neque sagittis diam faucibus vitae purus turpis phasellus. Pellentesque consectetur amet purus ultrices mauris.",
                        icons:['fa-facebook-f','fa-twitter','fa-youtube','fa-instagram','fa-linkedin-in']
                    },
                    {
                        headerMenu: "RECENT POST",
                        listMenu:['The best protein shake','Ultimate cardio workout','New juices available now','Tips to find trainig partners','20 best healthy recipes',],
                    },
                    {
                        headerMenu:"CONTACT INFORMATION",
                        addres:"4746 Tripple Road Michigan 48449",
                        mobile:"1.800.000.0000",
                        email:"info@your-company.com"
                    }
                ],
            }
        }
    }
</script>

<template>
    <MyHeader :headerMenuVoice="headerMenuVoice"></MyHeader>
    <jumbotron></jumbotron>
    <MyMain></MyMain>
    <MyFooter :footerMenuVoice="footerMenuVoice"></MyFooter>
</template>

<style lang="scss">
    @use "./style/general.scss";
</style>
