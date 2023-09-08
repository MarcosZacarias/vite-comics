<script>
export default {
  // components: { }
  data() {
    return {};
  },
};
</script>

<template>
  <div class="footer-main"></div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.footer-main {
  height: $height-footer-main;
  background-image: url("../../public/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
