<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
  <header>
    <div class="container">
        <div class="logo">
            <img src="/dc-logo.png" alt="dc-logo">
        </div>

        <nav>
            <ul>
                <li><a href="#">Characters</a></li>
                <li><a class="active" href="#">Comics</a></li>
                <li><a href="#">movies</a></li>
                <li><a href="#">tv</a></li>
                <li><a href="#">games</a></li>
                <li><a href="#">collectibles</a></li>
                <li><a href="#">videos</a></li>
                <li><a href="#">fans</a></li>
                <li><a href="#">news</a></li>
                <li><a href="#">shop</a></li>
            </ul>
        </nav>

    </div>
  </header>
</template>



<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;



    header{
        height: 120px;
        .container{
            height: 100%;
            @include centerFlex('vertical');
            justify-content: space-between;

            .logo{
                padding: 1rem 0;
            }
            nav{
                height: 100%;
                
            }
            ul{
                list-style: none;
                display: flex;
                height: 100%;
                li{
                    margin: 0 .5rem;
                }
                a{
                    color: $header-link-color;
                    height: 100%;
                    @include centerFlex('vertical');
                    text-decoration: none;
                    text-transform: uppercase;
                    font-size: .8rem;
                    &:hover,
                    &.active{
                        color: $main-color;
                        border-bottom: 4px solid $main-color;
                    }
                }
            }
        }
    }
</style>