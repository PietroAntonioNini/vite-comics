<script>
export default {
    name: 'AppMain',

    data() {
        return {

        }
    },
}
</script>

<template>
    <main>
        <div>
            <span> &rightarrow; Content goes here &leftarrow; </span>
        </div>
    </main>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

main {
    background-color: $secondaryColor;

    div {
        @include container;
        display: flex;
        align-items: center;
        height: 130px;

        span {
            font-size: 25px;
            font-weight: bold;
        }
    }
}


</style>