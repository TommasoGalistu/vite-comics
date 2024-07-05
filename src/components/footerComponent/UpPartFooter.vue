<script>
export default {
  name: "UpPartFooter",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contImg">
        <img
          src="/src/assets/ecommercePhoto/buy-comics-digital-comics.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../style/partials/_mixins.scss" as *;
@use "../../style/partials/variables.scss" as *;

.containerAll {
  background-color: #0f82f7;

  .contImg {
    width: 3rem;
  }
}
</style>