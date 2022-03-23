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
  name: "CentralMain",
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
          img: "buy-comics-digital-comics.png",
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
.banner {
  background-color: #0282f9;
}
img {
  width: 50px;
  height: 50px;
}
ul {
  padding: 1rem;
  display: flex;
  margin: 2rem;
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