<script >
export default {
    name: "JumbotronComponent",
    data (){
        return {

        }
    },
methods: {

}
};
</script>

<template>
    <section class="jumbotron">

<div id="arrow-l">
    <img src="../../assets/img/arrow.svg" alt="">
</div>

<div id="arrow-r">
    <img src="../../assets/img/arrow.svg" alt="">
</div>

<div class="jumbotron-img-container">
    <img src="../../assets/img/b.png" alt="">
</div>

<div class="jumbotron-description-container">
    <h1><strong>Welcome to</strong> 
        <br>
        DogMilo
        <strong>Pets!</strong></h1>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et, illo voluptates maxime ullam provident rem.</p>
    <div>
        <button>
                Get Started
        </button>
        <div class="play-icon-container">
            <img src="../../assets/img/play.png" alt="play-icon">
        </div>
    </div>
</div>

</section>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.jumbotron {
    position: relative;
    .jumbotron-img-container{
        width: 100%;
        img {
            width: 100%;
            display: block;
        }

    }

    #arrow-r {
        width: 100px;
        position: absolute;
        right: 0px;
        top: 50%;
        transform: translateY(-50%);
        filter: invert(60%) sepia(65%) saturate(3298%) hue-rotate(167deg) brightness(96%) contrast(100%) opacity(50%);
        cursor: pointer;

        &:hover {
            filter: invert(60%) sepia(65%) saturate(3298%) hue-rotate(167deg) brightness(96%) contrast(100%) opacity(100%);
        }
    }

    #arrow-l {
        width: 100px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%) scaleX(-1);
        filter: invert(60%) sepia(65%) saturate(3298%) hue-rotate(167deg) brightness(96%) contrast(100%) opacity(30%);
        cursor: pointer;

        &:hover {
            filter: invert(60%) sepia(65%) saturate(3298%) hue-rotate(167deg) brightness(96%) contrast(100%) opacity(100%);
        }
    }
    
    
    .jumbotron-description-container{
        width: 500px;
        color: white;
        position: absolute;
        top: 150px;
        left: 150px;

        h1 {
            font-size: 3.5em;
            line-height: 1.2em;
        }

        p{
            font-size: 1.1em;
            margin: 1.5625rem 0rem;
        }

        button {
            font-size: 1.3em;
            color: white;
            background-color: $orange-main-color;
            border: none;
            border-radius: 50px;
            padding: .625rem 1.5625rem;
            vertical-align: middle;
    
            &:hover {
                background-color: $button-hover-color;
            }
        }

        .play-icon-container {
                width: 3.125rem;
                display: inline-block;
                vertical-align: middle;
                margin-left: .9375rem;
            img {
                width: 100%;
                padding: 10px;
                display: block;
                background-color: $play-color;
                border-radius: 10px;

                &:hover {
                    cursor: pointer;
                }
            }
        }
    }



}

</style>