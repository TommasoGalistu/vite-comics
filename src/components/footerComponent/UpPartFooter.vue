<script>
export default {
  name: "UpPartFooter",
  data() {
    return {
      images: [
        {
          src: "buy-comics-digital-comics.png",
          text: "DIGITAL COMICS",
        },
        {
          src: "buy-comics-merchandise.png",
          text: "DC MERCHANDISE",
        },
        {
          src: "buy-comics-subscriptions.png",
          text: "SUBSCRIPTION",
        },
        {
          src: "buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR",
        },
        {
          src: "buy-dc-power-visa.svg",
          text: "DC POWER VISA",
        },
      ],
    };
  },
  methods: {
    getImagePath(immagine) {
      return new URL(immagine, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contImgText" v-for="(image, index) in images" :key="index">
        <div class="contImg">
          <img
            :src="getImagePath(`../../assets/ecommercePhoto/${image.src}`)"
            alt=""
          />
        </div>
        <span>{{ image.text }}</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../style/partials/_mixins.scss" as *;
@use "../../style/partials/variables.scss" as *;

.containerAll {
  background-color: #0f82f7;
  padding: 3rem 0;

  .mainContainer {
    padding: 0 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;

    .contImgText {
      display: flex;
      align-items: center;
      width: auto;

      .contImg {
        height: 3rem;
        width: 2.5rem;
        margin-right: 0.5rem;

        img {
          width: 100%;
        }
      }

      span {
        font-size: 0.7rem;
        color: white;
      }
    }
  }
}
</style>