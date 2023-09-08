<script>
// import ...... from "...."

export default {
  // components: {}

  data() {
    return {};
  },
};
</script>

<template>
  <footer>
    <div class="footer-top"></div>
    <div class="footer-main"></div>
    <div class="footer-bottom"></div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {
  background-color: $background-color-footer;
  .footer-top {
    height: $height-footer-top;

    background-color: $color-secondary;
  }

  .footer-main {
    height: $height-footer-main;
    background-image: url("../../public/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
  }

  .footer-bottom {
    height: $height-footer-bottom;
  }
}
</style>
