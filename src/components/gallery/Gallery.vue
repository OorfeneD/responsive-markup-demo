<template>
  <section id="gallery">
    <div class="gallery-container">
      <div class="gallery-title">Customer Gallery</div>
      <div class="gallery-images">
        <div class="gallery-item" v-for="i in 4" :key="i">
          <img :src="`images/gallery-image-${i}.png`" alt="" />
        </div>
      </div>
      <div class="gallery-action">
        <button class="btn btn-main">View More</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
#gallery {
  .gallery-container {
    min-height: 660px;
    padding: 2rem 1ch 3rem 1ch;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    flex-direction: column;
    .gallery-title {
      font-size: 32px;
      font-weight: bold;
      line-height: 1.3em;
      font-family: Helvetica, sans-serif;
    }
    .gallery-images {
      margin: 2rem 0;
      max-width: min(1300px, 100%);
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      .gallery-item {
        img {
          max-width: 310px;
          max-height: 310px;
        }
      }
    }
    @media screen and (max-width: 1300px) {
      .gallery-images {
        grid-template-columns: repeat(2, 1fr);
      }
    }
    @media screen and (max-width: 900px) {
      .gallery-images {
        grid-template-columns: 1fr;
      }
    }
  }
}
</style>
