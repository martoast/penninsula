<template>
  <div>

    <v-carousel>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
import SectionHeader from "~/components/SectionHeader";
export default {
  components: { SectionHeader },
  data() {
    return {
      items: [
        {
          src: require("@/assets/pen1.png")
        },
        {
          src: require("@/assets/pen2.png")
        },

        {
          src: require("@/assets/pen3.png")
        }
      ]
    };
  }
};
</script>
