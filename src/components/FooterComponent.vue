<script >
import { useAttrs } from 'vue';

export default {
    name: "FooterComponent",
data (){
    return {
        support: [
            'contact us',
            'online chat',
            'whatsapp',
            'telegram',
            'snapchat'
        ],

        about: [
            'about us',
            'blog',
            'career',
            'job',
            'in press'
        ],

        faq: [
            'account',
            'order',
            'delivery',
            'payment',
            'return'
        ]

    }
},
methods: {

}
};
</script>

<template>
    <footer>

        <section class="main-footer">
            <div class="my-container">
                <div class="my-row justify-content-between">

                    <div class="answers">
                        <div>
                            <h5>Get in Touch</h5>
                            <p>
                                Have a questions for us? <br>
                                we'll answer your questions here!
                            </p>
                        </div>

                        <div class="socials-container">
                            <a href="https://www.facebook.com/" target="_blank"><i class="fa-brands fa-square-facebook"></i></a>
                            <a href="https://www.pinterest.it/" target="_blank"><i class="fa-brands fa-square-pinterest"></i></a>
                            <a href="https://twitter.com/" target="_blank"><i class="fa-brands fa-square-twitter"></i></a>
                            <a href="https://www.linkedin.com/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
                            <a href="https://www.instagram.com/" target="_blank"><i class="fa-brands fa-instagram"></i></a>
                        </div>
                    </div>

                    <nav>
                        <ul>
                            <h5>Support</h5>
                            <li v-for="(supports, i) in support" :key="i">
                                <a href="#">
                                    {{ supports }}
                                </a>
                            </li>
                        </ul>
                    </nav>

                    <nav>
                        <ul>
                            <h5>About Us</h5>
                            <li v-for="(aboutus, i) in about" :key="i">
                                <a href="#">
                                    {{ aboutus }}
                                </a>
                            </li>
                        </ul>
                    </nav>

                    <nav>
                        <ul>
                            <h5> Faq</h5>
                            <li v-for="(faqs, i) in faq" :key="i">
                                <a href="#">
                                    {{ faqs }}
                                </a>
                            </li>
                        </ul>
                    </nav>


                    <div class="contacts">
                        <h5>Contact Me</h5>

                        <div class="d-flex">
                            <span>
                                <i class="fa-solid fa-location-arrow"></i>
                            </span>

                            <span>
                                4500 Mercantile plaza, suite <br>
                                300, forth worth, TX, 76137, USA
                            </span>

                        </div>

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

                </div>
            </div>
        </section>

        <section class="bottom-footer">
            <div>
                Copyright 2023 by AttdogMilo.com
            </div>
        </section>

    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

.main-footer {
    color: white;
    background-color: black;
    color: $text-color;
    padding: 40px 0px;
    border-bottom: 1px solid $text-color;

    h5 {
        color: $orange-main-color;
    }
    .answers{
        
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


    ul {
        list-style: none;

        li{
            margin-bottom: 5px;

            &::first-letter{
                text-transform: uppercase;
            }

            a{
                text-decoration: none;
                color: $text-color;

                &:hover {
                    color: $orange-main-color;
                }
            }
        }
    }

    .contacts {
        div {
            margin-bottom: 5px;

            i {
                color: $orange-main-color;
                margin-right: 10px;
            }
        }
    }
}

.bottom-footer {
    color: white;
    background-color: black;
    text-align: center;
    padding: 20px;
}

</style>
