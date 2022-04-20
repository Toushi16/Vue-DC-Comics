<template>
    <div class="comic">
        <figure class="comic__thumb">
            <img :src="srcThumb" alt="">
        </figure>

        <h4 class="comic__title">
            {{ title }}
        </h4>
    </div>
</template>

<script>
    export default {
        props: {
            srcThumb: {
                type: String,
                required: true
            },
            title: {
                type: String,
                required: true,
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';
@import '../assets/scss/mixins.scss';

.comic {

    .comic__thumb {

        margin-bottom: 15px;
        cursor: pointer;

        img {
            display: block;
            aspect-ratio: 1/1;
            width: 85%;
            object-fit: cover;
            object-position:top center;
        }
    }

    .comic__title {
        text-transform: uppercase;
        font-size: 12px;
        font-weight: 400;
        padding-top: 8px;
        padding-bottom: 20px;
    }
}
</style>