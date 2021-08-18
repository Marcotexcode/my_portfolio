<template>
  
  <div class="container" id="work">

    <h2 class="container--title">Porogetti</h2>
      
    <BoxItem class="box-item" />

  </div>
  
</template>


<script>
  
  import BoxItem from '@/components/BoxItem.vue';
  
  export default {

    name: 'Section1',

    components: {

      BoxItem,

    }
  
  }
  
</script>


<style lang="scss" scoped>

  @import '@/style/variabili.scss';


  .container {
    background: #45567d;
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