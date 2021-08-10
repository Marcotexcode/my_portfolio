<template>
  
  <div class="container">

    <h2 class="container--title">Porogetti</h2>
    
    <div class="container--box">
      
      <BoxItem class="box-item" v-for="(link, index) in links" :key="index"  :info="link"/>

    </div>

  </div>
  
</template>

<script>

    import ItemProg from '@/data/ItemProg.js';
    import BoxItem from '@/components/BoxItem.vue';

    export default {

      name: 'Section1',

      data() {

        return {

          links: ItemProg
            
        }

      },

      components: {

        BoxItem

      }
    
    }
</script>

<style lang="scss" scoped>

  @import '@/style/variabili.scss';


  .container {
    background: #45567d;
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
      justify-content: center;
    }

    .box-item {
      padding: 25px;
      background: $Bordeaux;
      width: 20%;
    }
    
  }

</style>