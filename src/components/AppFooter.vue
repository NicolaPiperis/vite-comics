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
        height: 390px;
        background-image: url("../../public/images/footer-bg.jpg")
    }

    #contacts{
        height: 120px;
        background-color: #303030;
        display: flex;
        justify-content: space-between;
        align-items: center;

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
