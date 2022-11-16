<script>
export default {
    name: 'AppJumbo'
}
</script>


<template>
 <div class="jumbotron">
    <div class="container">
        <button>Current series</button>
    </div>
 </div>
</template>



<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.jumbotron{
    min-height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    .container{
        height: 400px;
        position: relative;
        margin-bottom: -.8rem;
        button{
            position: absolute;
            bottom: 0;
            left: 0;
            background-color: $main-color;
            border: none;
            padding: .5rem 1rem;
            color: white;
            text-transform: uppercase;
            font-weight: 600;
        }
    }
}

</style>