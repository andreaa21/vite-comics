
<script>
export default {
    name: 'ComicCard'

}
</script>

<template>
    <div class="card debug">
        <div class="card-img">

        </div>
        <div class="card-text">card</div>
    </div>
  
</template>



<style lang="scss" scoped>
    .card{
        width: calc(100% / 6);
        min-height: 300px;
        padding: 1rem;
        .card-text{
            text-align: center;
        }
    }
</style>