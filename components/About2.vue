<template>
  <div>
    <section class="white">
      <v-sheet>
        <v-container>
          <v-row>
            <v-col cols="12" md="6">
              <v-container fluid pa-0>
                <v-row>
                  <v-col cols="12" md="6" class="pa-0">
                    <v-card-title>Contact Info</v-card-title>
                    <v-card-text>
                      <div>+1 (321) 383-4531</div>
                      <div>
                        <a href="#">contact@alphaconstruction.com</a>
                      </div>
                      <div>
                        <a href="#">@alphaconstruction</a>
                      </div>
                    </v-card-text>
                  </v-col>

                  <v-col cols="12">
                    <iframe
                      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6996653.320726327!2d-104.56654057311077!3d31.100430144601546!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x864070360b823249%3A0x16eb1c8f1808de3c!2sTexas!5e0!3m2!1sen!2sus!4v1563207206020!5m2!1sen!2sus"
                      width="100%"
                      height="600"
                      frameborder="0"
                      style="border:0"
                      allowfullscreen
                    />
                  </v-col>
                </v-row>
              </v-container>
            </v-col>

            <v-col cols="12" md="5" offset-md="1">
              <div>
                <div>
                  <netlify />
                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-sheet>
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
