<script >
export default {
    name: "SocialComponent",
    data (){
        return {

        }
    },
methods: {

}
};
</script>

<template>

    <div class="socials-container">
        <a href="https://www.facebook.com/" target="_blank"><i class="fa-brands fa-square-facebook"></i></a>
        <a href="https://www.pinterest.it/" target="_blank"><i class="fa-brands fa-square-pinterest"></i></a>
        <a href="https://twitter.com/" target="_blank"><i class="fa-brands fa-square-twitter"></i></a>
        <a href="https://www.linkedin.com/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
        <a href="https://www.instagram.com/" target="_blank"><i class="fa-brands fa-instagram"></i></a>
    </div>

</template>

<style lang="scss" scoped>

@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

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

</style>