<script>
export default {
  // components: { }
  data() {
    return {
      listFooterMain: [
        {
          title: "DC COMICS",
          links: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "SHOP",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          links: [
            "Term Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent WorkShops",
            "CPSC Certification",
            "Ratings",
            "Shop Help",
            "Contact US",
          ],
        },
        {
          title: "SITES",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-main">
    <div class="wrapper">
      <div class="list-links">
        <div v-for="(list, index) in listFooterMain">
          <h3>{{ list.title }}</h3>
          <ul>
            <li v-for="link in list.links">{{ link }}</li>
          </ul>
        </div>
      </div>

      <img src="../../public/img/dc-logo-bg.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.footer-main {
  height: $height-footer-main;
  background-image: url("../../public/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;

  .wrapper {
    display: flex;
    justify-content: space-between;

    .list-links {
      padding: 2rem 0 2rem 0;
      height: 100%;
      width: 50%;
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;

      gap: 1rem;
    }

    img {
      width: 40%;
      height: 100%;
      object-fit: cover;
    }
  }
}

h3 {
  color: white;
  padding: 0.5rem 0 0.5rem 0;
}

li {
  padding: 0.3rem 0 0.3rem 0;
  color: #959595;
  font-size: 0.8rem;
}
</style>
