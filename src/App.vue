<script>
import AppNav from './components/AppNav.vue';
import AppMain from './components/AppMain.vue';
import AppBanner from './components/AppBanner.vue';

export default {
  components: {
    AppNav,
    AppMain,
    AppBanner,
  }
}
</script>

<template>
  <AppNav></AppNav>

  <AppMain></AppMain>

  <AppBanner></AppBanner>
</template>

<style lang="scss">
</style>
