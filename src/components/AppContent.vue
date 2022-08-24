<template>
    <main>
        <section id="main-content" class="container">
            <div>
                <h1>Content goes here</h1>
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

    #main-content {
        padding: 3rem 0;

        h1 {
            color: #fff;
        }
    }

    #products {
        height: 200px;
        background-color: $brand_color;
        @include flex('both');

        ul {
            list-style: none;
            display: flex;

            li {
                @include flex('both');

                a {
                    text-decoration: none;
                    color: #fff;

                    &:hover {
                        text-decoration: underline;
                    }
                }

                img {
                    width: 20%;
                    margin-right: 10px;
                }
            }
        }
    }
</style>