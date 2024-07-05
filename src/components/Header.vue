<script>
export default {
  name: "HeaderPage",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contImg">
        <img src="/src/assets/dc-logo.png" alt="logo dc" />
      </div>

      <ul>
        <li v-for="(num, index) in 10" :key="index">{{ num }}</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins.scss" as *;
.containerAll {
  background-color: red;
  .mainContainer {
    @include flexa("spaceBetween");
    .contImg {
      width: 4.5rem;
      @include flexa("low-center");
    }
    ul {
      @include flexa();
      // debag
      background-color: red;

      li {
        padding: 2rem 1rem;
        //   debug
        border-bottom: 2px solid green;
      }
    }
  }
}
</style>