<script>
export default {
    name: 'AppMain'
}
</script>

<template>
<main>
  <div class="container">
    content
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
    }
</style>