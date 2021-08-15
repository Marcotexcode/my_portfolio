<template>

  <div class="container">

    <div class="container--title-sub">

      <h2 class="title-sub--title">Ciao! Sono Marco Tessitore</h2>

      <span class="title-sub--subtitle">Le mie conoscenze</span>

    

    </div>
    
  </div>

</template>


<script>

    

export default {

  name: 'Jumbotron',

 
}

</script>


<style lang="scss" scoped>

  @import '@/style/variabili.scss';
  
  .container {
    width: 100%;
    background:  #232726;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20%;

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

      .card {
        display: flex;
        margin:50px 0px;
        border: 1px solid #000;
        padding: 5px;

        .card--image {
          width: 20%;
          margin: 0px 20px;
          border: 1px solid #000;

        }

      }
      

    }


    .container-slider {
            padding: 50px;
            border: 1px solid #000;
            .container-box--element {
                width: 30%;
                margin: 0 auto;
                display: flex;
                justify-content: center;
                overflow:hidden;
                border: 1px solid #000;

                .element--image {
                    width: 250px;
                    margin-left: 100px;
                }

            }
            
        }
    
  }

  @media (max-width: 968px) {

    .container {
      padding: 0;
    
    }

  }


</style>