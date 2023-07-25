<script >

export default {
    name: "TrainingComponent",
    data (){
        return {

        }
    },
methods: {

}
};
</script>

<template>
    <!-- THIRD SECTION -->
    <section class="section-why-us" id="Training">
            
            <div class="my-row">

                <div class="left">
                    <img src="../../assets/img/why.png" alt="">
                </div>

                <div class="right">
                    <div class="upper-title d-flex align-items-center">
                        <div>
                            <img src="../../assets/img/dog-icon.png" alt="dog-icon">
                        </div>
                        <p>Choose us</p>
                    </div>

                    <h2>Why Choose Us?</h2>

                    <div class="reasons-to-choose">

                        <div class="my-row safety">
                            <div class="img-container">
                                <img src="../../assets/img/w-3.png" alt="">
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
                                <img src="../../assets/img/w-2.png" alt="">
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
                                <img src="../../assets/img/w-1.png" alt="">
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
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

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
            flex-grow: 0;
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
            flex-grow: 0;
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
            flex-grow: 0;
            width: 300px;
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

</style>