<template>
    <main>
        <section id="jumbotron">
            <div class="jumbo-text">
                CURRENT SERIES
            </div>
        </section>

        <section id="main-content" class="container">
            <div class="comic" v-for="(comic, index) in comics" :key="index">
                <div class="img-wrapper">
                    <img :src="comic.thumb" :alt="comic.series">
                </div>

                <h4>{{comic.series.toUpperCase()}}</h4>
            </div>

            <div class="load-more-btn">
                <button>LOAD MORE</button>
            </div>
        </section>

        <section id="products">
            <ul>
                <li v-for="(product, index) in products" :key="index">
                    <img :src="product.logo" :alt="product.text">
                    <a :href="product.url">{{product.text}}</a>
                </li>
            </ul>
        </section>
    </main>
</template>

<script>
export default {
    name: 'AppContent',
    data() {
        return {
            products: [
                {
                    logo: require('../assets/img/buy-comics-digital-comics.png'),
                    text: 'Digital Comics',
                    url: '#'
                },
                {
                    logo: require('../assets/img/buy-comics-merchandise.png'),
                    text: 'DC merchandise',
                    url: '#'
                },
                {
                    logo: require('../assets/img/buy-comics-subscriptions.png'),
                    text: 'Subscription',
                    url: '#'
                },
                {
                    logo: require('../assets/img/buy-comics-shop-locator.png'),
                    text: 'Comic shop locator',
                    url: '#'
                },
                {
                    logo: require('../assets/img/buy-dc-power-visa.svg'),
                    text: 'DC power visa',
                    url: '#'
                },
            ],
            comics: [
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                            "price": "$19.99",
                            "series": "Action Comics",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                            "price": "$3.99",
                            "series": "American Vampire 1976",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                            "price": "$16.99",
                            "series": "Aquaman",
                            "type": "graphic novel"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                            "price": "$2.99",
                            "series": "Batgirl",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                            "price": "$3.99",
                            "series": "Batman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                            "price": "$2.99",
                            "series": "Batman Beyond",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                            "price": "$3.99",
                            "series": "Batman/Superman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                            "price": "$4.99",
                            "series": "Batman/Superman Annual",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                            "price": "$5.99",
                            "series": "Batman: The Joker War Zone",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                            "price": "$6.99",
                            "series": "Batman: Three Jokers",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                            "price": "$4.99",
                            "series": "Batman: White Knight Presents: Harley Quinn",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                            "price": "$16.99",
                            "series": "Catwoman",
                            "type": "graphic novel"
                        }
                    ]
        }
    }
}
</script>

<style scoped lang="scss">

@import '../styles/generals.scss';
@import '../styles/variables.scss';
@import '../styles/mixins.scss';

    main {
        background-color: $content_sect_color;
    }

    #jumbotron {
        height: 450px;
        background-image: url('../assets/img/jumbotron.jpg');
        position: relative;

        .jumbo-text {
            padding: .5rem 3rem;
            background-color: $brand_color;
            border: none;
            color: #fff;
            font-weight: bold;
            width: 240px;
            height: 50px;
            @include flex('both');
            position: absolute;
            bottom: -25px;
            left: 270px;
        }
    }

    #main-content {
        padding: 3rem 0;
        display: flex;
        flex-wrap: wrap;


        .comic {
            flex-basis: calc(100% / 6);
            padding: 1rem 0;

            .img-wrapper {
                width: 150px;
                height: 150px;
                cursor: pointer;
                transition: transform .5s linear;

                &:hover {
                    transform: scale(1.1);
                }

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    object-position: top;
                }
            }

            h4 {
                color: #fff;
                margin-top: 1rem;
                font-weight: 300;
                font-size: .8rem;
                width: 70%;            
            }

        }
        .load-more-btn {
            width: 100%;
            @include flex('both');

            button {
                padding: .5rem 3rem;
                background-color: $brand_color;
                border: none;
                color: #fff;
                font-weight: bold;
                cursor: pointer;
            }
        }
    }

    #products {
        padding: 3rem 0;
        background-color: $brand_color;
        @include flex('both');

        ul {
            list-style: none;
            display: flex;

            li {
                @include flex('both');
                margin-right: 40px;

                a {
                    text-decoration: none;
                    color: #fff;

                    &:hover {
                        text-decoration: underline;
                    }
                }

                img {
                    width: 50px;
                    margin-right: 10px;
                }
            }
        }
    }
</style>