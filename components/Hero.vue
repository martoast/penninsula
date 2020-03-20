<template>
  <v-img
    v-if="namespace"
    height="100vh"
    :src="require('@/assets/arialrender.png')"
    class="white--text"
    gradient="to top, rgba(64, 75, 135, 0.5), rgba(25, 25, 38, .85)"
  >
    <!-- <LogoCard /> -->
    <v-container fill-height>
      <v-card class="mx-auto" max-width="800" outlined color="transparent" dark>
        <div>
          <v-row justify="center">
            <VuetifyLogoMobile />
          </v-row>
        </div>
        <v-row justify="center" align="center">
          <h1 class="mb-4 display-2 text-center">Primer Lifestyle Mall de Tijuana</h1>
        </v-row>

        <div>
          <v-row justify="center" align="center">
            <h2 class="title font-weight-light text-center">
              <strong>
                Todo lo que necesitas a
                <br class="hidden-md-and-up" />10 minutos de tu casa.
              </strong>
            </h2>
          </v-row>
        </div>

        <v-row justify="center">
          <h3>
            <strong>Shop | Live | Work | Play</strong>
          </h3>
        </v-row>

        <div class="py-4" />

        <v-row justify="center">
          <v-btn
            class="text--primary my-2"
            color="white"
            large
            min-width="175"
            rounded
            @click="$vuetify.goTo('#contact')"
          >Solicitar Info</v-btn>
        </v-row>
        <v-row justify="center">
          <div>
            <VideoDialog />
          </div>
        </v-row>
      </v-card>
    </v-container>
  </v-img>
</template>

<script>
import VideoDialog from "~/components/VideoDialog.vue";
import LogoCard from "~/components/LogoCard.vue";
import VuetifyLogoMobile from "~/components/VuetifyLogoMobile.vue";
export default {
  components: {
    VideoDialog,
    LogoCard,
    VuetifyLogoMobile
  },
  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
