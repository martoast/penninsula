<template>
  <div>
    <section class="white">
      <v-container>
        <v-row>
          <v-col cols="12" md="5" offset-md="1">
            <h2 :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']" class="mb-4">
              My name is Alex Martos.
              <br />I want to design your next infrastructure.
            </h2>

            <p
              class="subtitle-1"
            >Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec vitae orci sed dolor rutrum auctor. Proin pretium, leo ac pellentesque mollis, felis nunc ultrices eros, sed gravida augue augue mollis justo. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum ullamcorper mauris at ligula.</p>
          </v-col>
          <v-col cols="12" md="6">
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
