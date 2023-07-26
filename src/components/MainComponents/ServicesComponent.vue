<script >

export default {
    name: "ServicesComponent",
    data (){
        return {
            service: [
                {
                    title: 'Pet Sitting',
                    image: 'd-1.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.',
                },
                {
                    title: 'Puppy Sitting',
                    image: 'd-2.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.',
                },
                {
                    title: 'Dog Walking',
                    image: 'd-3.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.',
                },
                {
                    title: 'Night Care',
                    image: 'd-4.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.',
                },
                {
                    title: 'Pet Sitting',
                    image: 'd-5.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Assumenda, omnis dolor.',
                },
            ]
        }
    },
    methods: {
        getImagePath: function(image){
                return new URL (image, import.meta.url).href;
            }

    }
};
</script>

<template>
    <!-- SECOND SECTION -->
    <section class="section-services" id="Services">
            <div class="my-container">

                <div class="service-title">
                    <p>Service</p>
                    <h4>
                        DogMilo Pet Care Service <br>
                        For Your Best Friend.
                    </h4>
                </div>

                <div class="my-row justify-content-center">

                    <div class="card-service"
                        v-for="(singleCard, i) in service" :key="i">

                        <div class="img-container">
                            <img :src="getImagePath(`../../assets/img/${singleCard.image}`)" :alt="singleCard.title">
                        </div>

                        <h5>{{singleCard.title}}</h5>
                        <p>{{singleCard.text}}</p>

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
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/mixin.scss" as *;

.section-services {
    background-color: $bg-lightgrey-color;
    padding: 50px 0px;

    &::before {
        content: '';
        display: table;
        background-image: url('../../assets/img/dog-left.png');
        background-size: cover;
        height: 12.5rem;
        width: 12.5rem;
        position: absolute;
        right: 0rem;
        transform: scaleX(-1);
    }


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
        border-radius: 6.25rem;
        padding: 1.25rem .625rem;
        margin: 20px .625rem;
        color: white;
        cursor: pointer;
        box-shadow: .1875rem .1875rem .625rem rgb(137, 137, 137);
        transition: all 0.6s;

        &:hover{
            background-color: $top-header-bg-color;
        }
        .img-container {
            width: 2.5rem;

            img {
                width: 100%;
                display: block;
            }
        }

        h5 {
            margin: .625rem 0rem;
        }
        
        p{
            font-size: 0.9em;
        }

        .arrow-container {
            width: 2.5rem;
            height: 2.5rem;
            font-size: 1.5em;
            background-color: $button-color;
            border-radius: 50%;
            line-height: 40px;
            transition: all 0.6s;

            a {
                list-style: none;
                color: black;
                padding: .625rem;

                &:hover {
                    color: white;
                }
            }
            &:hover {
                background-color: $button-hover-color;

            }
        }
    }
}

</style>