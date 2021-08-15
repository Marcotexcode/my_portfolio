
<template>

    <div class="container">

        <VueSlickCarousel class="container-carousel" v-bind="settings">

            <div   v-for="(link, index) in links" :key="index"  :info="link">

                <img class="image" :src="require(`@/assets/img/${link.img}`)"  alt="">

            </div>

        </VueSlickCarousel>

    </div>

</template>


<script>

    import VueSlickCarousel from 'vue-slick-carousel'
    import 'vue-slick-carousel/dist/vue-slick-carousel.css'
    import ItemConoscenze from '@/data/ItemConoscenze.js';

    export default {
        name: 'Carousel',

        components: { VueSlickCarousel },

        data() {

            return{

                settings: {

                    "arrows": false,
                    "dots": false,
                    "infinite": true,
                    "slidesToShow": 3,
                    "slidesToScroll": 1,
                    "autoplay": true,
                    "speed": 2000,
                    "autoplaySpeed": 2000,
                    "cssEase": "linear"
                    
                },

                links: ItemConoscenze

            }
        }
    }

</script>

<style scoped lang="scss">

    .container {

        .image{
            width: 100%;
            height: 250px;
            margin: 20px;
        }
       
    }

</style>
