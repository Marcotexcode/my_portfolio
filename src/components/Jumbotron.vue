<template>

  <div class="container" id="about">

    <div class="container--title-sub">

      <h2 class="title-sub--title">Ciao! Questo  e il mio portfolio</h2>

      <span class="title-sub--subtitle">Le mie conoscenze</span>

      <CarouselJumbo class="carousel"/>
    
    </div>
    
  </div>

</template>


<script>

  import CarouselJumbo from '@/components/CarouselJumbo.vue';

  export default {

    name: 'Jumbotron',

    components: { 

      CarouselJumbo

    },

  }

</script>


<style lang="scss" scoped>

  @import '@/style/variabili.scss';
  
  .container {
    width: 100%;
    background:  #232726;
    height: 100vh;
    align-items: center;
    justify-content: center;
    padding: 20%;

    
    .container--title-sub {
      text-align: center;
      

      .title-sub--title {
        color: $White;
        text-transform: uppercase;
        font-size: 40px;
        margin-bottom: 20px;
      }

      .title-sub--subtitle{
        color: $Bordeaux;
        font-size: 30px;
       
      }

      .carousel {
        padding: 70px;
      }
      

    }
    
  }

  @media (max-width: 968px) {

    .container {
      padding: 0px;

      .container--title-sub {
        padding-top: 100px;

        .carousel {
          padding: 70px 0px;

        }

      }
    
    }

  }


</style>