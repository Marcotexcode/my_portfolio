<template>

  <div class="container">

    <div class="container--title-sub">

      <h2 class="title-sub--title">Ciao! Sono Marco Tessitore</h2>

      <span class="title-sub--subtitle">Le mie conoscenze</span>

      <Carousel class="caro"/>
    
    </div>
    
  </div>

</template>


<script>

  import Carousel from '@/components/Carousel.vue';

  export default {

    name: 'Jumbotron',

    components: { 

      Carousel

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

  .caro {
    padding: 0;
  }
      

    }
    
  }

  @media (max-width: 968px) {

    .container {
      padding: 0;
    
    }

  }


</style>