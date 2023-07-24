<script >
export default {
    name: "MainComponent",
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
        <!-- FIRST SECTION -->
        <section class="section-about-us">
            <div class="my-container">
                <div class="my-row justify-content-between">

                    <div class="left-img-container">
                        <img src="../assets/img/about.png" alt="">
                    </div>

                    <div class="right-description">

                        <div class="upper-title d-flex align-items-center">
                            <div>
                                <img src="../assets/img/dog-icon.png" alt="dog-icon">
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

        <!-- SECOND SECTION -->
        <section class="section-services">
            SECOND SECTION
        </section>
        <!-- SECOND SECTION -->

        <!-- THIRD SECTION -->
        <section class="section-why-us">
            
                <div class="my-row">

                    <div class="left">
                        <img src="../assets/img/why.png" alt="">
                    </div>

                    <div class="right">
                        <div class="upper-title d-flex align-items-center">
                            <div>
                                <img src="../assets/img/dog-icon.png" alt="dog-icon">
                            </div>
                            <p>Choose us</p>
                        </div>

                        <h2>Why Choose Us?</h2>

                        <div class="reasons-to-choose">
                            <div class="col-12">a</div>
                            <div class="col-9 offset-4">b</div>
                            <div class="col-6 offset-6">c</div>
                        </div>
                    </div>

                </div>

        </section>
        <!-- THIRD SECTION -->

        <!-- FOURF SECTION -->
        <section class="section-customers">
            FOURF SECTION
        </section>
        <!-- FOURF SECTION -->

    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;
.section-about-us {
    .my-row {
        padding: -30px;
        margin: 50px 0px;
        .left-img-container {
            width: calc(100% / 2);
            max-width: 500px;

            img {
                width: 100%;
                display: block;
                padding: 30px;
            }
        }

        .right-description {
            width: calc(100% / 2);
            margin-top: 50px;
            padding: 30px;
            

            .upper-title {
                p {
                    margin-bottom: 0;
                    margin-left: 10px;
                    color: $top-header-bg-color;
                }
            }

            h2 {
                margin: 20px 0px;
            }
        }
    }
}

.section-services {
    @include debug-2
}

.section-why-us {
    @include debug-3;

    .left {
        width: calc(100% / 2);

        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .right {
        width: calc(100% / 2);
        .upper-title {
                p {
                    margin-bottom: 0;
                    margin-left: 10px;
                    color: $top-header-bg-color;
                }
            }

        .reasons-to-choose {
            // text-align: end;
            .col-12 {
                @include debug-1;
            }

            .col-9 {
                @include debug-2;
                offset: 4;
            }

            .col-6 {
                @include debug-4;
            }
        }
    }
}

.section-customers {
    @include debug-4
}

</style>