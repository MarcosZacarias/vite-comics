<script>
import AppFooterTop from "./AppFooterTop.vue";
import AppFooterMain from "./AppFooterMain.vue";
import AppFooterBottom from "./AppFooterBottom.vue";

export default {
  components: { AppFooterTop, AppFooterMain, AppFooterBottom },

  data() {
    return {};
  },
};
</script>

<template>
  <footer>
    <AppFooterTop />
    <AppFooterMain />
    <AppFooterBottom />
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {
  background-color: $background-color-footer;
}
</style>
