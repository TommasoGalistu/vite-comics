<script>
import { links } from "../data/menuHeader";
export default {
  name: "HeaderPage",
  data() {
    return {
      links,
    };
  },
  methods: {
    activeLink(activeBool) {
      for (let i = 0; i < this.links.length; i++) {
        this.links[i].current = false;
      }
      activeBool.current = true;
    },
  },
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contImg">
        <img src="/src/assets/dc-logo.png" alt="logo dc" />
      </div>

      <ul>
        <li
          :class="{ active: link.current }"
          v-for="(link, index) in links"
          :key="index"
          @click="activeLink(link)"
        >
          {{ link.text }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins.scss" as *;
@use "../style/partials/_variables.scss" as *;
.containerAll {
  background-color: $sfondoHeader;
  .mainContainer {
    @include flexa("spaceBetween");
    @include flexa("low-center");
    .contImg {
      height: 4.5rem;
    }
    ul {
      @include flexa();

      li {
        padding: 3rem 0;
        margin: 0 0.5rem;
        font-size: 0.6rem;
        border-bottom: 4px solid white;

        &:hover {
          cursor: pointer;
        }

        //   debug
      }
      li.active {
        border-bottom: 4px solid blue;
        color: blue;
      }
    }
  }
}
</style>