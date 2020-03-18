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
              <h2
                :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
                class="mb-8"
              >
                My name is Alex Martos.
                <br />I want to design your next infrastructure.
              </h2>

              <p class="subtitle-1">Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec vitae orci sed dolor rutrum auctor. Proin pretium, leo ac pellentesque mollis, felis nunc ultrices eros, sed gravida augue augue mollis justo. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum ullamcorper mauris at ligula.</p>

            </div>

          </v-col>

        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import Cards from "~/components/Cards.vue";
export default {
  components: { Cards },
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
