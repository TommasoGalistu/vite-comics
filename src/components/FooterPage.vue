<script>
import FinalPartFooter from "./footerComponent/FinalPartFooter.vue";
import PolicyPart from "./footerComponent/PolicyPart.vue";
export default {
  name: "FooterPage",
  components: {
    FinalPartFooter,
    PolicyPart,
  },
};
</script>

<template>
  <h1>Footer</h1>
  <PolicyPart />
  <FinalPartFooter />
</template>

<style lang="scss" scoped>
</style>