<script>
import dcComics from "../assets/dc-comics.json";

export default {
  // components: {}

  data() {
    return {
      dcComics,
    };
  },
};
</script>

<template>
  <main>
    <div class="wrapper">
      <h2>CURRENT SERIES</h2>
      <div class="container-cards">
        <div class="card" v-for="comic in dcComics">
          <div class="card-media">
            <img :src="comic.thumb" alt="" />
          </div>
          <div class="card-text">
            {{ comic.series }}
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.wrapper {
  color: white;
  padding: 1rem 0 1rem 0;
  h2 {
    padding: 0.2rem;
    margin-bottom: 1rem;
    background-color: $color-secondary;

    display: inline-block;
  }

  .container-cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1%;

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
  }
}
</style>
