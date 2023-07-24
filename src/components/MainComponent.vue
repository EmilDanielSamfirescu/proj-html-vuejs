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

                            <div class="my-row safety">
                                <div class="img-container">
                                    <img src="../assets/img/w-3.png" alt="">
                                </div>

                                <div class="description-services">
                                    <h4>Safety First</h4>
                                    <p>
                                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repellendus voluptatum quo nulla qui omnis vel quaerat voluptatibus corporis adipisci sapiente!
                                    </p>
                                </div>
                            </div>

                            <div class="my-row col-9 offset-3 play">
                                <div class="img-container">
                                    <img src="../assets/img/w-2.png" alt="">
                                </div>

                                <div class="description-services">
                                    <h4>Play Yards</h4>
                                    <p>
                                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repellendus voluptatum quo nulla qui omnis vel quaerat voluptatibus corporis adipisci sapiente!
                                    </p>
                                </div>
                            </div>

                            <div class="my-row col-6 offset-6 monitor">
                                <div class="img-container">
                                    <img src="../assets/img/w-1.png" alt="">
                                </div>

                                <div class="description-services">
                                    <h4>Monitor Your Pet</h4>
                                    <p>
                                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repellendus voluptatum quo nulla qui omnis vel quaerat voluptatibus corporis adipisci sapiente!
                                    </p>
                                </div>
                            </div>

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

    .left {
        width: calc(100% / 2);

        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .right {
        width: calc(100% / 2);
        margin-top: 50px;
        padding: 20px;
        .upper-title {
                p {
                    margin-bottom: 0;
                    margin-left: 10px;
                    color: $top-header-bg-color;
                }
            }
        
        h2 {
            margin: 40px 0px;
        }

        .reasons-to-choose {
            .safety {
                .img-container {
                width: 250px;
                margin-right: 20px;

                img {
                    width: 100%;
                    display: block
                }
            }

            }

            .play {
                margin-top: 15px;
                margin-bottom: 15px;
                .img-container {
                width: 300px;
                margin-right: 20px;

                img {
                    width: 100%;
                    display: block
                }
            }

            }

            .monitor {
                .img-container {
                width: 140%;
                margin-right: 20px;

                img {
                    width: 100%;
                    display: block
                }
            }

            }
        }
    }
}

.section-customers {
    @include debug-4
}

</style>