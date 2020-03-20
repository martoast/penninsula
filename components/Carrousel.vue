<template>
  <div>
    <v-sheet height="400px">
      <div>
        <v-row justify="center">
          <v-col cols="12">
            <div class="pd-7 pt-7">
              <SectionHeader
                subHeader="Aquí no solo empieza la patria, empieza península."
                text="Península es un desarrollo emergente el cual busca ser un espacio social y de estilo de vida que refleje la identidad única de una Tijuana Cosmopolita conservando el encanto propio de la ciudad."
              />
            </div>
          </v-col>
        </v-row>
      </div>
    </v-sheet>
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
          src: require("@/assets/COMINGSOON.jpg")
        },
        {
          src: require("@/assets/arialrender.png")
        },

        {
          src: require("@/assets/2.jpg")
        }
      ]
    };
  }
};
</script>