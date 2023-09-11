<script>
export default {
  // components: {}

  props: {
    comic: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="card-media">
      <img :src="comic.thumb" alt="" />
      <div class="card-media-hover">
        <p>{{ comic.type }}</p>
        <p>{{ comic.price }}</p>
      </div>
    </div>
    <div class="card-text">
      {{ comic.series }}
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

    position: relative;

    .card-media-hover {
      display: none;
      font-size: 1.5rem;
      font-weight: bold;
    }

    &:hover > .card-media-hover {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      align-items: center;

      position: absolute;
      top: 0;
      right: 0;

      width: 100%;
      aspect-ratio: 1;

      background-color: rgba($color: #757575, $alpha: 0.8);
    }

    img {
      width: 100%;
      height: 100%;

      object-fit: cover;
      object-position: 0% 0%;
    }
  }
}
</style>
