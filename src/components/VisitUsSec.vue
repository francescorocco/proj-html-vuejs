<script>
    import playButton from "./playButton.vue"
    export default{
        name: "VisitUsSec",

        components:{
            playButton
        }
    }
</script>


<template>
    <section>
        <div class="container-flex">
            <div class="img-wrapper">
                <img class="big-img" src="../assets/service15-2x.jpg" alt="">
                <div class="play-button">
                    <playButton></playButton>
                </div>
            </div>
            <div class="visit-information">
                <div class="blu-text">Tune up your workouts</div>
                <h2>The best health & fitness advice online</h2>
                
                <div class="yt-profile-card">
                    <img class="small-logo" src="../assets/unnamed.jpg" alt="logo">
                    <div class="yt-btn">
                        <div class="logo-name">Team Fusion</div>
                        <div class="red-box"><i class="fa-brands fa-youtube"></i>YouTube</div>
                    </div>
                    <div class="gray-box">999+</div>
                </div>
            
                <div class="text-quote">Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper maurist venenatist leo integer sit pellentesque.</div>
            
                <div class="big-yt-button">
                    <i class="fa-brands fa-youtube"></i>
                    <a href="#">Visit my YouTube channel<i class="fa-solid fa-angle-right"></i></a>
                </div>    
            </div>
        </div>
    
        <div class="container">
            <div>Featured playlist</div>
            <div>View all videos<i class="fa-solid fa-angle-right"></i></div>
            
            <div class="videos-wrapper">
                <div class="card-video">
                    <div class="video-img">
                        <img  class="thumb" src="../assets/video2-2x.jpg" alt="">
                    </div>
                    <div class="video-name">Thiahs & qlute workout</div>
                    <div class="video-focused-on">Increase your mobility</div>
                </div>
                <div class="card-video">
                    <div class="video-img">
                        <img class="thumb"  src="../assets/video7-2x.jpg" alt="">
                    </div>
                    <div class="video-name">Lift, firm & perk up</div>
                    <div class="video-focused-on">Feel young again</div>
                </div>
                <div class="card-video">
                    <div class="video-img">
                        <img  class="thumb" src="../assets/video9-2x.jpg" alt="">
                    </div>
                    <div class="video-name">Slim & trim your waistYYYy</div>
                    <div class="video-focused-on">Shed those extra pounds</div>
                </div>
            </div>
        </div>
    </section>
    
</template>


<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    section{
        padding-bottom: 150px;
    }

    .container-flex {
        display: flex;
    }

    .big-img, .thumb{
        @include mixins.rounded-img;
    }

    .img-wrapper{
        width: 1000px;
        height: 850px;
        margin-top: -60px;
        object-fit: cover;
        position:relative
    }

    .play-button{
        position: absolute;
        top: 43%;
        left: 43%;
    }

    .visit-information{
        margin:150px
    }

    .blu-text{
        color: var(--blue-text-color);
        font-size: 30px;
        font-weight: 500;
    }

    h2{
        font-size: 60px;
        font-weight: 500;
        margin-top: 60px;
    }

    .yt-profile-card{
        display: flex;
        align-items: center;
        margin: 50px 0;
    }

    .red-box{
        background-color: var(--red-text-color);
        padding: 3px;
        font-size: 14px;
        color: var(--light-text-color);
        border: 1px solid lightgray;
        border-right: none;
    }

    .red-box i{
        padding-right: 5px;
    }

    .gray-box{
        background-color: rgb(240, 240, 240);
        padding: 5.5px;
        font-size: 10px;
        margin-top: 19px;
        border: 1px solid lightgray;

    }

    .small-logo{
        width: 60px;
        padding-right: 10px;
    }

    .text-quote{
        font-size: 20px;
        line-height: 35px;
        padding-bottom: 50px;
    }

    .big-yt-button{
        @include mixins.big-button;
        background-color: var(--red-button-background);
        width: fit-content;
        color: var(--light-text-color);
    }

    .big-yt-button i{
        padding-right: 10px;
    }

    .big-yt-button a{
        text-decoration: none;
        color: var(--light-text-color);
        font-weight: 500;
    }

    .container{
        @include mixins.container;
    }

    .videos-wrapper{
        @include mixins.d-flex-space-between;
    }

    .video-img{
        height: 250px;
        width: 410px;
    }

    .video-name{
        text-align: center;
        font-size: 20px;
        font-weight: 500;
        padding: 20px 0;
    }

    .video-focused-on{
        text-align: center;
        color: var(--blue-text-color);
        font-size: 18px;
        font-weight: 400;
    }

</style>