
<template>
  
    <div class="container">

        <img class="container--image" :src="require(`@/assets/img/${info.img}.png`)"  alt="">
        
        <h2 class="container--title">{{info.title}}</h2>

        <p class="container--description">{{info.description}}</p>

        <a class="container--link" :href="info.link">Link</a>

    </div>

</template>



<script>

export default {

    name: 'BoxCertificazioni',

    props: {

        info: Array

    }

}

</script>


<style lang="scss" scoped>

    .container {
        border-radius: 10px;
        width: 20%;
        margin: 10px;

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

        .container--link {
            text-decoration: none;
            background:  #232726;
            color: white;
            padding: 10px 30px;
            box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

        }

    }

</style>