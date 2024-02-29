<script>
export default {
    name: 'AppBanner',

    data() {
        return {
            articles: [
                {
                    img: "/img/buy-comics-digital-comics.png",
                    text: "Digital Comics"
                },
                {
                    img: "/img/buy-comics-merchandise.png",
                    text: "DC Merchandise"
                },
                {
                    img: "/img/buy-comics-subscriptions.png",
                    text: "Subscription"
                },
                {
                    img: "/img/buy-comics-shop-locator.png",
                    text: "Comic shop locator"
                },
                {
                    img: "/img/buy-dc-power-visa.svg",
                    text: "DC power visa"
                },
            ]
        }
    }    
}
</script>

<template>
    <div id="banner">
        <div id="banner-container">
            <ul>
                <li v-for="article in articles">
                    <img :src="article.img" alt="immagini articoli">
                    <span> {{ article.text }} </span>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

#banner {
    background-color: $primaryColor;

    #banner-container {
        @include container;

        ul {
            display: flex;
            justify-content: space-around;
            align-items: center;

            height: 160px;

            list-style-type: none;

            li {
                display: flex;
                align-items: center;
                gap: 20px;

                text-transform: uppercase;
                font-weight: 500;

                img {
                    height: 50px;
                }
            }
        }
    }
}
</style>