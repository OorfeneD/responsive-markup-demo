<template>
  <footer>
    <div class="footer-container">
      <div class="logo-container">
        <div class="line"></div>
        <Logo />
        <div class="line"></div>
      </div>
      <div class="links">
        <links
          title="About"
          :items="['Shop', 'Plan my kitchen', 'About us', 'Gallery']"
        />
        <links
          title="Service"
          :items="['FAQ', 'Contact', 'How to buy', 'Downloads']"
        />
        <links title="Info" :items="['Delivery', 'Terms', 'Privacy']" />
        <links
          title="Follow"
          :socials="true"
          :items="[
            ['fab', 'facebook-f'],
            ['fab', 'twitter'],
            ['fab', 'instagram'],
          ]"
        />
      </div>
      <div class="special-info">
        <p>Copyright Online MTC Home Kitchens 2018 - All rights reserved.</p>
        <p>Responsive website design, Development & Hosting by mtc.</p>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from "../shared/Logo.vue";
import Links from "../footer/Links.vue";

export default {
  components: { Logo, Links },
};
</script>

<style lang="scss">
footer {
  background-image: url("/images/footer-back.png");
  background-position: center;
  background-size: cover;
  color: $white;
  .footer-container {
    padding: 40px 1ch 3rem 1ch;
    border-bottom: 1px solid rgba($color: #fff, $alpha: 0.2);
    margin-bottom: 3.5rem;
    .logo-container {
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      gap: 20px;
      .line {
        border-bottom: 1px solid rgba($color: #fff, $alpha: 0.2);
        margin: auto;
        height: 0px;
      }
    }
    .links {
      display: flex;
      justify-content: center;
      align-items: top;
      flex-wrap: wrap;
      gap: 20px;
      padding: 2rem 0 2.5rem 0;
    }
    .special-info {
      text-align: center;
      font-size: 13px;
      line-height: 2em;
      opacity: 0.5;
    }
    @media screen and (max-width: 900px) {
      .links {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        .links-block {
          margin: 0 auto;
        }
      }
    }
    @media screen and (max-width: 500px) {
      .links {
        text-align: center;
        display: grid;
        grid-template-columns: 1fr;
        .links-block__items--socials {
          justify-content: center;
        }
      }
    }
  }
}
</style>
