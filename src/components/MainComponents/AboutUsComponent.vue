<script >

export default {
    name: "AboutUsComponent",
    data (){
        return {

        }
    },
    methods: {

    }
};
</script>

<template>
    <!-- FIRST SECTION -->
    <section class="section-about-us" id="About">
            <div class="my-container">
                <div class="my-row justify-content-between">

                    <div class="left-img-container">
                        <img src="../../assets/img/about.png" alt="">
                    </div>

                    <div class="right-description">

                        <div class="upper-title d-flex align-items-center">
                            <div>
                                <img src="../../assets/img/dog-icon.png" alt="dog-icon">
                            </div>
                            <p>About us</p>
                        </div>

                        <h2>Welcome DogMilo Pets</h2>

                        <div>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem tenetur at nihil, sunt omnis, fuga, laborum soluta fugit numquam reiciendis cupiditate officiis natus pariatur? Eveniet.
                            </p>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem tenetur at nihil, sunt omnis, fuga, laborum soluta fugit numquam reiciendis cupiditate officiis natus pariatur? Eveniet.
                            </p>
                        </div>

                    </div>

                    
                </div>
            </div>
        </section>
        <!-- FIRST SECTION -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.section-about-us {
    position: relative;

    &::before {
        content: '';
        display: table;
        background-image: url('../../assets/img/dog-left.png');
        background-size: cover;
        height: 15.625rem;
        width: 15.625rem;
        position: absolute;
        right: 0px;
        transform: scaleX(-1);
    }

    &::after {
        content: '';
        display: table;
        background-image: url('../../assets/img/dog-left.png');
        background-size: cover;
        height: 12.5rem;
        width: 12.5rem;
        position: absolute;
        bottom: -18.75rem;
    }

    .my-row {
        padding: -1.875rem;
        margin: 3.125rem 0rem;
        .left-img-container {
            width: calc(100% / 2);
            max-width: 31.25rem;

            img {
                width: 100%;
                display: block;
                padding: 1.875rem;
            }
        }

        .right-description {
            width: calc(100% / 2);
            margin-top: 3.125rem;
            padding: 1.875rem;
            

            .upper-title {
                p {
                    margin-bottom: 0;
                    margin-left: .625rem;
                    color: $top-header-bg-color;
                }
            }

            h2 {
                margin: 1.25rem 0rem;
            }
        }

    }
}

</style>