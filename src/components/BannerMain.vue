<template>
  <div class="banner">
    <div class="container">
      <ul>
        <li v-for="(item, index) in menuLink" :key="index">
          <a :href="item.link"> </a>
          <img :src="'../assets/img/' + item.img" />
          <p>{{ item.name }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "BannerMain",
  data() {
    return {
      menuLink: [
        {
          name: "DIGITAL COMICS",
          img: "buy-comics-digital-comics.png",
          link: "#",
        },
        {
          name: "DC MERCHANDISE",
          img: "buy-comics-merchandise.png",
          link: "#",
        },
        {
          name: "SUBSCRIPTION",
          img: "buy-comics-shop-locator.png",
          link: "#",
        },
        {
          name: "COMIC SHOP LOCATOR",
          img: "buy-comics-subscriptions.png",
          link: "#",
        },
        {
          name: "DC POWER VISA",
          img: "buy-dc-power-visa.svg",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/variables";
@import "../assets/scss/partials/general";

.banner {
  padding: 1rem 0;
  background-color: $back-color;
  color: white;
  img {
    object-fit: contain;
    object-position: center;
    height: 50px;
    margin-right: 3px;
  }
}

ul {
  padding: 1rem;
  display: flex;
  list-style: none;
  justify-content: space-around;
  align-items: center;
}
li {
  justify-content: space-around;
  align-items: center;
  display: flex;
}
</style>