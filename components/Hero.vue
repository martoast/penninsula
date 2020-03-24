<template>
  <div>
    <v-img
      v-if="namespace"
      height="100vh"
      :src="require('@/assets/arialrender.png')"
      class="white--text"
      gradient="to top, rgba(64, 75, 135, 0.5), rgba(25, 25, 38, .85)"
    >

      <div>
        <HeroFlex />
      </div>

    </v-img>

  </div>

</template>

<script>
import HeroFlex from "~/components/HeroFlex.vue";

import LogoCard from "~/components/LogoCard.vue";

export default {
  components: {
    LogoCard,

    HeroFlex
  },
  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
