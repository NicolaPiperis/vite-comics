<script >
import MainContent from './MainContent.vue' ;
export default {
    name : "AppMain" ,
    components: {
    MainContent
    },
   
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
            ],
            comicsInfo : [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
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

                <MainContent v-for = "(comic, index) in comicsInfo" :key="index" :details="comic"/>

            </div>

            <div class="more">
                <strong>LOAD MORE</strong>
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
        background-size: cover;
        background-repeat: no-repeat;
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
        height: 1100px;
        background-color: #1c1c1c;

            .container-comics{
                padding: 100px 200px;
                display: flex;
                flex-wrap: wrap;
                gap: 50px;

        }

        .more{
            text-align: center;
            background-color: #0282f9;
            color: white;
            padding: 15px;
            width: 200px;
            cursor: pointer;
            margin: auto;
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
