<script >

import NavLinkBar from './HeaderComponents/NavLinkBar.vue';
import JumbotronComponent from './HeaderComponents/JumbotronComponent.vue';
import SocialComponent from './HeaderComponents/SocialComponent.vue'


export default {
    name: "HeaderComponent",
    components: {
        NavLinkBar,
        JumbotronComponent,
        SocialComponent
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

                    <SocialComponent />

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
    padding: .3125rem 0rem;
    color: white;
    font-size: 15px;

        .info-container * i {
            color: #ce7c2a;
        }

        .info-container > div:first-child {
            margin-right: 1.25rem;
        }

    }
}

</style>