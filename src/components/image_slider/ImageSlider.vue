<template>
  <section id="slider">
    <Splide
      class="slider"
      :options="{
        type: 'loop',
        height: 'min(900px, 100vh)',
        arrows: false,
        classes: {
          pagination: 'splide__pagination slider__pagination',
        },
        autoplay: true,
      }"
    >
      <SplideSlide class="slider__slide">
        <div class="slider__content">
          <div class="slider__sub-text">
            Design and order your new kitchen online today
          </div>
          <div class="slider__title">
            Bespoke & made to measure handmade kitchen design
          </div>
          <div class="slider__action">
            <button class="btn btn-main">Order now</button>
          </div>
        </div>
        <img class="slider__image" src="images/slider-image-1.png" alt="" />
      </SplideSlide>
      <SplideSlide class="slider__slide">
        <div class="slider__content">
          <div class="slider__sub-text">
            Design and order your new kitchen online today
          </div>
          <div class="slider__title">
            Bespoke & made to measure handmade kitchen design
          </div>
          <div class="slider__action">
            <button class="btn btn-main">Order now</button>
          </div>
        </div>
        <img class="slider__image" src="images/slider-image-1.png" alt="" />
      </SplideSlide>
      <SplideSlide class="slider__slide">
        <div class="slider__content">
          <div class="slider__sub-text">
            Design and order your new kitchen online today
          </div>
          <div class="slider__title">
            Bespoke & made to measure handmade kitchen design
          </div>
          <div class="slider__action">
            <button class="btn btn-main">Order now</button>
          </div>
        </div>
        <img class="slider__image" src="images/slider-image-1.png" alt="" />
      </SplideSlide>
    </Splide>
    <div class="slider-actions">
      <span class="active"></span><span></span><span></span>
    </div>
  </section>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import "@splidejs/splide/dist/css/themes/splide-default.min.css";

export default {
  components: { Splide, SplideSlide },
};
</script>

<style lang="scss">
#slider {
  height: min(900px, 100vh);
  --title-size: 52px;
  @media screen and (max-width: 1300px) {
    --title-size: 36px;
  }
  div {
    width: 100%;
  }
  overflow: hidden;
  .slider__pagination {
    padding-bottom: 1rem;
    li {
      margin: 0.25rem;
    }
    .splide__pagination__page {
      width: 50px;
      height: 5px;
      border-radius: 10px;
      background-color: white;
      :hover {
        background-color: $text-color;
      }
    }
    .splide__pagination__page.is-active {
      transform: none;
      background-color: $button-color;
    }
  }
  .slider {
    &__image {
      position: absolute;
      top: 0;
      z-index: -1;
      height: inherit;
      object-fit: cover;
      height: min(900px, 100vh);
      width: 100%;
      filter: brightness(0.5);
    }
    &__slide {
      padding-top: 3rem;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__content {
      color: $white;
      text-align: center;
      width: calc(700px + 1ch);
      z-index: 20;
      padding: 0 1ch;
    }
    &__sub-text {
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 3px;
      line-height: 1.15em;
    }
    &__title {
      font-family: Helvetica, sans-serif;
      font-size: var(--title-size);
      font-weight: bold;
      line-height: 1.15em;
      letter-spacing: -1px;
      padding-bottom: 35px;
    }
  }
  .slider-actions {
    position: absolute;
  }
}
</style>
