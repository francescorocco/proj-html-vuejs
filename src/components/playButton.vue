<script>
    export default {
        name: 'playButton',
    }
</script>

<template>
    <div class="circle">
        <i class="fa-solid fa-play"></i>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixins";

    .circle{
        background-color: var(--light-bg-color);
        color: var(--button-blue-background-color);
        height: 100px;
        width: 100px;
        border-radius: 50%;
        @include mixins.d-flex-center-center
    }

    i{
        font-size: 22px;
    }
</style>