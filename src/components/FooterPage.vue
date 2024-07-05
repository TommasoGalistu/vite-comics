<script>
import FinalPartFooter from "./footerComponent/FinalPartFooter.vue";
import PolicyPart from "./footerComponent/PolicyPart.vue";
import UpPartFooter from "./footerComponent/UpPartFooter.vue";
export default {
  name: "FooterPage",
  components: {
    FinalPartFooter,
    PolicyPart,
    UpPartFooter,
  },
};
</script>

<template>
  <h1>Footer</h1>
  <UpPartFooter />
  <PolicyPart />
  <FinalPartFooter />
</template>

<style lang="scss" scoped>
</style>