<template>
  <div id="app">
    <HeaderMain />
    <CentralMain />
    <FooterMain />
  </div>
</template>

<script>
import HeaderMain from "./components/HeaderMain.vue";
import CentralMain from "./components/CentralMain.vue";
import FooterMain from "./components/FooterMain.vue";

export default {
  name: "App",
  components: {
    HeaderMain,
    CentralMain,
    FooterMain,
  },
};
</script>

<style lang="scss">
// @import "./assets/scss/allStyle.scss";
* {
  box-sizing: border-box;
  margin: 0;
}
</style>
