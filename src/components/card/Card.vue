<template>
  <section id="card">
    <div class="card">
      <div class="card__image">
        <img src="images/card-image.png" alt="" />
      </div>
      <div class="card__content">
        <div class="card__sub-text">
          Quality Craftmanship from build to delivery
        </div>
        <div class="card__title">Discover the beauty of a handmade kitchen</div>
        <div class="card__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi eget
          est sit amet sapien venenatis maximus vel in urna. Nam mauris arcu,
          feugiat in finibus vitae, sollicitudin id purus. Ut imperdiet, magna
          eu pharetra tincidunt, mauris purus ultrices.
        </div>
        <div class="card__action">
          <button class="btn btn-main">About Us</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
#card {
  .card {
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    --title-size: 42px;
    &__image {
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    &__content {
      padding: clamp(1rem, 2rem, 2vw) clamp(1ch, 4rem, 5vw);
      margin: auto 0;
      max-width: calc(1300px / 2);
      font-size: 15px;
    }
    &__sub-text {
      font-size: 13px;
      color: $button-color;
      text-transform: uppercase;
      letter-spacing: 0.35ch;
      border-bottom: 1em;
    }
    &__title {
      font-size: var(--title-size);
      line-height: 1.2em;
      font-weight: bold;
      font-family: Helvetica, sans-serif;
    }
    &__description {
      line-height: 28px;
      padding: clamp(1ch, 30px, 2vw) 0;
      color: #777;
    }
    @media screen and (max-width: 900px) {
      --title-size: 32px;
      grid-template-columns: auto;
      &__content {
        grid-row: 1;
        text-align: center;
        max-width: 100%;
        padding-left: 1ch;
      }
      &__image {
        grid-row: 2;
      }
    }
  }
}
</style>
