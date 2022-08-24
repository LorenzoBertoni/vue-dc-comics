<template>
    <main>
        <section id="main-content" class="container">
            <div>
                <h1>Content goes here</h1>
            </div>
        </section>

        <section id="products">
            <!-- <ul>
                <li v-for="(product, index) in products" :key="index">
                    <img :src="product.logo" alt="">
                    <span>{{product.text}}</span>
                </li>
            </ul> -->
        </section>
    </main>
</template>

<script>
export default {
    name: 'AppContent',
    /*
    data() {
        return {
            products: [
                {
                    logo: 'buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    logo: 'buy-comics-merchandise.png',
                    text: 'DC merchandise'
                },
                {
                    logo: 'buy-comics-subscription.png',
                    text: 'Subscription'
                },
                {
                    logo: 'comics-digital-comics.png',
                    text: 'Comic shop locator'
                },
                {
                    logo: 'comics-digital-comics.png',
                    text: 'DC power visa'
                },
            ]
        }
    }
    */
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
    }
</style>