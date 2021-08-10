<template>

  <div class="container">

    <div class="container--title-sub">

      <h2 class="title-sub--title">Ciao! Sono Marco Tessitore</h2>

      <span class="title-sub--subtitle">Questo e il mio portfolio</span>

    </div>
    
  </div>

</template>


<script>

export default {

  name: 'Jumbotron'

}

</script>


<style lang="scss" scoped>

  @import '@/style/variabili.scss';
  
  .container {
    width: 100%;
    background:  #232726;
    height: 100vh;

    &:hover{
      background: linear-gradient(-45deg, #333333, #aaaaaa, #494949, #232726);
      background-size: 400% 400%;
      animation: gradient 2s ease;

      @keyframes gradient {
        0% {
          background-position: 0% 50%;
        }
        50% {
          background-position: 100% 50%;
        }
        100% {
          background-position: 0% 50%;
        }
      }
    }  
    .container--title-sub {
      text-align: center;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

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

    }
    
  }


</style>