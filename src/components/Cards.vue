<template>
  <div class="card">
    <div class="imgCard">
      <img :src="img" :alt="title" />
    </div>
    <div class="title">{{ title }}</div>
  </div>
</template>

<script>
export default {
  name: "CardsCentral",
  props: {
    title: String,
    img: String,
  },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/partials/variables";
@import "../assets/scss/partials/general";
$gutter: 1rem;

.card {
  align-self: stretch;
  padding: 0 1rem;
  margin: 2rem 0;
  height: 200px;
  width: calc(100% / 6);
  .imgCard {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    overflow: hidden;
    height: 90%;
    img {
      width: 100%;
    }
    .title {
      font-weight: 1rem;
      white-space: wrap;
      margin: $gutter 0;
    }
  }
}
</style>