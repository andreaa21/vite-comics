<script>
export default {
    name: 'ComponenteAggiuntivo',
    data() {
        return {
            menu: [
                {
                    text: 'Digital Comics',
                    href: '#',
                    src: 'buy-comics-digital-comics.png'
                },
                {
                    text: 'DC Merchandise',
                    href: '#',
                    src: 'buy-comics-merchandise.png'
                },
                {
                    text: 'Subscriptions',
                    href: '#',
                    src: 'buy-comics-subscriptions.png'
                },
                {
                    text: 'Comics Shop Locator',
                    href: '#',
                    src: 'buy-comics-shop-locator.png'
                },
                {
                    text: 'DC Power Visa',
                    href: '#',
                    src: 'buy-dc-power-visa.svg'
                }
            ]
        }
    },
    methods: {
        getImgPath(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }

}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <nav>
                <ul>
                    <li v-for="(item, index) in menu" :key="index">
                        <div class="image">
                            <img :src="getImgPath(item.src)" alt="{{item.text}}">
                        </div>
                        <a :href="item.href">{{ item.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>

</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

.wrapper {
    background-color: $main-color;
    height: 155px;
    color: white;
    @include centerFlex('vertical');

    ul {
        display: flex;
        justify-content: space-between;
        list-style: none;
        padding: 0 .5rem;

        li {
            @include centerFlex('vertical');
            width: calc(100% / 5);
            margin: 0 .5rem;

            .image {
                height: 70px;
                width: 60px;
                margin-right: 1rem;

                img {
                    height: 100%;
                    width: 100%;
                }
            }
        }

        a {
            color: white;
            text-decoration: none;
            text-transform: uppercase;
            font-size: .9rem;
        }
    }
}
</style>