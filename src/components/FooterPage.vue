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
  <UpPartFooter />
  <PolicyPart />
  <FinalPartFooter />
</template>

<style lang="scss" scoped>
</style>