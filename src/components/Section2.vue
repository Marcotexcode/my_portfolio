<template>
  
  <div class="container">

    <h2 class="container--title">Certificazioni</h2>

    <BoxCertificazioni class="box-item" v-for="(link, index) in links" :key="index"  :info="link"/>

  </div>
  
</template>

<script>

    import BoxCertificazioni from '@/components/BoxCertificazioni.vue';
    import ItemCert from '@/data/ItemCert.js';


    export default {

      name: 'Section2',

       data() {

        return {

          links: ItemCert
            
        }

      },

      components: {

        BoxCertificazioni

      }
    
    }
</script>

<style lang="scss" scoped>

  @import '@/style/variabili.scss';


  .container {
    background:  #232726;
    text-align: center;
    padding: 10px;
    width: 100%;

    .container--title {
      margin: 90px 0px;
      text-transform: uppercase;
    }
    .container--box {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }

    .box-item {
      padding: 25px;
      background: $Bordeaux;
      width: 20%;
    }
    
  }

</style>