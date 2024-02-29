<script>
export default {
    name: 'AppNav',

    data() {
        return {
            tabs: ["Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"],
        }
    },
}
</script>

<template>
    <nav>
        <div>
            <img id="logo" src="/img/dc-logo.png" alt="logo DC">

            <ul>
                <li class="tabs" v-for="tab in tabs">
                    {{ tab }}
                </li>
            </ul>
        </div>
    </nav>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

nav {
    background-color: white;

    div {
        @include container;

        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 115px;

        #logo {
            height: 80px;
        }
        
        ul {
            display: flex;
            gap: 40px;
            list-style-type: none;

            .tabs {
                display: flex;
                align-items: center;
                height: 115px;

                font-weight: bold;
                text-transform: uppercase;
                color: $secondaryColor;
                border-bottom: 5px solid transparent;
                cursor: pointer;

                &:hover {
                    color: $primaryColor;
                    border-bottom: 5px solid $primaryColor;
                }
            }
        }
    }
    
}
</style>