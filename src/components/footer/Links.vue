<template>
  <div class="links-block">
    <div class="links-block__title">{{ title }}</div>
    <div v-if="socials" class="links-block__items links-block__items--socials">
      <div v-for="(item, i) in items" :key="i" class="links-block__item">
        <div class="links-block__item">
          <font-awesome-icon :icon="item" />
        </div>
      </div>
    </div>
    <div v-else class="links-block__items">
      <div v-for="(item, i) in items" :key="i" class="links-block__item">
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import {
  faFacebookF,
  faTwitter,
  faInstagram,
} from "@fortawesome/free-brands-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
library.add(faFacebookF, faTwitter, faInstagram);

export default {
  components: { FontAwesomeIcon },
  props: {
    socials: {
      type: Boolean,
      default: false,
    },
    title: {
      type: String,
      default: "Title",
    },
    items: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss">
.links-block {
  max-width: 200px;
  &__title {
    font-size: 24px;
    line-height: 1.75em;
    font-family: Helvetica, sans-serif;
    padding-bottom: 1em;
    font-weight: bold;
  }
  &__items {
    font-size: 13px;
    line-height: 2.3em;
    letter-spacing: 0.35ch;
    text-transform: uppercase;
    &--socials {
      display: flex;
      gap: 1ch;
      line-height: unset;
      letter-spacing: unset;
      div {
        width: 40px;
        height: 40px;
        border-radius: 100%;
        background-color: $white;
        color: black;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
      }
    }
  }
}
</style>
