<script>
import HeaderPage from "../src/components/Header.vue";
import FooterPage from "../src/components/FooterPage.vue";
import ContentPage from "../src/components/ContentPage.vue";
export default {
  name: "App",
  components: {
    HeaderPage,
    FooterPage,
    ContentPage,
  },
};
</script>

<template>
  <HeaderPage />
  <main>
    <ContentPage />
  </main>
  <FooterPage />
</template>

<style lang="scss" >
@import url("./style/general.scss");
</style>
