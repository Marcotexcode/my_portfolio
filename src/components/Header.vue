<template>

    <div class="container">

        <h1 class="container--title">Marco Tessitore</h1>
        <h1 class="container--title-mobile">M. T.</h1>
        
        <ul class="container--menu" :class="{active: isActive}">

            <li class="container--menu--list" @click="myFilter"><a class="container--menu--list--link" href="#about">Home</a></li>
            <li class="container--menu--list" @click="myFilter"><a class="container--menu--list--link" href="#work">Progetti</a></li>
            <li class="container--menu--list" @click="myFilter"><a class="container--menu--list--link" href="#certificazioni">Certificazioni</a></li>
            <li class="container--menu--list" @click="myFilter"><a class="container--menu--list--link" href="#contact">Contatti</a></li>

        </ul>

        <div class="container--burgher-menu" @click="myFilter">
            <div class="line1"></div>
            <div class="line2"></div>
            <div class="line3"></div>
        </div>

    </div>

</template>


<script>

export default {

    name: 'Header',

    data() {
        
        return {
        
            isActive: false

        }
    
    },

    methods: {

        myFilter: function() {

            this.isActive = !this.isActive;

        }

    }

}

</script>


<style lang="scss" scoped>

    @import '@/style/variabili.scss';

    .container {
        z-index: 10;
        width: 100%;
        display: flex;
        justify-content: space-between;
        padding: 20px;
        background: $Bordeaux;
        align-items: center;
        position: fixed;

        .container--title {
            color: $White;
            font-weight: 400;
        }

        .container--title-mobile {
            display: none;
        }

        .container--menu {
            display: flex;
            list-style: none;
            text-decoration: none;

            .container--menu--list {
                margin: 10px 60px;
                transition: 0.6s ease-out;

                &:hover {
                    transition: 0.6s ease-out;
                    transform: scale(2);
                }
                .container--menu--list--link {
                    text-decoration: none;
                    color: $White;
                }
            }
        }

        .container--burgher-menu {
            display: none;
        }

        .container--burgher-menu div {
            width: 25px;
            height: 3px;
            background-color: #fff;
            margin: 5px;
            
        }
        
    }


    @media (max-width: 968px) {

        .container {
            display: flex;

            .container--title{
                display: none;
                
            }

            .container--title-mobile {
                color: $White;
                font-weight: 400;
                display: block;

            }

            .container--menu {
                position: absolute;
                right: 0px;
                height: 100vh;
                top: 79px;
                background: $Bordeaux;
                flex-direction: column;
                text-align: center;
                width: 100%;
                display: none;
            }

            // trovare un modo in cui al click dell burgher il trasform di container--menu diventa 0% perche e 
            // 100% scompare e per farlo comparire devo mettere 0%

            .active {
                display: flex;
                

            }

            .container--burgher-menu {
                display: block;
                margin: 0px 30px;

            }

        }


    }


</style>