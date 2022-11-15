<script>
export default {
    name: 'AppHeader',
    data(){
        return{
            menu: [
                {
                    text: 'Characters',
                    href: '#',
                    current: false
                },
                {
                    text: 'Comics',
                    href: '#',
                    current: true
                },
                {
                    text: 'movies',
                    href: '#',
                    current: false
                },
                {
                    text: 'tv',
                    href: '#',
                    current: false
                },
                {
                    text: 'games',
                    href: '#',
                    current: false
                },
                {
                    text: 'collectibles',
                    href: '#',
                    current: false
                },
                {
                    text: 'videos',
                    href: '#',
                    current: false
                },
                {
                    text: 'fans',
                    href: '#',
                    current: false
                },
                {
                    text: 'news',
                    href: '#',
                    current: false
                },
                {
                    text: 'shop',
                    href: '#',
                    current: false
                }
            ]
        }
    }
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
                <li
                v-for="(item, index) in menu"
                :key="index"
                :class="{'active': item.current}"
                ><a href='item.href'>{{item.text}}</a></li>
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
                img{
                    width: 80%;
                }
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
                }                    // &:hover{
                    //     color: $main-color;
                    //     border-bottom: 4px solid $main-color;
                    // }
                a{
                    color: $header-link-color;
                    height: 100%;
                    @include centerFlex('vertical');
                    text-decoration: none;
                    text-transform: uppercase;
                    font-size: .8rem;
                    &:hover{
                        color: $main-color;
                        border-bottom: 4px solid $main-color;
                    }
                }
            }
        }
    }
</style>