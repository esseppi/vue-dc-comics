<template>
  <main>
    <header>
      <div class="jumbotron"></div>
      <div id="adv">CURRENT SERIES</div>
    </header>
    <section>
      <CardsCentral
        v-for="card in cardList"
        :img="card.thumb"
        :title="card.series"
        :key="card.series"
      />
      <button>LOAD MORE</button>
    </section>
    <footer>
      <BannerMain />
    </footer>
  </main>
</template>

<script>
import BannerMain from "./BannerMain.vue";
import CardsCentral from "./Cards.vue";
import cardList from "../assets/data/dc-comics.json";
export default {
  name: "CentralMain",
  components: {
    BannerMain,
    CardsCentral,
  },
  data() {
    return {
      cardList,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/variables";

.jumbotron {
  background-image: url(../../public/assets/img/jumbotron.jpg);
  background-position: top;
  background-size: cover;
  height: 45vh;
  width: 100%;
}
#adv {
  display: inline;
  transform: translateY(-30%);
  padding: 1rem;
  margin-left: calc(100% - $container-width);
  background-color: $back-color;
  color: white;
  font-weight: bolder;
}

section {
  width: $container-width;
  max-width: 1600px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  color: white;
  button {
    margin: 0 auto 1rem;
    padding: 1rem;
    background-color: $back-color;
  }
}
footer {
}
</style>