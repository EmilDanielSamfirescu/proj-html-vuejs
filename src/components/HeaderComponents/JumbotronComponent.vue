<script >
export default {
    name: "JumbotronComponent",
    data (){
        return {
            autoplay: null,
            courrentImg: 0,
            jumboSlide: [
                {
                    image: '../../assets/img/b.png',
                    title: 'Welcome To DogMilo Pets',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et, illo voluptates maxime ullam provident rem.',
                },
                {
                    image: '../../assets/img/labrador.jpeg',
                    title: 'Welcome To DogMilo Pets',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil consectetur cupiditate, qui consequuntur eligendi aliquid.',
                },
                {
                    image: '../../assets/img/dog-outdoors.jpg',
                    title: 'Welcome To DogMilo Pets',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam blanditiis excepturi provident, ratione corporis possimus.',
                },
                {
                    image: '../../assets/img/dog-pet.jpg',
                    title: 'Welcome To DogMilo Pets',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Optio ad dolor corporis quos nobis placeat.',
                },
                {
                    image: '../../assets/img/husky-dog.jpg',
                    title: 'Welcome To DogMilo Pets',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, excepturi sint esse recusandae debitis quo.',
                },
            ]
        }
    },
    methods: {
        getImagePath: function(image){
                return new URL (image, import.meta.url).href;
            },
        nextButton (){
                // console.log(`ciaone a dopo`);
                if (this.courrentImg == this.jumboSlide.length - 1){
                    this.courrentImg = 0;
                } else {
                    this.courrentImg++;
                }
            },
            prevButton (){
                // console.log(`ciao a prima`);
                if (this.courrentImg == 0){
                    this.courrentImg = this.jumboSlide.length - 1;
                } else {
                    this.courrentImg--;
                }
            },
            stopautoplay(){
                // console.log(`stoppato`);
                clearInterval(this.autoplay);
                this.autoplay = null;
            },
            restartautoplay() {
                // console.log(`ripartito`);
                this.autoplay = setInterval(() => {
                this.nextButton();
                }, 4000);
            }
            
    },
    mounted () {
        this.autoplay = setInterval(() => {
        this.nextButton();
        }, 4000);
    }
    
};
</script>

<template>
    <section class="jumbotron"
    @mouseenter="stopautoplay()"
    @mouseleave="restartautoplay()">


        <div id="arrow-l" @click="prevButton()" class="prev">
            <img src="../../assets/img/arrow.svg" alt="">
        </div>

        <div id="arrow-r" @click="nextButton()" class="next">
            <img src="../../assets/img/arrow.svg" alt="">
        </div>

        <template 
        v-for="(dogImg, i) in jumboSlide" :key="i">
            <div class="jumbotron-img-container" v-if="i == courrentImg ">
                <!-- <img src="../../assets/img/b.png" alt=""> -->
                <img :src="getImagePath(dogImg.image)" alt="various-dog">

                <div class="my-container">
                    <div class="jumbotron-description-container">
                    <h1><strong>Welcome to</strong> 
                        <br>
                        DogMilo
                        <strong>Pets!</strong></h1>
                    <p>{{dogImg.text}}</p>
                    <div>
                        <button>
                                Get Started
                        </button>
                        <div class="play-icon-container">
                            <img src="../../assets/img/play.png" alt="play-icon">
                        </div>
                    </div>
                </div>
                </div>
            </div>
        </template>

</section>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.jumbotron {
    position: relative;

    .active {
        display: block;
    }
    .jumbotron-img-container{
        width: 100%;
        height: 600px;
        overflow: hidden;
        
        
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
    top: 120px;
    left: 210px;

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
        transition: all 0.4s;

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