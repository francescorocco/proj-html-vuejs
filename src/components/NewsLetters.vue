<script>
    export default{
        name:"NewsLetters",
    }
</script>

<template>
    <section>
        <div class="container">
            <h3 class="red-text">Join our mailing list today</h3>
            <h2>Insider offers & flash sales in your <br> inbox every week.</h2>
            <div class="underline"><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i><i class="fa-solid fa-angle-up"></i></div>
            <div>
                <input type="text" placeholder="Insert your email ...*">
                <button class="blue-button">Subscribe</button>
                <div class="paragraph">Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur <br> adipiscing elit sed porttitor lectus.</div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
    @use "../style/general.scss";
    @use "../style/partials/mixins";

    section{
        background-image: linear-gradient(to left, rgba(0, 0, 0, 0) 20%, rgba(0, 0, 0, 1) 60%,rgba(0, 0, 0, 1) 100%), url(../assets/banner1-2x.jpg); 
        height: 730px;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: right;
    }

    .container{
        @include mixins.container;
        padding: 150px 0;
    }

    .red-text{
        color: var(--red-text-color);
        font-size: 24px;
        font-weight: 500;
        padding-bottom: 30px;
    }

    h2{
        color: var(--light-text-color);
        font-size: 50px;
        font-weight: 500;
        padding-bottom: 30px;
    }

    .underline{
        color: var(--underline-color);
        font-size: 24px;
        padding-bottom: 40px;
    }

    .underline i:not(:first-of-type){
        margin-left: -5px;
    }

    input{
        font-size: 18px;
        padding: 15px;
        width: 500px;
        border-radius: 25px;
        border: none;
    }

    .blue-button{
        @include mixins.blue-button;
        border: none;
        font-size: 18px;
        margin-left: 30px;
        padding: 15px 100px ;
        border-radius: 30px;
    }

    .paragraph{
        color: var(--unselected-text-color);
        font-size: 20px;
        line-height: 30px;
        padding-top: 40px;
    }
</style>