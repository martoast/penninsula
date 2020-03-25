<template>
  <div>
    <section class="white">
      <div class="pd-7 pt-7">
        <v-card
          class="d-flex align-center justify-center mb-6"
          flat
          height="350px"
        >
          <v-card
            flat
            class="pa-2"
          >
            <v-container>

              <SectionHeader
                subHeader="Aquí no solo empieza la patria, empieza Península."
                text="Península es un desarrollo emergente el cual busca ser un espacio social y de estilo de vida que refleje la identidad única de una Tijuana Cosmopolita conservando el encanto propio de la ciudad."
              />

            </v-container>

          </v-card>
        </v-card>

      </div>
      <v-container>

        <v-row>

          <v-col
            cols="12"
            md="12"
          >
            <Carrousel />
          </v-col>
        </v-row>

      </v-container>
    </section>
  </div>
</template>

<script>
import Carrousel from "~/components/Carrousel.vue";
import SectionHeader from "~/components/SectionHeader";
export default {
  components: { Carrousel, SectionHeader },
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
