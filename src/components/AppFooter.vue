<template>
    <footer>
        <div class="container">
            <div class="footer-left">
                <ul class="dc-comics">
                    <h4 class="list-title">DC Comics</h4>
                    <li v-for="(list, index) in dcComicLists" :key="index">
                        <a :href="list.url">{{list.text}}</a>
                    </li>

                    <ul class="shop">
                        <h4 class="list-title">Shop</h4>
                        <li v-for="(list, index) in shopLists" :key="index">
                            <a :href="list.url">{{list.text}}</a>
                        </li>
                    </ul>
                </ul>

                <ul class="dc">
                    <h4 class="list-title">DC</h4>
                    <li v-for="(list, index) in dcLists" :key="index">
                        <a :href="list.url">{{list.text}}</a>
                    </li>
                </ul>

                <ul class="sites">
                    <h4 class="list-title">Sites</h4>
                    <li v-for="(list, index) in sitesLists" :key="index">
                        <a :href="list.url">{{list.text}}</a>
                    </li>
                </ul>
            </div>


            <div class="footer-right">
                <img src="../assets/img/dc-logo-bg.png" alt="DC Logo">
            </div>
        </div>
        
        <div class="cta">
            <a id="sign-up-btn">SIGN-UP NOW</a>

            <div class="social">
                <span class="follow-us">FOLLOW US</span>
                <ul class="cta-list">
                    <li v-for="(social, index) in socialList" :key="index">
                        <a :href="social.url">
                            <img :src="social.logo" :alt="social.name">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dcComicLists: [
                {
                    url: '#',
                    text: 'Characters'
                },
                {
                    url: '#',
                    text: 'Comics'
                },
                {
                    url: '#',
                    text: 'Movies'
                },
                {
                    url: '#',
                    text: 'TV'
                },
                {
                    url: '#',
                    text: 'Games'
                },
                {
                    url: '#',
                    text: 'Videos'
                },
                {
                    url: '#',
                    text: 'News'
                },
            ],
            shopLists: [
                {
                    url: '#',
                    text: 'Shop DC'
                },
                {
                    url: '#',
                    text: 'Shop DC Collectibles'
                }
            ],
            dcLists: [
                {
                    url: '#',
                    text: 'Terms Of Use'
                },
                {
                    url: '#',
                    text: 'Privacy Policy (new)'
                },
                {
                    url: '#',
                    text: 'Ad Choices'
                },
                {
                    url: '#',
                    text: 'Advertising'
                },
                {
                    url: '#',
                    text: 'Jobs'
                },
                {
                    url: '#',
                    text: 'Subscriptions'
                },
                {
                    url: '#',
                    text: 'Talent Workshops'
                },
                {
                    url: '#',
                    text: 'CPSC certificates'
                },
                {
                    url: '#',
                    text: 'Ratings'
                },
                {
                    url: '#',
                    text: 'Shop Help'
                },
                {
                    url: '#',
                    text: 'Contact Us'
                },
            ],
            sitesLists: [
                {
                    url: '#',
                    text: 'DC'
                },
                {
                    url: '#',
                    text: 'MAD Magazine'
                },
                {
                    url: '#',
                    text: 'DC Kids'
                },
                {
                    url: '#',
                    text: 'DC universe'
                },
                {
                    url: '#',
                    text: 'DC Power Visa'
                },
            ],
            socialList: [
                {
                    name: 'Facebook',
                    logo: require('../assets/img/footer-facebook.png'),
                    url: '#'
                },
                {
                    name: 'Twitter',
                    logo:  require('../assets/img/footer-twitter.png'),
                    url: '#'
                },
                {
                    name: 'YouTube',
                    logo:  require('../assets/img/footer-youtube.png'),
                    url: '#'
                },
                {
                    name: 'Pinterest',
                    logo:  require('../assets/img/footer-pinterest.png'),
                    url: '#'
                },
                {
                    name: 'Periscope',
                    logo:  require('../assets/img/footer-periscope.png'),
                    url: '#'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/variables.scss';
@import '../styles/mixins.scss';

    footer {
        background-image: url('../assets/img/footer-bg.jpg');
        background-position: center;
        background-size: cover;
        padding-top: 2rem;
        position: relative;

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 350px;

            .footer-left {
                display: flex;
                gap: 0 3rem;

                ul {
                list-style: none;

                .list-title {
                    font-size: 1.5rem;
                    color: #fff;
                }

                li {
                    margin: 10px 0;

                    a {
                        color: #727171;
                        text-decoration: none;
                        font-size: small;

                        &:hover {
                            text-decoration: underline;
                        }
                    }
                }
            }
        }

        .footer-right {
            img {
                display: block;
            }
        }
    }

    .cta {
        background-color: $footer_color;
        padding: 2rem 0;
        @include flex ('vertical');
        justify-content: space-around;
        position: relative;
        z-index: 1;

        #sign-up-btn {
            background-color: $footer_color;
            padding: .7rem;
            border: 2px solid $brand_color;
            color: #fff;
            cursor: pointer;
            transition: all linear .5s;

            &:hover {
                background-color: $brand_color;
                color: #fff;
            }
        }

        .social {
            @include flex('both');

            .follow-us {
                color: $brand_color;
                font-weight: bold;
                margin-right: 10px;
            }
        }

        .cta-list {
            list-style: none;

            li {
                display: inline-block;

                a {
                    margin: 0 10px;
                }
            }
        }
    }
}
</style>