<script >
export default {
    name: "NavLinkBar",
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
    props:{
        
    },
    methods: {
        

    }
};
</script>

<template>

    <section class="menu-header">
            <div class="my-container">
                <div class="my-row justify-content-between align-items-center">

                    <div class="logo-container">
                        <a href="#">
                            <img src="../../assets/img/logo.png" alt="logo">
                        </a>
                    </div>

                    <div class="link-contaner d-flex justify-content-between align-items-center">
                        <div class="links-menu"
                        v-for="(links, i) in headerNavLinks" :key="i">
                            <a :href="`#${links}`">{{ links }}</a>
                        </div>
                        <button>
                            Get In Touch!
                        </button>
                    </div>

                </div>
            </div>
        </section>
        
</template>

<style lang="scss" scoped>

@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.menu-header {
    padding: .625rem 0rem;
    background-color: white;
    position: sticky;
    top: 0px;
    z-index: 10;


    .links-menu > a{
        font-size: 1.3em;
        margin-right: 1.875rem;
        color: $text-color;
        text-decoration: none;
        padding: 1.875rem 0rem;
        transition: all 0.4s;

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
        box-shadow: .1875rem .1875rem .4375rem rgb(137, 137, 137);
        transition: all 0.4s;

        &:hover {
            background-color: $button-hover-color;
        }
        &:active {
            box-shadow: 1px 1px 4px rgb(112, 112, 112);
        }
    }
}

</style>