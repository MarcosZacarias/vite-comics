<script>
export default {
  // components: { }
  data() {
    return {
      btnText: "SIGN-UP NOW!",
      socials: {
        text: "FOLLOW US",
        icons: [
          "../../public/img/footer-facebook.png",
          "../../public/img/footer-periscope.png",
          "../../public/img/footer-pinterest.png",
          "../../public/img/footer-twitter.png",
          "../../public/img/footer-youtube.png",
        ],
      },
    };
  },
};
</script>

<template>
  <div class="footer-bottom">
    <div class="wrapper">
      <button>{{ btnText }}</button>
      <ul>
        <li>
          {{ socials.text }}
        </li>
        <li v-for="(icon, index) in socials.icons">
          <img :src="icon" alt="" />
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.footer-bottom {
  height: $height-footer-bottom;

  .wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;

    font-weight: 900;

    button {
      height: 50%;
      width: 10%;
      padding: 0.7rem;

      font-size: 1.05rem;

      border-color: $color-secondary;
      color: white;
      background-color: transparent;
    }

    ul {
      display: flex;
      align-items: center;
      gap: 1rem;

      color: $color-secondary;
    }
  }
}
</style>
