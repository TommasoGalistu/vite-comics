<script>
export default {
  name: "CardImage",
  props: {
    path: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="path" alt="" />
    <span>{{ title }}</span>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 8rem;
  height: 12rem;
  margin-bottom: 1rem;
  img {
    width: 100%;
    height: 80%;
    display: block;
  }

  span {
    display: block;
    font-size: 0.8rem;
    padding: 0.8rem 0;
  }
}
</style>