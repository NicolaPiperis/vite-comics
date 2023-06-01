<script >
// import MainContent from './components/MainContent.vue' ;
export default {
    name : "AppMain" ,
   
    data () {
        return {
            buyItems : [
                {
                    img : "images/buy-comics-digital-comics.png",
                    text : "DIGITAL COMICS"
                },
                {
                    img : "images/buy-comics-merchandise.png",
                    text : "DC MERCHANDISE"
                },
                {
                    img : "images/buy-comics-subscriptions.png",
                    text : "SUBSCRIPTION"
                },
                {
                    img : "images/buy-comics-shop-locator.png",
                    text : "COMIC SHOP LOCATOR"
                },
                {
                    img : "images/buy-dc-power-visa.svg",
                    text : "DC POWER VISA"
                }
            ]
        }
    }
    
}
</script>

<template>

    <main>

        <section class="hero">
            <div>
                <strong>CURRENT SERIES</strong>
            </div>
        </section>

        <section class="comics">

            <div class="container-comics">

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

                <div class="card-comic">
                    <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
                    <h4>BATMAN</h4>
                </div>

            </div>

        </section>

        <section class="buy">

            <div class="tools-container">

                <div class="tools" v-for = "item in buyItems">
                    <img :src="item.img" alt="">
                    <h5>{{ item.text }}</h5>
                </div>
               

            </div>

        </section>

    </main>

</template>

<style scoped lang="scss">
    .hero{
        height: 400px;
        background-image: url(../../public/images/jumbotron.jpg);
        position: relative;

        div{
            text-align: center;
            color: white;
            background-color: #0282f9;
            position: absolute;
            padding: 16px;
            width: 200px;
            height: 50px;
            left: 200px;
           bottom: -25px;
        }
    }

    .comics{
        height: 900px;
        background-color: #1c1c1c;

            .container-comics{
                padding: 100px 200px;
                display: flex;
                flex-wrap: wrap;
                gap: 50px;

            .card-comic{
            width: calc((100% / 6) - 50px);

                h4{
                    color: white;
                    text-align: left;
                    padding: 15px 0;
                }
                
            }
        }
    }

    .buy{
        height: 140px;
        background-color: #0282f9;
        position: relative;
        z-index: 99;

        .tools-container{
            margin: 0 200px;
            height: 100%;
            display: flex;
            justify-content: space-around;
            align-items: center;

            .tools{
                display: flex;
                align-items: center;
                gap: 10px;
                color: white;

                img{
                    width: 40px;
                }

            }
        
        }
    }
   
</style>
