<template>

  <div class="container" id="app">

    <Header/>

    <Jumbotron/> 
    
    <Main/>

    <Footer/>

  </div>

</template>


<script>

  import Header from '@/components/Header.vue'
  import Jumbotron from '@/components/Jumbotron.vue'
  import Main from '@/components/Main.vue'
  import Footer from '@/components/Footer.vue'
  import '@fortawesome/fontawesome-free/js/all.js'
  import '@fortawesome/fontawesome-free/css/all.css'




  export default {

    name: 'App',

      components: {

      Header,

      Jumbotron,

      Main,

      Footer

      }

  }

</script>


<style lang="scss">
  @import '@/style/commons.scss';
  

</style>
