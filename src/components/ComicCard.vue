
<script>



export default {
    name: 'ComicCard',
    props:{
        img: String,
        text: String
    }
}
</script>

<template>
    <div class="card">
        <div class="card-img">
            <img :src="img" :alt="text">
        </div>
        <div class="card-text">{{text}}</div>
    </div>
  
</template>



<style lang="scss" scoped>
    .card{
        width: calc(100% / 6);
        min-height: 300px;
        padding: 1rem;
        .card-text{
            text-align: center;
            margin-top: 1rem;
        }
    }
</style>