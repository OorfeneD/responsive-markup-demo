<template>
  <header>
    <nav class="nav--desktop">
      <Socials />
      <Menu />
      <OrderButton />
    </nav>
    <nav class="nav--mobile">
      <Menu :logo="false" />
    </nav>
  </header>
</template>

<script>
import Socials from "./Socials.vue";
import OrderButton from "./OrderButton.vue";
import Menu from "./Menu.vue";
export default {
  components: { Socials, OrderButton, Menu },
};
</script>

<style lang="scss">
$button-color: #d4b254;
$border-color: #928f86;
$white: #fff;
header {
  font-size: 13px;
  text-transform: uppercase;
  position: absolute;
  top: 0;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 10;
  .nav--mobile {
    display: none;
  }
  nav {
    color: $white;
    padding: 28px 1px;
    border-bottom: 1px solid $border-color;
    width: min(100%, 1300px);
    display: grid;
    grid-template-columns: 200px auto 200px;
    gap: 60px;
    .menu {
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      &__links {
        flex-grow: 1;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: clamp(1ch, 35px, 5vw);
        letter-spacing: 0.3ch;
      }
      &__link {
        width: max-content;
        text-decoration: none;
        border: none;
        color: inherit;
        :hover,
        :visited {
          color: inherit;
        }
      }
      &__logo {
        flex-grow: 0;
        // display: flex;
        // align-items: center;
        margin: auto 0;
      }
    }
    .socials {
      display: flex;
      gap: 1ch;
      align-items: center;
      padding-left: 1em;
      font-size: 16px;
      margin-right: auto;
    }
    .order-block {
      .order {
        margin-left: auto;
        display: block;
        &__text {
          padding-right: 1ch;
        }
      }
    }
    .socials,
    .order-block {
      flex-grow: 0;
      button {
        font-size: 13px;
        line-height: 15px;
      }
    }
  }
  @media screen and (max-width: 1300px) {
    nav {
      padding: clamp(1ch, 1rem, 2vw) 1ch;
    }
    .nav--desktop {
      grid-template-columns: 1fr auto 1fr;
      gap: clamp(1ch, 2rem, 5vw);
      .menu {
        grid-template-columns: auto;
        &__links {
          display: none;
        }
        &__logo {
          width: fit-content;
          margin: auto;
        }
      }
      .socials {
        font-size: 1.5em;
      }
      .order-block {
        .btn {
          padding: 1em;
        }
        .order__text {
          display: none;
        }
      }
    }
    .nav--mobile {
      display: block;
      .menu {
        margin: auto;
        display: block;
      }
    }
  }
  @media screen and (max-width: 650px) {
    .nav--desktop {
      display: flex;
      justify-content: center;
    }
    .nav--mobile,
    .socials,
    .order-block {
      display: none !important;
    }
  }
}
</style>
