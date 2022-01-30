<template>
  <section id="quotes-slider">
    <Splide
      class="slider-container"
      :options="{ gap: '50px', pagination: false, type: 'loop' }"
    >
      <SplideSlide>
        <div class="slider-quote">
          <div class="slider-quote__sub-text">What Our Customers Say</div>
          <div class="slider-quote__title">
            Over 35 years experience designing handmade kitchens
          </div>
          <div class="slider-quote__content">
            Since my first contact I have received a very high level of customer
            service and advice with my kitchen plans. Ben responded very quickly
            to all of my emails and delivery of the kitchen was as planned.
          </div>
          <div class="slider-quote__sign">Jane, Dundee</div>
          <div class="slider-quote__action">
            <button class="btn btn-main">Frequently Asked Questions</button>
          </div>
        </div>
      </SplideSlide>
      <SplideSlide>
        <div class="slider-quote">
          <div class="slider-quote__sub-text">What Our Customers Say</div>
          <div class="slider-quote__title">
            Over 35 years experience designing handmade kitchens
          </div>
          <div class="slider-quote__content">
            Since my first contact I have received a very high level of customer
            service and advice with my kitchen plans. Ben responded very quickly
            to all of my emails and delivery of the kitchen was as planned.
          </div>
          <div class="slider-quote__sign">Jane, Dundee</div>
          <div class="slider-quote__action">
            <button class="btn btn-main">Frequently Asked Questions</button>
          </div>
        </div>
      </SplideSlide>
      <SplideSlide>
        <div class="slider-quote">
          <div class="slider-quote__sub-text">What Our Customers Say</div>
          <div class="slider-quote__title">
            Over 35 years experience designing handmade kitchens
          </div>
          <div class="slider-quote__content">
            Since my first contact I have received a very high level of customer
            service and advice with my kitchen plans. Ben responded very quickly
            to all of my emails and delivery of the kitchen was as planned.
          </div>
          <div class="slider-quote__sign">Jane, Dundee</div>
          <div class="slider-quote__action">
            <button class="btn btn-main">Frequently Asked Questions</button>
          </div>
        </div>
      </SplideSlide>
    </Splide>
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
#quotes-slider {
  --title-size: 32px;
  --content-size: 18px;
  @media screen and (max-width: 900px) {
    --title-size: 24px;
    --content-size: 14px;
  }
  background-color: #eee;
  .slider-container {
    .splide__arrows {
      button {
        background-color: transparent;
        color: $button-color;
        svg {
          fill: $button-color !important;
          display: none;
        }
        width: 50px;
        height: 50px;
        border-radius: 0;
        border-color: $button-color;
        border-left: 2px solid;
        border-bottom: 2px solid;
        transform: rotateZ(45deg);
      }
      .splide__arrow--next {
        transform: rotateZ(225deg);
      }
    }
    .slider-quote {
      min-height: 600px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: auto;
      max-width: min(calc(100% - 8ch), calc(600px + 2ch));
      box-sizing: content-box;
      padding: auto 1ch;
      text-align: center;
      &__sub-text {
        font-size: 13px;
        color: $button-color;
        text-transform: uppercase;
        letter-spacing: 0.25ch;
      }
      &__title {
        font-size: var(--title-size);
        font-weight: bold;
        line-height: 1.3em;
        font-family: Helvetica, sans-serif;
        margin: 1rem 0;
      }
      &__content {
        color: #777;
        font-size: var(--content-size);
        line-height: 1.8em;
        font-family: Helvetica, sans-serif;
      }
      &__sign {
        color: #777;
        font-size: 15px;
        line-height: 1.8em;
        padding-top: 1em;
      }
      &__action {
        padding-top: 30px;
      }
    }
  }
  @media screen and (max-width: 900px) {
    .slider-container {
      .slider-quote {
        min-height: auto;
      }
      padding: clamp(1ch, 2rem, 4vw) 1ch;
    }
  }
}
</style>
