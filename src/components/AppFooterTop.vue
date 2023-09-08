<script>
export default {
  // components: { }

  data() {
    return {
      links: [
        {
          imagePath: "../../public/img/buy-comics-digital-comics.png",
          text: "DIGITAL COMICS",
          url: "#",
          current: false,
        },
        {
          imagePath: "../../public/img/buy-comics-merchandise.png",
          text: "DC MERCHANDISE",
          url: "#",
          current: false,
        },
        {
          imagePath: "../../public/img/buy-comics-subscriptions.png",
          text: "SUBSCRIPTION",
          url: "#",
          current: false,
        },
        {
          imagePath: "../../public/img/buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR",
          url: "#",
          current: false,
        },
        {
          imagePath: "../../public/img/buy-dc-power-visa.svg",
          text: "DC POWERS VISA",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="wrapper">
      <ul>
        <li v-for="link in links">
          <img :src="link.imagePath" alt="" />
          <a :href="link.url">
            <span>{{ link.text }}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.footer-top {
  height: $height-footer-top;
  background-color: $color-secondary;

  .wrapper {
    height: 100%;

    ul {
      height: 100%;

      display: flex;
      justify-content: space-around;
      align-items: center;

      li {
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 1rem;
        color: white;

        img {
          width: 50px;
        }
      }
    }
  }
}
</style>
