<script >

export default {
    name: "BlogComponent",
    data (){
        return {
            courrentCard: 0,
            courrentCardSecond: 1,
            userReview: [
                {
                    image: '../../assets/img/t1.png',
                    name:'Tobias May',
                    roleJob: 'UI/UX Designer',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'Great Place',
                    vote: '10'
                },
                {
                    image: '../../assets/img/wayne-barnett.jpg',
                    name:'Wayne Barnett',
                    roleJob: 'Founder & CEO',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'Beo ciò!',
                    vote: '8'
                },
                {
                    image: '../../assets/img/angela-caroll.jpg',
                    name:'Angela Caroll',
                    roleJob: 'Chief Editor',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'El me can xe sta ben!',
                    vote: '10'
                },
                {
                    image: '../../assets/img/walter-gordon.jpg',
                    name:'Walter Gordon',
                    roleJob: 'Office Manager',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'Bello ma non troppo',
                    vote: '6'
                },
                {
                    image: '../../assets/img/angela-lopez.jpg',
                    name:'Angela Lopez',
                    roleJob: 'Social Media Manager',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'Non mi è piaciuto',
                    vote: '4'
                },
                {
                    image: '../../assets/img/barbara-ramos.jpg',
                    name:'Barbara Ramos',
                    roleJob: 'Graphic Designer',
                    text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, esse labore odio corrupti error molestiae nemo quis natus recusandae numquam cum facere quibusdam debitis sunt',
                    title: 'Oi ndemo a vedere i pinfloi!',
                    vote: '2'
                },
            ]
        }
    },
methods: {
    getImagePath: function(image){
                return new URL (image, import.meta.url).href;
    },
    // nextButton (){
    //     // console.log(`ciaone a dopo`);
    //     if (this.courrentCard == this.userReview.length - 1 ){
    //         this.courrentCard = 0;
            
    //     } else {
    //         this.courrentCard++;
            

    //     }
    // },
    // prevButton (){
    //     // console.log(`ciao a prima`);
    //     if (this.courrentCard == 0 ){
    //         this.courrentCard = this.userReview.length - 1;
            
    //     } else {
    //         this.courrentCard--;
            
    //     }
    // },
    nextButtonSecond (){
        // console.log(`ciaone a dopo`);
        if (this.courrentCardSecond == this.userReview.length - 1){
            this.courrentCardSecond = 1;
            
        } else {
            this.courrentCardSecond++;
            

        }
    },
    prevButtonSecond (){
        // console.log(`ciao a prima`);
        if (this.courrentCardSecond == 1 ){
            this.courrentCardSecond = this.userReview.length - 1;
            
        } else {
            this.courrentCardSecond--;
            
        }
    },
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
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                        </div>
                        
                    </div>

                    <div class="my-card">

                        <template v-for="(user, i) in userReview" :key="i">
                            <div class="customer-card" v-if="i == courrentCard">

                                <div class="stars">
                                    <span v-for="numero in Math.ceil(user.vote / 2)" :key="numero"><i class="fa-solid fa-star"></i></span>
                                    <span v-for="numero in (5 - (Math.ceil(user.vote / 2)))" :key="numero"><i class="fa-regular fa-star"></i></span>
                                </div>

                                <h5>{{user.title}}</h5>

                                <p>{{user.text}}</p>

                                <div class="customer-info">

                                    <div class="customer-img">
                                        <img :src="getImagePath(user.image)" alt="customer">
                                    </div>

                                    <div class="customer-name">
                                        <h6>{{user.name}}</h6>
                                        <p>{{user.roleJob}}</p>
                                    </div>

                                </div>
                            </div>
                        </template>
                        
                    </div>

                    <div class="my-card">

                        <template v-for="(user, index) in userReview" :key="index">
                            <div class="customer-card" v-if="index == courrentCardSecond">

                                <div class="stars">
                                    <span v-for="numero in Math.ceil(user.vote / 2)" :key="numero"><i class="fa-solid fa-star"></i></span>
                                    <span v-for="numero in (5 - (Math.ceil(user.vote / 2)))" :key="numero"><i class="fa-regular fa-star"></i></span>
                                </div>

                                <h5>{{user.title}}</h5>

                                <p>{{user.text}}</p>

                                <div class="customer-info">

                                    <div class="customer-img">
                                        <img :src="getImagePath(user.image)" alt="customer">
                                    </div>
                                    
                                    <div class="customer-name">
                                        <h6>{{user.name}}</h6>
                                        <p>{{user.roleJob}}</p>
                                    </div>

                                </div>
                            </div>
                        </template>

                        <div class="arrows">
                            <i @click="prevButtonSecond()" class="fa-solid fa-chevron-left"></i>
                            <i @click="nextButtonSecond()" class="fa-solid fa-chevron-right"></i>
                        </div>
                        
                    </div>

                    <!-- <div class="my-card">

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
                        
                    </div> -->

                    <!-- <div class="my-card last-card">

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
                    </div> -->

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
            margin: 4.375rem .3125rem 7.5rem .3125rem;
            position: relative;
            .stars{
                text-align: start;
                i {
                    color: #FFD608;
                }
                }
        
            .review-card{
                padding: 15px;
                text-align: center;
                

                p{
                    font-size: 0.8em;
                }

                h4 {
                    margin: 1.25rem 0rem;
                }
                .card-title {
                    .img-container {
                        width: 30px;
                        height: 30px;
                        img {
                            width: 100%;
                            display: block;
                        }
                    }
                    h6 {
                        margin-left: .9375rem;
                        font-size: 0.8em;
                        color: $top-header-bg-color;
                    }
                }
            }

            .customer-card {
                background-color: $bg-lightgrey-color;
                padding: .9375rem;
                h5 {
                margin: .625rem 0rem;
            }

            p{
                font-size: 1em;
                margin-bottom: 1.25rem;
            }
            .customer-info {
                .customer-img {
                    width: 3.125rem;
                    height: 3.125rem;
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
                    margin-left: 1.25rem;
                    vertical-align: middle;

                    h6{
                        margin-bottom: .125rem;
                    }

                    p{
                        font-size: 0.8em;
                        margin: 0;
                        color: #878787;
                    }
                }
            }
            }

            .arrows{
            position: absolute;
            right: 0px;
            bottom: -45px;
            i {
                padding: .3125rem .5rem;
                font-size: 1.5em;
                background-color: $orange-main-color;
                color: white;
                margin-left: .3125rem;

                &:hover{
                    background-color: $top-header-bg-color;
                    cursor: pointer;
                }
            }

        }
        }
    }

    // .last-card {
    //     position: relative;
    //     .arrows{
    //         position: absolute;
    //         right: 0px;
    //         bottom: -45px;
    //         i {
    //             padding: 5px 8px;
    //             font-size: 1.5em;
    //             background-color: $orange-main-color;
    //             color: white;
    //             margin-left: 5px;

    //             &:hover{
    //                 background-color: $top-header-bg-color;
    //                 cursor: pointer;
    //             }
    //         }

    //     }
    // }


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
            margin-right: 3.75rem;
        }

        .dog-img-container {
            width: 15.625rem;
            position:absolute;
            top: -3.6875rem;

            img {
                width: 100%;
            }
        }
        .newsletter {
            margin-top: 1.5625rem;
            .e-mail {
            position: relative;
            display:inline-block;
            width:50%; 
                
                input[type="email"] { 
                    width: 100%; 
                    height: 2.5rem; 
                    } 
                .fa-at { 
                    position: absolute;
                    right: 2px;
                    top:50%;
                    transform: translateY(-50%); 
                    padding: .625rem;
                    background-color: $orange-main-color;
                    color: white;
                    }
        }
        }
    }


}

</style>