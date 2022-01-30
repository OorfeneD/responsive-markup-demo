<template>
  <div class="socials">
    <font-awesome-icon :icon="['fab', 'facebook-f']" />
    <font-awesome-icon :icon="['fab', 'twitter']" />
    <font-awesome-icon :icon="['fab', 'instagram']" />
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
};
</script>

<style></style>
