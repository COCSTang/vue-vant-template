<template>
  <section class="app-main">
    <keep-alive :include="cachedViews">
      <router-view :key="key" />
    </keep-alive>
  </section>
</template>

<script>
  export default {
    name: 'AppMain',
    computed: {
      cachedViews () {
        return this.$store.state.routerView.cachedViews
      },
      key () {
        return this.$route.path
      }
    }
  }
</script>

<style lang="scss" scoped>
  /*.app-main {*/
  /*  padding: 16px;*/
  /*}*/
</style>
