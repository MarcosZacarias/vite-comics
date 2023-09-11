<script>
export default {
  // components: {}

  props: {
    thumb: String,
    series: String,
  },
};
</script>

<template>
  <div class="card">
    <div class="card-media">
      <img :src="thumb" alt="" />
    </div>
    <div class="card-text">
      {{ series }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
// @use "../styles/partials/variables" as *;

.card {
  width: calc(95% / 6);
  margin-bottom: 1rem;
  .card-media {
    width: 100%;
    aspect-ratio: 1;
    img {
      width: 100%;
      height: 100%;

      object-fit: cover;
      object-position: 0% 0%;
    }
  }
}
</style>
