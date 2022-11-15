<script>
export default {
    name: 'AppFooter',
    data(){
        return {
            dcComics: [
                {
                    text: 'Characters',
                    href: '#'
                },
                {
                    text: 'Comics',
                    href: '#'
                },
                {
                    text: 'Movies',
                    href: '#'
                },
                {
                    text: 'TV',
                    href: '#'
                },
                {
                    text: 'Games',
                    href: '#'
                },
                {
                    text: 'Videos',
                    href: '#'
                },
                {
                    text: 'News',
                    href: '#'
                }
            ],
            shop: [
                {
                    text: 'Shop DC',
                    href: '#'
                },
                {
                    text: 'Shop DC Collectibles',
                    href: '#'
                }
            ],
            dc: [
                {
                    text: 'Terms Of Use',
                    href: '#'
                },
                {
                    text: 'Privacy Policy (new)',
                    href: '#'
                },
                {
                    text: 'Advertising',
                    href: '#'
                },
                {
                    text: 'Job',
                    href: '#'
                },
                {
                    text: 'Subscriptions',
                    href: '#'
                },
                {
                    text: 'Talent Workshops',
                    href: '#'
                },
                {
                    text: 'CPSC Certificates',
                    href: '#'
                },
                {
                    text: 'Ratings',
                    href: '#'
                },
                {
                    text: 'Shop Help',
                    href: '#'
                },
                {
                    text: 'Contact Us',
                    href: '#'
                }
            ],
            sites: [
                {
                    text: 'DC',
                    href: '#'
                },
                {
                    text: 'MAD Magazine',
                    href: '#'
                },
                {
                    text: 'DC Kids',
                    href: '#'
                },
                {
                    text: 'DC Universe',
                    href: '#'
                },
                {
                    text: 'DC Power Visa',
                    href: '#'
                }
            ],
            socials: [
                {
                    src: 'footer-facebook.png',
                    href: '#'
                },
                {
                    src: 'footer-pinterest.png',
                    href: '#'
                },
                {
                    src: 'footer-twitter.png',
                    href: '#'
                },
                {
                    src: 'footer-youtube.png',
                    href: '#'
                },
                {
                    src: 'footer-periscope.png',
                    href: '#'
                }
            ]
        }
    },
    methods: {
        getImgPath(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }
}
</script>

<template>
  <footer>
    <div class="footer-top">
        <div class="container">
            <div class="links">
                <div class="link-1">
                    <h3>dc comics</h3>
                    <nav>
                        <ul>
                            <li
                            v-for="(item, index) in dcComics"
                            :key="index"
                            ><a :href="item.href">{{item.text}}</a></li>
                        </ul>
                    </nav>
                    <div class="shop">
                        <h3>shop</h3>
                        <nav>
                        <ul>
                            <li
                            v-for="(item, index) in shop"
                            :key="index"
                            ><a :href="item.href">{{item.text}}</a></li>
                        </ul>
                        </nav>
                    </div>
                </div>

                 

                <div class="link-2">
                    <h3>DC</h3>
                    <nav>
                        <ul>
                            <li
                            v-for="(item, index) in dc"
                            :key="index"
                            ><a :href="item.href">{{item.text}}</a></li>

                        </ul>
                    </nav>
                </div>
                <div class="link-3">
                    <h3>sites</h3>
                    <nav>
                        <ul>
                            <li
                            v-for="(item, index) in sites"
                            :key="index"
                            ><a :href="item.href">{{item.text}}</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
            <div class="logo deubg">
                <img src="/dc-logo.png" alt="">
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">
            <div class="sign-up">
            <button>sign-up now!</button>
        </div>
        <div class="socials">
            <h2>follow us</h2>
            <ul>
                <li
                v-for="(item, index) in socials"
                :key="index"
                ><a href="#"><img :src="getImgPath(item.src)" alt="{{item.href}}"></a></li>
            </ul>
        </div>
        </div>
    </div>
  </footer>
</template>



<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

    .footer-top{
        height: 375px;
        background-image: url(../assets/img/footer-bg.jpg);
        .container{
            height: 100%;
            display: flex;
            .links{
                width: 50%;
                display: flex;
                margin: 1.5rem 0;
            }
            .link-1, .link-2, .link-3{
                margin-right: 1rem;
            }
            .shop{
                margin-top: 1rem;
            }
            .logo{
                width: 50%;
                overflow: hidden;
                @include centerFlex('both');
                img{
                     width: 90%;
                    transform: rotate(-30deg);
                    opacity: .5;
                }
            }
            h3{
                color: white;
                text-transform: uppercase;
                margin-bottom: .7rem;
            }
            ul{
                list-style: none;
            }
            li{
                margin: .3rem 0;
            }
            a{
                text-decoration: none;
                color: #959595;
                font-size: .8rem;
            }
        }
    }
    .footer-bottom{
        background-color: $footer-btm-color;
        height: 110px;
        .container{
            height: 100%;
            @include centerFlex('vertical');
            justify-content: space-between;
            button{
                text-transform: uppercase;
                font-size: 1.1rem;
                font-weight: 600;
                padding: 1rem;
                color: white;
                background-color: rgba($color: #000000, $alpha: 0);
                border: 2px solid $main-color;
                cursor: pointer;
            }
            .socials{
                display: flex;
                align-items: center;
                h2{
                    color: $main-color;
                    text-transform: uppercase;
                    margin-right: 1rem;
                }
                ul{
                    display: flex;
                    list-style: none;
                    li{
                        margin: 0 .5rem;
                    }
                }
            }

        }
    }
</style>