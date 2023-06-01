<script >
export default {
    name : "AppHeader" ,
    data () {
        return {
            topics : [
            {
                name : "CHARACTERS" ,
                active : false ,
                href : "#"
            },
            {
                name : "COMICS" ,
                active : true,
                href : "#"
            },
            {
                name : "MOVIES" ,
                active : false ,
                href : "#"
            },
            {
                name : "TV" ,
                active : false , 
                href : "#"
            },
            {
                name : "GAMES" ,
                active : false ,
                href : "#"
            },
            {
                name : "COLLECTIBLES" ,
                active : false ,
                href : "#"
            },
            {
                name : "VIDEOS" ,
                active : false ,
                href : "#"
            },
            {
                name : "FANS" ,
                active : false ,
                href : "#"
            },
            {
                name : "NEWS" ,
                active : false ,
                href : "#"
            },
            {
                name : "SHOP" ,
                active : false ,
                href : "#"
            }
        ]
        }
        
    }
}
</script>

<template>

    <header>
        <div class="container-img">
            <img src="images/dc-logo.png" alt="">
        </div>

        <ul>
            <li v-for = " topic in topics">
                <a :href="topic.href">{{ topic.name }}</a>
            </li>
        </ul>
    </header>

</template>

<style scoped lang="scss">

    header{
        height: 135px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .container-img{
            margin-left: 200px;
        }

        ul{
            height: 100%;
            margin-right: 200px;
            display: flex;
            gap: 50px;
            list-style: none;

            li{
                height: 100%;
                display: flex;
                align-items: center;
            }

            li a {
                text-decoration: none;
                color: #292929;
                font-weight: 600;
                font-size: 15px;
            }

            li:hover{
                border-bottom: 6px solid #0282f9;
            }
            
            li:hover a {
                color: #0282f9;
            }
        }
    }
</style>
