<template>
  <div class="back">
    <div class="container">
      <button type="submit">SIGN-UP NOW!</button>

      <div class="socialIcons">
        <div>FOLLOW US</div>
        <ul>
          <li v-for="(icon, index) in socialIcons" :key="index">
            <a :href="icon.link"
              ><img :src="'../assets/img/' + icon.img" :alt="icon.name"
            /></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      socialIcons: [
        {
          name: "Facebook",
          img: "footer-facebook.png",
          link: "#",
        },
        {
          name: "Twitter",
          img: "footer-twitter.png",
          link: "#",
        },
        {
          name: "YouTube",
          img: "footer-youtube.png",
          link: "#",
        },
        {
          name: "Pinterest",
          img: "footer-pinterest.png",
          link: "#",
        },
        {
          name: "Periscope",
          img: "footer-periscope.png",
          link: "#",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
@import "../assets/scss/partials/variables";
@import "../assets/scss/partials/general";
.back {
  background-color: #303030;
}
.container {
  display: flex;
  justify-content: space-between;
  padding: 1rem 0;
  button {
    padding: 0.5rem;
    color: white;
    background-color: transparent;
    border: 3px solid $back-color;
  }
  .socialIcons {
    display: flex;
    align-items: center;
    justify-content: space-around;
    li {
      margin-right: 0.4rem;
    }
    div:first-child {
      margin-right: 1rem;
      color: $back-color;
      font-weight: bolder;
    }
  }
  ul {
    list-style: none;
    display: flex;
    justify-content: space-around;
  }
}
</style>
