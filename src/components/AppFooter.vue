<script>
import AppBanner from './AppBanner.vue';



export default {

    name: 'AppFooter',

    components: {
        AppBanner,
    },

    data() {
        return {
            links: [
                {
                    title: "Dc comics",
                    links: ["Character", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "Shop",
                    links: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    links: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Ratings", "Shop Help", "Contact US"]
                },
                {
                    title: "Sities",
                    links: ["DC", "MAD magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                },
                
            ]
        }
    },
}
</script>

<template>
    
    <AppBanner></AppBanner>

    <footer>

        <div class="footer-links">
            <div class="column-left">
                <div>
                    <div v-for="link in links.slice(0,1)">
                        <h3> {{ link.title }} </h3>

                        <ul>
                            <li v-for="sublink in link.links">
                                {{ sublink }}
                            </li>
                        </ul>
                    </div>
                </div>

                <div>
                    <div v-for="link in links.slice(1,2)">
                        <h3> {{ link.title }} </h3>

                        <ul>
                            <li v-for="sublink in link.links">
                                {{ sublink }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="column-center" v-for="link in links.slice(2,3)">
                <h3> {{ link.title }} </h3>

                <ul>
                    <li v-for="sublink in link.links">
                        {{ sublink }}
                    </li>
                </ul>
            </div>

            <div class="column-right" v-for="link in links.slice(3,4)">
                <h3> {{ link.title }} </h3>

                <ul>
                    <li v-for="sublink in link.links">
                        {{ sublink }}
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

footer {
    height: 380px;

    display: flex;
    align-items: center;

    background-image: url(/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    .footer-links {
        @include container;

        display: flex;
        gap: 55px;

        .column-left {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        h3 {
            margin-bottom: 10px;

            font-size: 18px;
            font-weight: bold;
            text-transform: uppercase;
        }

        ul {
            display: flex;
            flex-direction: column;
            gap: 3px;
            list-style-type: none;

            li {
                cursor: pointer;

                font-size: 12px;
                color: #959595;

                &:hover {
                    color: white;
                }
            }
        }
    }
}
</style>