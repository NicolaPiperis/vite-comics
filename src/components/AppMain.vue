<script >
export default {
    name : "AppMain" ,
    data () {
        return {
            buyItems : [
                {
                    img : "../images/buy-comics-digital-comics.png",
                    text : "DIGITAL COMICS"
                },
                {
                    img : "./images/buy-comics-merchandise.png",
                    text : "DC MERCHANDISE"
                },
                {
                    img : "./images/buy-comics-subscriptions.png",
                    text : "SUBSCRIPTION"
                },
                {
                    img : "./images/buy-comics-shop-locator.png",
                    text : "COMIC SHOP LOCATOR"
                },
                {
                    img : "./images/buy-dc-power-visa.svg",
                    text : "DC POWER VISA"
                }
            ]
        }
    }
    
}
</script>

<template>

    <main>

        <section class="empty">

            <div class="content">
                - -&gt;Content goes here&lt;- -
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
    .empty{
        height: 135px;
        background-color: #1c1c1c;

        .content{
            height: 100%;
            font-size: 30px;
            font-weight: 600;
            color: white;
            margin-left: 200px;
            display: flex;
            align-items: center;
        }
    }

    .buy{
        height: 140px;
        background-color: #0282f9;

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
                    width: 50px;
                }

            }
        
        }
    }
   
</style>
