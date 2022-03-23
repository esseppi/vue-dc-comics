<template>
  <footer>
    <div class="footer-back">
      <div class="container">
        <div class="footer-list">
          <div>
            <ul>
              <h3>DC COMICS</h3>
              <li v-for="(link, index) in dcComics" :key="index">
                <a :href="link.link">
                  {{ link.text }}
                </a>
              </li>
            </ul>
            <ul>
              <h3>SHOP</h3>
              <li v-for="(link, index) in shop" :key="index">
                <a :href="link.link">
                  {{ link.text }}
                </a>
              </li>
            </ul>
          </div>
          <ul>
            <h3>DC</h3>
            <li v-for="(link, index) in dc" :key="index">
              <a :href="link.link">
                {{ link.text }}
              </a>
            </li>
          </ul>
          <ul>
            <h3>SITES</h3>
            <li v-for="(link, index) in sites" :key="index">
              <a :href="link.link">
                {{ link.text }}
              </a>
            </li>
          </ul>
        </div>
        <div class="footer-logo">
          <img src="../../public/assets/img/dc-logo-bg.png" alt="" srcset="" />
        </div>
      </div>
    </div>
    <BottomBar />
  </footer>
</template>

<script>
import BottomBar from "./BottomBar.vue";
export default {
  name: "FooterMain",
  components: {
    BottomBar,
  },
  data() {
    return {
      dcComics: [
        {
          href: "#",
          text: "characters",
        },
        {
          href: "#",
          text: "comics",
        },
        {
          href: "#",
          text: "movies",
        },
        {
          href: "#",
          text: "TV",
        },
        {
          href: "#",
          text: "games",
        },
        {
          href: "#",
          text: "videos",
        },
        {
          href: "#",
          text: "news",
        },
      ],
      shop: [
        {
          href: "#",
          text: "shop DC",
        },
        {
          href: "#",
          text: "shop DC collectibles",
        },
      ],
      dc: [
        {
          href: "#",
          text: "terms of use",
        },
        {
          href: "#",
          text: "privacy",
        },
        {
          href: "#",
          text: "ad choice",
        },
        {
          href: "#",
          text: "advertising",
        },
        {
          href: "#",
          text: "jobs",
        },
        {
          href: "#",
          text: "subscriptions",
        },
        {
          href: "#",
          text: "talent workshops",
        },
        {
          href: "#",
          text: "CPSC certificates",
        },
        {
          href: "#",
          text: "ratings",
        },
        {
          href: "#",
          text: "shop helps",
        },
        {
          href: "#",
          text: "contact us",
        },
      ],
      sites: [
        {
          href: "#",
          text: "DC",
        },
        {
          href: "#",
          text: "MAD magazines",
        },
        {
          href: "#",
          text: "DC kids",
        },
        {
          href: "#",
          text: "DC universe",
        },
        {
          href: "#",
          text: "DC power visa",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/partials/variables";
@import "../assets/scss/partials/general";

.footer-back {
  color: white;
  background-image: url("../../public/assets/img/footer-bg.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  .container {
    height: 300px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .footer-list {
    padding: 2rem 0;
    display: flex;
    h3 {
      margin: 0.8rem 0;
    }
    div ul {
      padding-left: 0;
    }
    ul {
      list-style: none;
      li {
        white-space: nowrap;
      }
    }
    a {
      color: gray;
      &:hover {
        color: white;
      }
    }
  }
  .footer-logo {
    width: 70%;
    height: 100%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    img {
      align-self: center;
      object-fit: cover;
      object-position: center;
      height: 130%;
    }
  }
}
</style>
