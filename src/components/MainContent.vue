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
    <div class="wrapper">
      <h2>CURRENT SERIES</h2>
      <div class="container-cards">
        <CardMain
          v-for="comic in dcComics"
          :key="comic.series"
          :comic="comic"
        />
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
  }
}
</style>
