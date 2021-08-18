<template>
  
    <div class="container">

        <VueSlickCarouse class="cont-caro" v-bind="settings" > 

            <div class="container-box" v-for="(link, index) in linkProg" :key="index">

                <div class="box">

                    <img class="container--image" :src="require(`@/assets/img/${link.img}`)"  :alt="link.title">

                    <h2 class="container--title">{{link.title}}</h2>

                    <p class="container--description">{{link.description}}</p>

                    <h3 class="container--language">Linguaggi: <span>{{link.language}}</span></h3>

                    <a class="container--link" :href="link.link">Link</a>

                </div>

            </div>

        </VueSlickCarouse> 

    </div>
  
</template>

<script>

    import ItemProg from '@/data/ItemProg.js';
    import VueSlickCarouse from 'vue-slick-carousel';
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css';

    export default {

      name: 'BoxItem',

        data() {
            return {

                settings: {

                    "infinite": true,
                    "slidesToShow": 3,
                    "slidesToScroll": 1,
                    "autoplay": true,
                    "arrows": true,
                    "responsive": [
                        
                        {
                            "breakpoint": 968,
                            "settings": {
                                "slidesToShow": 1,
                                "arrows": false,

                            
                            }
                        }
                    ]
                },

                linkProg: ItemProg

            }
        },

        components: {

            VueSlickCarouse

        }
    
    }

</script>


<style lang="scss" scoped>

    @import '@/style/variabili.scss';

    .container {
        
        .container--image {
            width: 100%;
        }

        .container--title {
            margin: 20px 0px;
        }

        .container--image {
            width: 100%;
        }

        .container--description {
            text-align: left;
            margin: 30px 0px;
        }

        .container--language {
            margin: 40px 0px;
        }

        .container--link {
            text-decoration: none;
            background:  #232726;
            color: white;
            padding: 10px 30px;
            box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
        }

        .cont-caro {
            display: flex;
            align-items: center;
            padding: 10px;
            
            .container-box {

                .box {
                    height: 100%;
                    border-radius: 20px;
                    background: $Bordeaux;
                    padding: 20px;
                    margin: 5%;
                }

            }

        }   
        
    }

</style>