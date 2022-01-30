<template>
  <div class="order-block">
    <button class="order btn btn-alt">
      <span class="order__text">My order</span>
      <font-awesome-icon :icon="['fas', 'shopping-cart']" />
    </button>
  </div>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faShoppingCart } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
library.add(faShoppingCart);

export default {
  components: {
    FontAwesomeIcon,
  },
};
</script>

<style></style>
