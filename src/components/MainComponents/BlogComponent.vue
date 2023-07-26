<script >

export default {
    name: "BlogComponent",
    data (){
        return {

        }
    },
methods: {

}
};
</script>

<template>
    <!-- FOURF SECTION -->
    <section class="section-customers" id="Blogs">
            <div class="my-container">

                <div class="my-row jusftify-content-between">

                    <div class="my-card">

                        <div class="review-card">

                            <div class="card-title d-flex align-items-center">
                                <div class="img-container">
                                    <img src="../../assets/img/dog-icon.png" alt="">
                                </div>
                                <h6>Review & Rating</h6>
                            </div>

                            <h4>Over 8000Customers With 5 Star Review</h4>
                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Earum velit amet enim. Quod commodi hic quidem, numquam odit quas laborum nobis laudantium optio enim. Debitis.</p>
                            <div class="stars">
                                ⭐️⭐️⭐️⭐️⭐️
                            </div>
                        </div>
                        
                    </div>

                    <div class="my-card">

                        <div class="customer-card">
                            <div class="stars">
                                ⭐️⭐️⭐️⭐️⭐️
                            </div>

                            <h5>Great Place</h5>

                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt.</p>

                            <div class="customer-info">

                                <div class="customer-img">
                                    <img src="../../assets/img/t1.png" alt="customer">
                                </div>
                                <div class="customer-name">
                                    <h6>Tobias May</h6>
                                    <p>UI/UX Designer</p>
                                </div>

                            </div>
                        </div>
                        
                    </div>

                    <div class="my-card last-card">

                        <div class="customer-card">
                            <div class="stars">
                                ⭐️⭐️⭐️⭐️⭐️
                            </div>

                            <h5>Great Place</h5>

                            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt.</p>

                            <div class="customer-info">

                                <div class="customer-img">
                                    <img src="../../assets/img/t1.png" alt="customer">
                                </div>
                                <div class="customer-name">
                                    <h6>Tobias May</h6>
                                    <p>UI/UX Designer</p>
                                </div>

                            </div>
                        </div>
                        
                        <div class="arrows">
                            <i class="fa-solid fa-chevron-left"></i>
                            <i class="fa-solid fa-chevron-right"></i>
                        </div>
                    </div>

                </div>
                


                <div class="subscribe-container">

                    <div class="dog-img-container">
                        <img src="../../assets/img/news.png" alt="dogs">
                    </div>

                    <div>
                        <h4>Subscribe To Our News Letter</h4>

                        <div class="newsletter">

                            <div class="e-mail">

                                <form>
                                    <input 
                                    type="email" 
                                    placeholder="Your Email Here">
                                        <i class="fa-solid fa-at"></i>
                                </form>

                            </div>

                        </div>
                    </div>

                </div>

            </div>
        </section>
        <!-- FOURF SECTION -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.section-customers {
    background: rgb(0,0,0);
    background: linear-gradient(360deg, rgba(0,0,0,1) 13%, rgba(255,255,255,1) 13%);
    .my-row {
        .my-card {
        width: calc(100% / 3);
        margin: 70px 5px 120px 5px;
        
        .review-card{
            padding: 15px;
            text-align: center;
            .stars{
                text-align: start;
            }

            p{
                font-size: 0.8em;
            }

            h4 {
                margin: 20px 0px;
            }
            .card-title {
                .img-container {
                    width: 30px;
                    img {
                        width: 100%;
                    }
                }
                h6 {
                    margin-left: 15px;
                    font-size: 0.8em;
                    color: $top-header-bg-color;
                }
            }
        }

        .customer-card {
            background-color: $bg-lightgrey-color;
            padding: 15px;
            h5 {
            margin: 10px 0px;
        }

        p{
            font-size: 1em;
            margin-bottom: 20px;
        }
        .customer-info {
            .customer-img {
                width: 50px;
                border-radius: 50%;
                overflow: hidden;
                display: inline-block;
                vertical-align: middle;
        
                img {
                    width: 100%;
                }
            }

            .customer-name {
                display: inline-block;
                margin-left: 20px;
                vertical-align: middle;

                p{
                    font-size: 0.6em;
                    margin: 0;
                }
            }
        }
        }
        }
    }

    .last-card {
        position: relative;
        .arrows{
            position: absolute;
            right: 0px;
            bottom: -45px;
            i {
                padding: 5px 8px;
                font-size: 1.5em;
                background-color: $orange-main-color;
                color: white;
                margin-left: 5px;

                &:hover{
                    background-color: $top-header-bg-color;
                    cursor: pointer;
                }
            }

        }
    }


    .subscribe-container {

        background-color: $orange-main-color;
        text-align: end;
        padding: 35px;
        width: 70%;
        position: relative;
        color: white;
        margin: auto;

        h4{
            font-size: 1.2em;
            margin-right: 60px;
        }

        .dog-img-container {
            width: 250px;
            position:absolute;
            top: -59px;

            img {
                width: 100%;
            }
        }
        .newsletter {
            margin-top: 25px;
            .e-mail {
            position: relative;
            display:inline-block;
            width:50%; 
                
                input[type="email"] { 
                    width: 100%; 
                    height: 40px; 
                    } 
                .fa-at { 
                    position: absolute;
                    right: 2px;
                    top:50%;
                    transform: translateY(-50%); 
                    padding: 10px;
                    background-color: $orange-main-color;
                    color: white;
                    }
        }
        }
    }


}

</style>