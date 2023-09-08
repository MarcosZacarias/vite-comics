<script>
// import ...... from "...."

export default {
  // components: {}

  data() {
    return {
      image: "../../public/img/dc-logo.png",
    };
  },
};
</script>

<template>
  <header>
    <div class="wrapper">
      <img :src="image" alt="" />
    </div>
  </header>
</template>

<style lang="scss" scoped></style>
