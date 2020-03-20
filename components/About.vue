<template>
  <div>
    <section class="white">
      <v-container>
        <v-row>
          <!-- <v-col cols="12" md="5">
            <h2
              :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
              class="mb-4"
            >Aquí no solo empieza la patria, empieza península.</h2>

            <p
              class="subtitle-1"
            >Península es un desarrollo emergente el cual busca ser un espacio social y de estilo de vida que refleje la identidad única de una Tijuana Cosmopolita conservando el encanto propio de la ciudad.</p>
          </v-col>-->
          <v-col cols="12" md="12">
            <Carrousel />
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import Carrousel from "~/components/Carrousel.vue";
export default {
  components: { Carrousel },
  data: () => ({
    src: require("@/assets/COMINGSOON.jpg"),
    highlights: [
      "Architecture development",
      "Cloud computing",
      "Consulting",
      "AWS maintenance",
      "Corporate training",
      "Backend hardening"
    ],
    experiences: [
      ["mdi-vuejs", "75", "Vue"],
      ["mdi-vuetify", "100", "Vuetify"],
      ["mdi-aws", "67", "AWS"],
      ["mdi-server-security", "95", "Security"]
    ]
  })
};
</script>
