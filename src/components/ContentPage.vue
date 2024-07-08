<script>
import CardImage from "./CardImage.vue";
export default {
  name: "ContentPage",
  data() {
    return {
      images: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
      // BONUS
      // datiFetch: [],
    };
  },
  components: {
    CardImage,
  },
  mounted() {
    // BONUS
    // fetch("/src/data/dc-comics-2.json")
    //   .then((response) => {
    //     console.log("Raw response:", response);
    //     if (!response.ok) {
    //       throw new Error("ERROOR");
    //     }
    //     return response.text();
    //   })
    //   .then((text) => {
    //     console.log("TESTO:", text);
    //     return JSON.parse(text);
    //   })
    //   .then((data) => {
    //     this.datiFetch = data;
    //     console.log("Dati caricati:", this.datiFetch);
    //   })
    //   .catch((error) => console.error("Errore nel caricamento", error));
  },
};
</script>

<template>
  <div class="containerAll">
    <div class="contImg">
      <div class="immagineJumbo"></div>
    </div>
    <div class="mainContainer">
      <div class="button">
        <span class="bottone"><strong>CURRENT SERIES</strong></span>
      </div>
      <div class="containerCard">
        <CardImage
          v-for="(photo, index) in images"
          :key="index"
          :path="photo.thumb"
          :title="photo.series.toUpperCase()"
        />
      </div>
      <div class="viewContinue">
        <span class="bottone"><strong>LOAD MORE</strong></span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/_mixins.scss" as *;
@use "../style/partials/variables.scss" as *;

.containerAll {
  background-color: black;
  color: white;

  .contImg {
    .immagineJumbo {
      height: 20rem;
      width: 100%;
      background-image: url("../assets/jumbotron.jpg");
      background-size: cover;
    }
  }
  .mainContainer {
    position: relative;
    .button {
      position: absolute;
      top: -10px;
    }
    .containerCard {
      width: 100%;
      padding: 3rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      gap: 1rem;
    }
    .viewContinue {
      text-align: center;
      padding-bottom: 2rem;
    }
  }
  .bottone {
    padding: 1rem;
    background-color: #0282f9;

    &:hover {
      cursor: pointer;
      background-color: #67b3fa;
    }
  }
}
</style>