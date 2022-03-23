<template>
  <div class="container">
    <button type="submit">SIGN-UP NOW!</button>
    <div class="socialIcons">
      <ul>
        <li v-for="(icon, index) in socialIcons" :key="index">
          <a :href="icon.link">{{ icon.name }}</a>
        </li>
      </ul>
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
