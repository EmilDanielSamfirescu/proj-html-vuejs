<script >

import AboutUsComponent from './MainComponents/AboutUsComponent.vue';
import ServicesComponent from './MainComponents/ServicesComponent.vue';
import TrainingComponent from './MainComponents/TrainingComponent.vue';
import BlogComponent from './MainComponents/BlogComponent.vue';

export default {
    name: "MainComponent",
    components: {
        AboutUsComponent,
        ServicesComponent,
        TrainingComponent,
        BlogComponent
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
    <main>

        <AboutUsComponent />

        <ServicesComponent />

        <TrainingComponent />

        <BlogComponent />

    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;


</style>