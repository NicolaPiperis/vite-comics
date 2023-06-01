<script >
export default {
    name : "AppFooter" ,
    data () {
        return {
            socials : ["images/footer-facebook.png", "images/footer-twitter.png", "images/footer-youtube.png", "images/footer-pinterest.png", "images/footer-periscope.png"]
        }
    }
    
}
</script>

<template>

    <footer>

        <section id="info">

            <div class="info-container">
                
                <div class="info-list">

                    <h3>DC COMICS</h3>
                    <ul>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>

                    <h3>SHOP</h3>
                    <ul>
                        <li>Shop DC</li>
                        <li>Shop DC collectibles</li>
                    </ul>

                </div>

                <div class="info-list">

                    <h3>DC</h3>
                    <ul>
                        <li>Terms of use</li>
                        <li>Privicy policy (New)</li>
                        <li>Ad choices</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscription</li>
                        <li>Talent workshop</li>
                        <li>CPSC Certificates</li>
                        <li>Ratings</li>
                        <li>Shop help</li>
                        <li>Contact us</li>
                    </ul>

                    
                </div>

                <div class="info-list">

                    <h3>SITIES</h3>
                    <ul>
                        <li>DC</li>
                        <li>MAD magazine</li>
                        <li>DC Kids</li>
                        <li>TV</li>
                        <li>DC Universe</li>
                        <li>DC Power visa</li>
                    </ul>

                    
                </div>

            </div>

            <div class="big-logo">
                <img src="../../public/images/dc-logo-bg.png" alt="">
            </div>

        </section>

        <section id="contacts">

            <div class="register">
                <a href="#">
                    <strong>SING-UP NOW!</strong>
                </a>
            </div>

            <div class="socials">

                <h3>FOLLOW US</h3>

                <div class="social-icons">
                    <img v-for = "(social, index) in socials" :key="index" :src="social" alt="">
                </div>
            </div>

        </section>

    </footer>

</template>

<style scoped lang="scss">

    #info{
        display: flex;
        justify-content: space-between;
        height: 390px;
        background-image: url("../../public/images/footer-bg.jpg");
        position: relative;

        .info-container{
            padding: 50px 0 50px 200px;
            display: flex;
            gap: 30px;
            
            h3{
                color: white;
                margin-bottom: 10px;
            }

            ul{
                color: rgba(255, 255, 255, 0.63);
                font-size: 11px;
                line-height: 200%;
                margin-bottom: 20px;

                li{
                    cursor: pointer;
                }
            }
        }

        .big-logo{
            margin-right: 200px;
            position: absolute;
            right: 0;
            top: -100px;
            z-index: 0;
        }
    }

    #contacts{
        height: 120px;
        background-color: #303030;
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: relative;
        z-index: 99;

        .register{
            margin-left: 200px;
            border: 3px solid #0282f9;
            padding: 16px;
            cursor: pointer;

            a{
                color: white;
                font-size: 18px;
            }
        }

        .socials{
            margin-right: 200px;
            display: flex;
            align-items: center;

            h3{
                color: #0282f9;
                margin-right: 20px;
            }

            .social-icons{
                display: flex;
                gap: 20px;

                img{
                    cursor: pointer;
                }
            }
        }
    }
   
</style>
