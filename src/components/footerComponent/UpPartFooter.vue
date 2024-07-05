<script>
export default {
  name: "UpPartFooter",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contImgText">
        <div class="contImg">
          <img
            src="/src/assets/ecommercePhoto/buy-comics-digital-comics.png"
            alt=""
          />
        </div>
        <span>DIGITAL COMICS</span>
      </div>
      <div class="contImgText">
        <div class="contImg">
          <img
            src="/src/assets/ecommercePhoto/buy-comics-merchandise.png"
            alt=""
          />
        </div>
        <span>DC MERCHANDISE</span>
      </div>
      <div class="contImgText">
        <div class="contImg">
          <img
            src="/src/assets/ecommercePhoto/buy-comics-shop-locator.png"
            alt=""
          />
        </div>
        <span>SUBSCRIPTION</span>
      </div>
      <div class="contImgText">
        <div class="contImg">
          <img
            src="/src/assets/ecommercePhoto/buy-comics-subscriptions.png"
            alt=""
          />
        </div>
        <span>COMIC SHOP LOCATOR</span>
      </div>
      <div class="contImgText">
        <div class="contImg">
          <img src="/src/assets/ecommercePhoto/buy-dc-power-visa.svg" alt="" />
        </div>
        <span>DC POWER VISA</span>
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
    @include flexa("spaceAround");
    .contImgText {
      @include flexa("center-center");
      .contImg {
        height: 3rem;
        width: 2.5rem;
        margin-right: 0.5rem;
      }
      span {
        font-size: 0.8rem;
        color: white;
      }
    }
  }
}
</style>