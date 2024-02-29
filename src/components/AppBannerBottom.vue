<script>
export default {
    name: 'AppBannerBottom',

    data() {
        return {
            socials: [
                {
                    img: "/img/footer-facebook.png",
                },
                {
                    img: "/img/footer-twitter.png",
                },
                {
                    img: "/img/footer-youtube.png",
                },
                {
                    img: "/img/footer-pinterest.png",
                },
                {
                    img: "/img/footer-periscope.png",
                },
            ]
        }
    }    
}
</script>

<template>
    <div id="banner-bottom">
        <div class="banner-container-bottom">

            <button id="sign-up">Sign-up now! </button>

            <div id="socials">
                <a class="follow-us" href="#">Follow US</a>
                
                <ul>
                    <li v-for="social in socials">
                        <img class="social-img" :src="social.img" alt="Loghi Social">
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

#banner-bottom {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: $tertiaryColor;

    .banner-container-bottom {
        @include container;

        height: 110px;

        display: flex;
        justify-content: space-between;
        align-items: center;

        #sign-up {
            padding: 12px 14px;

            font-size: 16px;
            font-weight: bold;
            text-transform: uppercase;

            border: 1px solid $primaryColor;
            background-color: transparent;
        }

        #socials {
            display: flex;
            gap: 40px;

            .follow-us {
                display: flex;
                align-items: center;
                
                font-size: 18px;
                font-weight: bold;
                text-decoration: none;
                text-transform: uppercase;

                color: $primaryColor;
            }

            ul {
                display: flex;
                gap: 20px;
                list-style-type: none;
            }
        }        
    }
}
</style>