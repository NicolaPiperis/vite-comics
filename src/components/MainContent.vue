<script >
export default {
    name : "MainContent",
    props: {
        details: Object
    }
}
        
    

</script>

<template>

    <div class="card-comic">
        <img :src="details.thumb" :alt="details.type">
        <div>{{ details.series }}</div>
    </div>

</template>

<style scoped lang="scss">

.card-comic{
    width: calc((100% / 6) - 50px);

    div{
    color: white;
    text-align: left;
    padding: 15px 0;
    }
                
}
</style>
