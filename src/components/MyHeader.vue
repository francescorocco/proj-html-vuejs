<script>
    export default {
        name: 'MyHeader',

        props:{
            headerMenuVoice: Array,
        },
    }
</script>

<template>
    <div class="bg-container">
        <header class="container">
            <div>
                <img src="src/assets/logo.png" alt="logo avada fitnes">
            </div>
            <div>
                <ul>
                    <li v-for="element in headerMenuVoice">
                        <a href="#">{{ element }}</a>
                    </li>
                    <li class="tag">
                        new
                    </li>
                    <li class="button">
                        Schedule a workout
                    </li>
                    <li>
                        <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
                    </li>
                </ul>
            </div>
        </header>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    .bg-container{
        background-color: var(--dark-bg-color);
        font-family:  'Marsden Narrow','Yantramanav', sans-serif;
    }
    header.container{
        @include mixins.container;
        @include mixins.d-flex-space-between;
        height: 100px;
        align-items: center;
    }

    ul{
        @include mixins.list;
    }

    li{
        padding: 5px;
        margin-right: 22px;
        color: var(--light-text-color);
    }

    a{
        text-decoration: none;
        color: var(--unselected-text-color);
        font-weight: 400;
        font-size: 18px;
        
    }

    .tag{
        background-color: var(--news-tag-bg-color);
        color: black;
        padding: 3px 6px;
        margin-left: -20px;
        height: 24px;
        border-radius: 3px;
        font-size: 14px;
    }    
    
    .button{
        @include mixins.blue-button;
        @include mixins.big-button;
        margin: 0 30px;
    }
    
    .button:hover{
        background-color: var(--red-button-background);
    }

    a i {
        font-size: 16px;
    }
    
    a:hover{
        color: var(--light-text-color);
    }
</style>