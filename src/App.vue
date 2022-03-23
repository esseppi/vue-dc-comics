<template>
  <div id="app">
    <HeaderMain></HeaderMain>
  </div>
</template>

<script>
import HeaderMain from "./components/HeaderMain.vue";

export default {
  name: "App",
  components: {
    HeaderMain,
  },
  data: () => {},
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
