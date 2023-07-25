<script >
import { useAttrs } from 'vue';
import SocialComponent from './HeaderComponents/SocialComponent.vue';

export default {
    name: "FooterComponent",
    components: {
        SocialComponent
    },
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

                        <SocialComponent />
                        
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
