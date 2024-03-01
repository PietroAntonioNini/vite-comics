<script>
export default {
    name: 'ComicsItem',

    props: {
        comicsName: String,
        comicsImg: String
    },

    data() {
        return {

        }
    },
}
</script>

<template>
    <div id="comics-items">
        <div class="comics-poster">
            <img class="comics-img" :src="comicsImg" :alt="comicsName">
        </div>

        <h3 class="comics-title">{{ comicsName }}</h3>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

    #comics-items {
        display: flex;
        flex-direction: column;
        gap: 20px;

        .comics-poster {
            width: 185px;
            height: 185px;

            .comics-img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: top;
            }
        }

        .comics-title {
            font-size: 16px;
            font-weight: 400;
            text-transform: uppercase;
        }
    }

</style>