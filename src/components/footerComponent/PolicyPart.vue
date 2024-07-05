<script>
export default {
  name: "PolicyPart",
};
</script>

<template>
  <div class="containerAll">
    <div class="mainContainer">
      <div class="contListe">
        <div>
          <h3>DC COMICS</h3>
          <ul>
            <li>Characters</li>
            <li>Comics</li>
            <li>Movies</li>
            <li>TV</li>
            <li>Games</li>
            <li>Videos</li>
            <li>News</li>
          </ul>
          <h3>SHOP</h3>
          <ul>
            <li>Shop DC</li>
            <li>Shop DC Collectibles</li>
          </ul>
        </div>
        <div>
          <h3>DC</h3>
          <ul>
            <li>Terms Of Use</li>
            <li>Pivacy policy(New)</li>
            <li>Ad Choices</li>
            <li>Advertising</li>
            <li>Jobs</li>
            <li>Subsciptions</li>
            <li>Talent Workshops</li>
            <li>CPSC Certificates</li>
            <li>Rating</li>
            <li>Shop Help</li>
            <li>Contact Us</li>
          </ul>
        </div>
        <div>
          <h3>SITES</h3>
          <ul>
            <li>DC</li>
            <li>MAD Magazine</li>
            <li>DC Kids</li>
            <li>DC Universe</li>
            <li>DC Power Visa</li>
          </ul>
        </div>
      </div>
      <div class="contImg"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../style/partials/_mixins.scss" as *;
@use "../../style/partials/variables.scss" as *;

.containerAll {
  background-image: url("/src/assets/dc-logo-bg.png"),
    url("/src/assets/footer-bg.jpg");
  //   background-size: 30% cover;
  background-position-x: 70%;
  background-position-y: center;
  background-repeat: no-repeat, repeat;
  filter: saturate(50%);
  //   background-color: $backGroundColorFooter;

  .mainContainer {
    padding: 1.5rem 0;
    .contListe {
      @include flexa("niente");
      * {
        margin-right: 1rem;
      }
      h3 {
        color: white;
      }
      h3,
      ul {
        margin-bottom: 0.5rem;

        li {
          color: gray;
        }
      }
    }
    .contImg {
      width: 40%;
    }
  }
}
</style>