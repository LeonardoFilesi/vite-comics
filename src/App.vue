<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import AppNavbar from "./components/AppNavbar.vue";
  import AppInfo from "./components/AppInfo.vue";
  import AppFooter from "./components/AppFooter.vue"
export default {
  components: {
    AppHeader,
    AppMain,
    AppNavbar,
    AppInfo,
    AppFooter,
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppNavbar/>
  <AppInfo/>
  <AppFooter/>
</template>

<style lang="scss">
  @use "../src/style/general.scss"
</style>