<template>
  <div>
    <section class="white">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <Cards />
          </v-col>

          <v-col
            cols="12"
            md="4"
            offset-md="1"
          >
            <div class="pt-6">
              <div class="hidden-md-and-down">
                <br />
                <br />
                <br />
                <br />
                <br />

              </div>

              <h2
                :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
                class="mb-8"
              >
                Un Destino de
                Experiencias
                <br />
              </h2>

              <p class="subtitle-1">Península propone innovar el concepto de entretenimiento utilizando las tradiciones culinarias de la Baja junto cono el auge cultural y artístico que tanto caracteriza el estado.</p>

            </div>

          </v-col>

        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import Cards from "~/components/Cards.vue";
import netlify from "~/components/netlify-form.vue";
export default {
  components: { Cards, netlify },
  data: () => ({
    hover: null,
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
