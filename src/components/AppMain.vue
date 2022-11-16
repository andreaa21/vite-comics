<script>

import ComicCard from './ComicCard.vue';
import comicsData from '../data/data';

export default {
    name: 'AppMain',
    components:{
      ComicCard
    },
    data(){
      return {
        comics:comicsData
      }
    }
}
</script>

<template>
<main>
  <div class="container cards">
    <ComicCard 
    v-for="(comic, index) in comics"
    :key="index"
    :img="comic.thumb"
    :text="comic.series"
    />
  </div>
  <div class="btn-container">
    <button>load more</button>
  </div>
</main>
</template>



<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

    main{
        background-color: $main-bg-color;
        color: white;
        min-height: 130px;
        @include centerFlex('vertical');
        flex-direction: column;
        .cards{
          display: flex;
          flex-wrap: wrap;
          padding: 2rem;
          margin-top: 100px;
        }

        .btn-container{
          margin: 2rem 0;
          button{
            background-color: $main-color;
            border: none;
            padding: .5rem 2rem;
            color: white;
            text-transform: uppercase;

          }
        }


    }
</style>