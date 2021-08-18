<template>
  
  <div class="container" id="certificazioni">

    <h2 class="container--title">Certificazioni</h2>

    <BoxCertificazioni class="box-item" />

  </div>
  
</template>


<script>

  import BoxCertificazioni from '@/components/BoxCertificazioni.vue';

  export default {

    name: 'Section2',

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
    padding: 10px 50px;
    width: 100%;

    .container--title {
      margin: 90px 0px 10px;
      text-transform: uppercase;
    }
  
  }

  @media (max-width: 968px) {

      .container {
        padding: 10px 15px;

        .container--title {
          margin: 90px 0px 0px;

        }

      }

  }

</style>