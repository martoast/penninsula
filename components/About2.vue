<template>
  <div>
    <section class="white">
      <v-container>
        <v-row>
          <v-col cols="12" md="6">
            <Cards />
          </v-col>

          <v-col cols="12" md="4" offset-md="1">
            <div>
              <div>
                <ManiForm />
              </div>
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
import ManiForm from "~/components/ManiForm.vue";
export default {
  components: { Cards, netlify, ManiForm },
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
