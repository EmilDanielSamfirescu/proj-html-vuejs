<script >

import NavLinkBar from './HeaderComponents/NavLinkBar.vue';
import JumbotronComponent from './HeaderComponents/JumbotronComponent.vue';

export default {
    name: "HeaderComponent",
    components: {
        NavLinkBar,
        JumbotronComponent
    },
data (){
    return {
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

        <NavLinkBar />

        <JumbotronComponent />



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




</style>