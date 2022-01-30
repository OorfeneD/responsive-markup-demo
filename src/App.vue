<template>
  <Header />
  <image-slider />
  <card />
  <quote-slider />
  <Gallery />
  <Footer />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Logo from "./components/shared/Logo.vue";
import Header from "./components/header/Header.vue";
import ImageSlider from "./components/image_slider/ImageSlider.vue";
import Card from "./components/card/Card.vue";
import QuoteSlider from "./components/quote_slider/QuoteSlider.vue";
import Gallery from "./components/gallery/Gallery.vue";
import Footer from "./components/footer/Footer.vue";

@Options({
  components: {
    Logo,
    Header,
    ImageSlider,
    Card,
    QuoteSlider,
    Footer,
    Gallery,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
}
header,
section,
footer {
  width: 100%;
  display: flex;
  justify-content: center;
  font-family: Roboto, Helvetica, sans-serif;
  div,
  nav {
    width: min(100%, 1300px);
  }
}
/* UI COMPONENTS */
.btn {
  font-size: 15px;
  line-height: 18px;
  border-radius: 9999px;
  padding: 1.4em 3.5em;
  text-transform: uppercase;
  letter-spacing: 0.35ch;
  border: none;
  background-color: white;
  font-family: Roboto, Helvetica, sans-serif;
  transition: all 0.2s ease;
  cursor: pointer;
  user-select: none;
}
.btn-alt {
  background-color: transparent;
  border: 1px solid white;
  color: white;
  &:hover {
    background-color: white;
    color: black;
  }
}
.btn-main {
  background-color: $button-color;
  color: white;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
  &:hover {
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  }
}
/* END UI COMPONENTS */
</style>
