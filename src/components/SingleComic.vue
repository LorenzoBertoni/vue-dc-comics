<template>
    <div class="comic">
        <div class="img-wrapper">
            <img :src="thumb" :alt="series">
        </div>

        <h4>{{series.toUpperCase()}}</h4>
    </div>
</template>

<script>
export default {
    name: 'SingleComic',
    props: {
        thumb: String,
        series: String
    }
}
</script>

<style lang="scss">
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
</style>