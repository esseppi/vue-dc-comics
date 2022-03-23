<template>
  <div id="app">
    <HeaderMain />
    <CentralMain />
  </div>
</template>

<script>
import HeaderMain from "./components/HeaderMain.vue";
import CentralMain from "./components/CentralMain.vue";

export default {
  name: "App",
  components: {
    HeaderMain,
    CentralMain,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/partials/general";
</style>
