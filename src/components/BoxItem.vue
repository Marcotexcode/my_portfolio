<template>
  
    <div class="container">

        <img class="container--image" :src="require(`@/assets/img/${info.img}.jpg`)"  :alt="info.title">

        <h2 class="container--title">{{info.title}}</h2>

        <p class="container--description">{{info.description}}</p>

        <h3 class="container--language">Linguaggi: <span>{{info.language}}</span></h3>

        <a class="container--link" :href="info.link">Link</a>

    </div>
  
</template>

<script>

    export default {

      name: 'BoxItem',

      props: {

        info: Object

      }
    
    }

</script>

<style lang="scss" scoped>

    .container {
        border-radius: 10px;
        width: 20%;
        margin: 10px;
        
        .container--image {
            width: 100%;
        }

        .container--title {
            margin: 20px 0px;
        }

        .container--image {
            width: 100%;
        }

        .container--description {
            text-align: left;
            margin: 30px 0px;
        }

        .container--language {
            margin: 40px 0px;
        }

        .container--link {
            text-decoration: none;
            background:  #232726;
            color: white;
            padding: 10px 30px;
            box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

        }
        
    }

</style>