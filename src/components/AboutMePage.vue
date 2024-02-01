<template>
    <div class="about-page"> 
        <h2 class="about-page__title">Відгуки</h2>
        <div class="about-page__bg">
        <carousel :items-to-show="1" :autoplay="3000" >
            <slide 
                v-for="slide in sliders" 
                :key="slide.id"
                >
                    <span class="about-page__slide">{{ slide.text }}</span>
            </slide>
            <template #addons>
                <navigation />
                <pagination />
            </template>
        </carousel>    
        </div>    
    </div>
</template>

<script>   
    import 'vue3-carousel/dist/carousel.css'
    import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
    export default {
        name: 'AboutMePage',
        components: {
            Carousel,
            Slide,
            Pagination,
            Navigation,
        },
        data: () => {
            return { 
                sliders: [
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 1
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 2
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 3
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 4
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 5
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 6
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    .about-page {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: #fffff5;
        height: 600px;
        &__title {
            font-family: 'Poppins', sans-serif;
            font-size: 36px;                
            padding-top: 50px;
            text-transform: uppercase;
            margin: 0 auto;
            @media (max-width: 1440px) {
                font-size: 30px;
            }
            @media (max-width: 768px) {
                font-size: 20px;
            }
            @media (max-width: 425px) {
                padding-top: 20px;
            }
        }
        &__slide {
            width: 50%;
            color: darkred;
            font-style: italic;
        }
        &__bg {
            position: relative;
            height: 100%;
            width: 100%;
            &::before {
              content: '';
              position: absolute;
              top: 0;
              left: 0;
              width: 100%;
              height: 100%;
              background-image: url('../assets/images/feed.jpg');
              background-size: contain;
              background-position: center;
              background-repeat: no-repeat;
              opacity: 0.3;
            }
        }
    }
    .carousel {
        width: 100%;
        height: 400px;
        &__viewport {
            width: 100%;
            height: 100%;
            margin: 0 auto;
        }
        &__track {
            width: 100%;
            height: 100%;
        }
        &__pagination-button::after {
            background-color: rgba(247, 236, 222, 1);
        }
        &__pagination-button--active::after {
            background-color: rgba(255, 0, 0, 0.5);
        }
        &__pagination-button:hover::after {
            background-color: rgba(255, 0, 0, 0.5);
        }
        &__icon {
            color: rgba(255, 0, 0, 0.5);
        }
    }
</style>
