<script>
    export default {
        name: 'MyHeader',

        props:{
            headerMenuVoice: Array,
        }
    }
</script>

<template>
    <div class="container">
        <header>
            <div>
                <img src="src/assets/logo.png" alt="logo avada fitnes">
            </div>
            <div>
                <ul>
                    <li v-for="element in headerMenuVoice">
                        <a href="#">{{ element }}</a>
                    </li>
                </ul>
            </div>
        </header>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/general.scss";

</style>