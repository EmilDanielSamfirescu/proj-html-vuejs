<script >
export default {
    name: "HeaderComponent",
data (){
    return {
        headerNavLinks: [
            'Home',
            'About',
            'Services',
            'Training',
            'Blogs'
        ]
    }
},
methods: {

}
};
</script>

<template>
    <header>

        <section class="info-header">
            <div class="my-container">
                <div class="my-row justify-content-between align-items-center">

                    <div class="info-container my-row">
                        <div>
                            <span>
                                <i class="fa-solid fa-envelope"></i>
                            </span> 
                            info@example.com
                        </div>

                        <div>
                            <span>
                                <i class="fa-solid fa-phone"></i>
                            </span> 
                            +1(817)9013377
                        </div>
                    </div>

                    <div class="socials-container">
                        <a href="https://www.facebook.com/" target="_blank"><i class="fa-brands fa-square-facebook"></i></a>
                        <a href="https://www.pinterest.it/" target="_blank"><i class="fa-brands fa-square-pinterest"></i></a>
                        <a href="https://twitter.com/" target="_blank"><i class="fa-brands fa-square-twitter"></i></a>
                        <a href="https://www.linkedin.com/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
                        <a href="https://www.instagram.com/" target="_blank"><i class="fa-brands fa-instagram"></i></a>
                    </div>

                </div>
            </div>
        </section>

        <section class="menu-header">
            <div class="my-container">
                <div class="my-row justify-content-between align-items-center">

                    <div class="logo-container">
                        <a href="#">
                            <img src="../assets/img/logo.png" alt="logo">
                        </a>
                    </div>

                    <div class="link-contaner d-flex justify-content-between align-items-center">
                        <div class="links-menu"
                        v-for="(links, i) in headerNavLinks" :key="i">
                            <a href="#">{{ links }}</a>
                        </div>
                        <button>
                            Get In Touch!
                        </button>
                    </div>

                </div>
            </div>
        </section>

        <section class="jumbotron">

            <div id="arrow-l">
                <img src="../assets/img/arrow.svg" alt="">
            </div>

            <div id="arrow-r">
                <img src="../assets/img/arrow.svg" alt="">
            </div>

            <div class="jumbotron-img-container">
                <img src="../assets/img/b.png" alt="">
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
                        <img src="../assets/img/play.png" alt="play-icon">
                    </div>
                </div>
            </div>

        </section>

    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

.info-header {
    background-color: $top-header-bg-color;
    .my-row {
    padding: 5px 0px;
    color: white;
    font-size: 15px;

        .info-container * i {
            color: #ce7c2a;
        }

        .info-container > div:first-child {
            margin-right: 20px;
        }

        .socials-container {

            a {
                list-style: none;
                color: white;
                margin-right: 5px;
                i{

                &.fa-brands{
                    padding: 3px;
                    border-radius: 3px;
                    &.fa-square-facebook {
                        background-color: #333BB0;
                    }
                    &.fa-square-pinterest {
                        background-color: #B03E4E;
                    }
                    &.fa-square-twitter {
                        background-color: #96D0CD;
                    }
                    &.fa-linkedin {
                        background-color: #0B65CB;
                    }
                    &.fa-instagram {
                        background-color: #992DA1;
                    }
                }
            }
            }
        }

    }
}

.menu-header {
    padding: .625rem 0rem;


    .links-menu > a{
        font-size: 1.3em;
        margin-right: 1.875rem;
        color: $text-color;
        text-decoration: none;
        padding: 30px 0px;

        &:hover {
            color: $orange-main-color;
        }
    }

    button {
        font-size: 1.3em;
        color: white;
        background-color: $orange-main-color;
        border: none;
        border-radius: 50px;
        padding: .625rem 1.5625rem;

        &:hover {
            background-color: $button-hover-color;
        }
    }
}

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