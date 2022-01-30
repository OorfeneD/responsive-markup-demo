<template>
  <div class="menu">
    <div v-if="!logo" class="menu__links">
      <a href="#" class="menu__link">Shop</a>
      <a href="#" class="menu__link">Plan my kitchen</a>
      <a href="#" class="menu__link">About us</a>
      <a href="#" class="menu__link">Gallery</a>
    </div>
    <div v-if="logo" class="menu__links">
      <a href="#" class="menu__link">Shop</a>
      <a href="#" class="menu__link">Plan my kitchen</a>
    </div>
    <div v-if="logo" class="menu__logo">
      <Logo />
    </div>
    <div v-if="logo" class="menu__links">
      <a href="#" class="menu__link">About us</a>
      <a href="#" class="menu__link">Gallery</a>
    </div>
  </div>
</template>

<script>
import Logo from "../shared/Logo.vue";
export default {
  props: {
    logo: {
      type: Boolean,
      default: true,
    },
  },
  components: { Logo },
};
</script>

<style></style>
