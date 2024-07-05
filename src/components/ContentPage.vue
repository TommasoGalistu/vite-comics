<script>
export default {
  name: "ContentPage",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <h1>content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins.scss" as *;
@use "../style/partials/variables.scss" as *;

.containerAll {
  background-color: black;
  color: white;
  height: 5rem;
  @include flexa("low-center");
}
</style>