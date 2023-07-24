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
            <div class="my-container">

                <div class="service-title">
                    <p>Service</p>
                    <h4>
                        DogMilo Pet Care Service <br>
                        For Your Best Friend.
                    </h4>
                </div>

                <div class="my-row justify-content-center">

                    <div class="card-service">

                        <div class="img-container">
                            <img src="../assets/img/d-1.png" alt="dog-icon">
                        </div>

                        <h5>Puppy Sitting</h5>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.</p>

                        <div class="arrow-container">
                            <a href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                            </a>
                        </div>

                    </div>

                    <div class="card-service">

                        <div class="img-container">
                            <img src="../assets/img/d-2.png" alt="dog-icon">
                        </div>

                        <h5>Dog Walking</h5>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.</p>

                        <div class="arrow-container">
                            <a href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                            </a>
                        </div>

                    </div>

                    <div class="card-service">

                        <div class="img-container">
                            <img src="../assets/img/d-3.png" alt="dog-icon">
                        </div>

                        <h5>Night Care</h5>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.</p>

                        <div class="arrow-container">
                            <a href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                            </a>
                        </div>

                    </div>

                    <div class="card-service">

                        <div class="img-container">
                            <img src="../assets/img/d-4.png" alt="dog-icon">
                        </div>

                        <h5>Pet Sitting</h5>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.</p>

                        <div class="arrow-container">
                            <a href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                            </a>
                        </div>

                    </div>

                    <div class="card-service">

                        <div class="img-container">
                            <img src="../assets/img/d-5.png" alt="dog-icon">
                        </div>

                        <h5>Pet Sitting</h5>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.</p>

                        <div class="arrow-container">
                            <a href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                            </a>
                        </div>

                    </div>


                </div>

            </div>
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

                            <div class="my-row col-10 offset-2 play">
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

                            <div class="my-row col-8 offset-4 monitor">
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
    background-color: $bg-lightgrey-color;
    padding: 50px 0px;

    .service-title {
        text-align: center;

        p{
            color: $top-header-bg-color;
        }
    }

    .card-service {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: $orange-main-color;
        width: calc(100% / 6);
        text-align: center;
        border-radius: 100px;
        padding: 20px 10px;
        margin: 20px 10px;
        color: white;
        .img-container {
            width: 40px;

            img {
                width: 100%;
                display: block;
            }
        }

        h5 {
            margin: 10px 0px;
        }

        p{
            font-size: 0.9em;
        }

        .arrow-container {
            width: 40px;
            height: 40px;
            font-size: 1.5em;
            background-color: $button-color;
            border-radius: 50%;
            line-height: 40px;

            a {
                list-style: none;
                color: black;
                padding: 10px;

            }

            &:hover {
                background-color: $button-hover-color;
                
                a{
                    color: white;
                }
            }
        }
    }
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
            margin-top: 20px;
            margin-bottom: 40px;
        }

        p {
            font-size: 14px;
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
                width: 80%;
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