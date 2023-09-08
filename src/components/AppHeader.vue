<script>
// import ...... from "...."

export default {
  // components: {}

  data() {
    return {
      image: "../../public/img/dc-logo.png",
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          current: false,
        },
        {
          text: "COMICS",
          url: "#",
          current: false,
        },
        {
          text: "MOVIES",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "GAMES",
          url: "#",
          current: false,
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          current: false,
        },
        {
          text: "VIDEOS",
          url: "#",
          current: false,
        },
        {
          text: "FANS",
          url: "#",
          current: false,
        },
        {
          text: "NEWS",
          url: "#",
          current: false,
        },
        {
          text: "SHOP",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="wrapper">
      <img :src="image" alt="" />

      <ul>
        <li v-for="link in links">
          <a :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.wrapper {
  display: flex;
  gap: 20rem;
  justify-content: space-between;
  align-items: center;

  ul {
    flex-grow: 1;

    display: flex;
    justify-content: space-around;

    li {
      font-size: 0.9rem;
      font-weight: bolder;
      a {
        &:hover {
          color: $color-secondary;
        }
      }
    }
  }
}
</style>
