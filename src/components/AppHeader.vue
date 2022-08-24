<template>
    <header class="container">
        <a href="#">
            <img src="../assets/img/dc-logo.png" alt="DC Logo">
        </a>

        <ul>
            <li v-for="(list, index) in lists" :key="index" :class="list.isActive?'active':''">
                <a :href="list.url">{{list.text}}</a>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            lists: [
                    {
                        text: 'Characters',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Comics',
                        isActive: true,
                        url: '#'
                    },
                    {
                        text: 'Movies',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'TV',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Games',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Collectibles',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Videos',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Fans',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'News',
                        isActive: false,
                        url: '#'
                    },
                    {
                        text: 'Shop',
                        isActive: false,
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

    header {
        @include flex('vertical');
        justify-content: space-between;
        padding: .7rem 0;

        ul {
            li {
                display: inline-block;
                margin: 0 15px;

                &.active {
                    background-color: $brand_color;
                    padding: 1rem;
                    border-radius: .5rem;

                    a {
                        color: #fff;
                    }
                }

                    a {
                        color: #464646;
                        text-decoration: none;
                        font-weight: bold;

                    &:hover {
                        color: $brand_color;
                    }
                }
            }
        }
    }
</style>