<script>
import ComicsItem from './ComicsItem.vue';

export default {
    name: 'AppMain',

    components: {
        ComicsItem,
    },

    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },
}
</script>

<template>
    <div id="main-img">
        <img class="jumbotron-img" src="/img/jumbotron.jpg" alt="jumbotron">
    </div>

    <div id="main-cards">
        <h2 id="page-title">Current Series</h2>

        <ComicsItem v-for="comic in comics" :comics-name="comic.series" :comics-img="comic.thumb" class="card"></ComicsItem>

        <button id="more">Load More</button>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

#main-img {
    height: 400px;

    .jumbotron-img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

#main-cards {
    @include container;

    display: flex;
    justify-content: center;
    flex-flow: row wrap;
    gap: 10px;

    padding-top: 60px;
    position: relative;

    #page-title {
        position: absolute;
        top: -30px;
        left: -20px;

        padding: 10px 20px;

        font-size: 25px;
        text-transform: uppercase;
        background-color: $primaryColor;
    }

    .card {
        width: calc(100% / 6 - 10px / 6 * 5);
        margin-bottom: 40px;
    }

    #more {
        padding: 10px 70px;
        margin-bottom: 25px;

        font-size: 14px;
        font-weight: bold;
        text-transform: uppercase;

        background-color: $primaryColor;
        border: 0;
    }
}

</style>