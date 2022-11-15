<script>
export default {
    name: 'AppFooter'
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
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                        </ul>
                    </nav>
                    <div class="shop">
                        <h3>shop</h3>
                        <nav>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                        </nav>
                    </div>
                </div>

                 

                <div class="link-2">
                    <h3>DC</h3>
                    <nav>
                        <ul>
                            <li><a href="#">Terms Of Use</a></li>
                            <li><a href="#">Privacy Policy (new)</a></li>
                            <li><a href="#">Ad choices</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Job</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Certificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="#">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                        </ul>
                    </nav>
                </div>
                <div class="link-3">
                    <h3>sites</h3>
                    <nav>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>

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
                <li><a href="#"><img src="../assets/img/footer-facebook.png" alt=""></a></li>
                <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
                <li><a href="#"><img src="../assets/img/footer-twitter.png" alt=""></a></li>
                <li><a href="#"><img src="../assets/img/footer-youtube.png" alt=""></a></li>
                <li><a href="#"><img src="../assets/img/footer-periscope.png" alt=""></a></li>
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
                color: grey;
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