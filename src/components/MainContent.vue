<script >
export default {
    name : "MainContent" 
}
        
    

</script>

<template>

    <div class="card-comic">
        <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
        <h4>BATMAN</h4>
    </div>

</template>

<style scoped lang="scss">

.card-comic{
    width: calc((100% / 6) - 50px);

    h4{
    color: white;
    text-align: left;
    padding: 15px 0;
    }
                
}
</style>
