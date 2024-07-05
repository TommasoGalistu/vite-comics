<script>
export default {
  name: "FinalPartFooter",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <button>SIGN-UP NOW!</button>
      <div class="contLink">
        <span>FOLLOW US</span>
        <img src="/src/assets/footer-facebook.png" alt="" />
        <img src="/src/assets/footer-twitter.png" alt="" />
        <img src="/src/assets/footer-youtube.png" alt="" />
        <img src="/src/assets/footer-pinterest.png" alt="" />
        <img src="/src/assets/footer-periscope.png" alt="" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../style/partials/_mixins.scss" as *;
@use "../../style/partials/variables.scss" as *;
.containerAll {
  background-color: $backGroundColorFooter;
  .mainContainer {
    @include flexa("spaceBetween");
    padding: 2rem 0;

    button {
      background-color: $backGroundColorFooter;
      color: white;
      border: 2px solid blue;
      padding: 0.5rem;

      &:hover {
        cursor: pointer;
        background-color: rgb(39, 42, 146);
      }
    }
    .contLink {
      @include flexa("low-center");
      span {
        color: blue;
      }
      * {
        padding: 0 0.5rem;
      }
    }
  }
}
</style>