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
        <span> &rightarrow; Content goes here &leftarrow; </span>
    </main>
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;

main {
    @include container;

    display: flex;
    align-items: center;
    height: 130px;
    background-color: $secondaryColor;

    span {
        font-size: 25px;
        font-weight: bold;
    }
}


</style>