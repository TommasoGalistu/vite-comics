<script>
export default {
  name: "CardImage",
};
</script>

<template>
  <div class="card">
    <img
      src="https://www.coverbrowser.com/image/action-comics/1-1.jpg"
      alt=""
    />
    <span>titolo</span>
  </div>
</template>

<style lang="scss" scoped>
.card {
  height: 14rem;
  background-color: red;
  img {
    height: 80%;
    display: block;
  }

  span {
    display: block;
    padding: 0.8rem 0;
  }
}
</style>