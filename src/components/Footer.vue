<template>
  
  <div class="container" id="contact">

    <h2 class="container--title">Contattatemi</h2>

    <div class="contact-icon">
        
        <a class="contact" target="_blank" href="https://www.facebook.com/mtessitore"><i class="fab icon fa-facebook"></i><h2 class="contact-text">Facebook</h2></a>
        <a class="contact" target="_blank" href=""><i class="fab icon fa-twitter"></i><h2 class="contact-text">Twitter</h2></a>
        <a class="contact" target="_blank" href="https://github.com/Marcotexcode"><i class="fab icon fa-github"></i><h2 class="contact-text">GitHub</h2></a>
        <a class="contact" target="_blank" href=""><i class="fas icon fa-envelope"></i><h2 class="contact-text">Mail</h2></a>
        <a class="contact" target="_blank" href=""><i class="fas icon fa-phone"></i><h2 class="contact-text">Phone</h2></a>

        
    </div>
      
  </div>
  
</template>


<script>
  
  
    export default {

        name: 'Footer',

    }
  
</script>


<style lang="scss" scoped>

  @import '@/style/variabili.scss';

    .container {
        
        background: #45567d;
        text-align: center;
        padding: 10px 50px;
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .container--title {
            margin: 90px 0px 10px;
            text-transform: uppercase;
        }

        .contact-icon {
            padding: 30px;
            display: flex;
            justify-content: space-between;

            .contact {
                display: flex;
                justify-content: space-around;
                align-items: center;
                text-decoration: none;

                .icon {
                    font-size: 50px;
                    vertical-align: middle;
                    margin: 0px 20px;
                    color: black;
                }

                .contact-text {
                    color: #000;

                }
            }
        }
    }
 

  @media (max-width: 968px) {

      .container {
        
        background: #45567d;
        text-align: center;
        height: 100vh;
        display: block;

        .container--title {
            margin: 90px 0px 0px;
            text-transform: uppercase;
        }

        .contact-icon {
            padding: 30px;
            display: block;

            .contact {
                display: block;
                text-decoration: none;

                .icon {
                    font-size: 40px;
                    vertical-align: middle;
                    margin: 20px 0px;
                    color: black;
                }

                .contact-text {
                    color: #000;
                    display: none;

                }
            }
        }
    }
    

  }

</style>