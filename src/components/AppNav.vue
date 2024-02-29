<script>
export default {
    name: 'AppNav',

    data() {
        return {
            links: ["Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"],
        }
    },
}
</script>

<template>
    <nav class="container">
        <img id="logo" src="/img/dc-logo.png" alt="logo DC">

        <ul>
            <li class="links" v-for="link in links">
                {{ link }}
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
@use '../styles/variables' as *;

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    height: 115px;
    background-color: white;

    #logo {
        height: 80px;
    }
    
    ul {
        display: flex;
        gap: 40px;
        list-style-type: none;

        li {
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
</style>