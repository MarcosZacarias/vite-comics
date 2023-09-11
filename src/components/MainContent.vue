<script>
import dcComics from "../data/comics";
import CardMain from "../components/CardMain.vue";

export default {
  components: { CardMain },

  data() {
    return {
      dcComics,
    };
  },
};
</script>

<template>
  <main>
    <div class="jumbotron"></div>

    <div class="wrapper">
      <h2>CURRENT SERIES</h2>
      <div class="container-cards">
        <CardMain
          v-for="comic in dcComics"
          :key="comic.series"
          :comic="comic"
        />
      </div>
      <button>Load More</button>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
  .jumbotron {
    background-image: url("../../public/img/jumbotron.jpg");
    background-size: cover;
    width: 100%;
    height: 400px;
  }
}

.wrapper {
  color: white;
  margin-top: -30px;
  padding: 1rem 0 1rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;

  h2 {
    padding: 0.2rem;
    margin-bottom: 1rem;
    background-color: $color-secondary;

    align-self: flex-start;

    display: inline-block;
  }

  .container-cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1%;
  }

  button {
    height: 50%;
    width: 10%;
    padding: 0.7rem;

    font-size: 1.05rem;

    color: white;
    background-color: $color-secondary;
    border-color: transparent;
  }
}
</style>
