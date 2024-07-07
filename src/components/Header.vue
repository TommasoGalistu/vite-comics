<script>
export default {
  name: "HeaderPage",
  data() {
    return {
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          current: false,
        },
        {
          text: "COMICS",
          url: "#",
          current: false,
        },
        {
          text: "MOVIES",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "GAMES",
          url: "#",
          current: false,
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          current: false,
        },
        {
          text: "VIDEOS",
          url: "#",
          current: false,
        },
        {
          text: "FANS",
          url: "#",
          current: false,
        },
        {
          text: "NEWS",
          url: "#",
          current: false,
        },
        {
          text: "SHOP",
          url: "#",
          current: false,
        },
      ],
      linkAttivato: {
        index: "",
        boolValue: false,
      },
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