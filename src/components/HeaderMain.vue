<template>
  <div class="container">
    <div class="c-logo">
      <img src="../assets/img/dc-logo.png" alt="" />
    </div>
    <div class="c-header-link">
      <ul>
        <li v-for="link in menuLink" :key="link.name">
          <a :href="link.link">
            {{ link.name }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderMain",
  data() {
    return {
      menuLink: [
        {
          name: "CHARACTERS",
          link: "#",
        },
        {
          name: "COMICS",
          link: "#",
        },
        {
          name: "MOVIES",
          link: "#",
        },
        {
          name: "TV",
          link: "#",
        },
        {
          name: "GAMES",
          link: "#",
        },
        {
          name: "COLLECTIBLES",
          link: "#",
        },
        {
          name: "VIDEOS",
          link: "#",
        },
        {
          name: "FANS",
          link: "#",
        },
        {
          name: "NEWS",
          link: "#",
        },
        {
          name: "SHOP",
          link: "#",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/partials/variables";
@import "../assets/scss/partials/general";
$logo-side: 4rem;
$header-height: 5rem;
$border-bottom-hover-height: 0.5rem;

.container {
  margin-bottom: $border-bottom-hover-height;
  height: $header-height;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .c-logo {
    width: 30%;
    text-align: start;
    img {
      height: $logo-side;
      width: $logo-side;
    }
  }
  .c-header-link {
    height: $header-height;
    width: 70%;
    ul {
      list-style-type: none;
      overflow-x: scroll;
      white-space: nowrap;
      padding: 0;
    }
    li {
      margin-bottom: -$border-bottom-hover-height;
      vertical-align: middle;
      display: inline-block;
      position: relative;
      list-style: none;
      margin: 0 0.3rem;
      background-color: white;
      line-height: $header-height;
      border-bottom: $border-bottom-hover-height solid transparent;
      &:hover a {
        color: $back-color;
      }
      &:hover {
        border-bottom: $border-bottom-hover-height solid $back-color;
      }
    }
    a,
    a:visited {
      font-weight: bold;
      color: gray;
      text-decoration: none;
    }
  }
}
</style>
