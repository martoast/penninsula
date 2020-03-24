<template>
  <div>
    <v-card
      class="d-flex mb-6"
      color="transparent"
      flat
      height="100vh"
      tile
    >
      <div class="hidden-md-and-down">
        <v-card
          class="pa-2 align-self-start"
          outlined
          tile
          color="transparent"
        >
          <div class="hidden-md-and-down">
            <VuetifyLogoMobile />
          </div>
        </v-card>
      </div>

      <v-card
        class="mx-auto align-self-center"
        outlined
        color="transparent"
        dark
        tile
      >
        <div class="hidden-md-and-up">
          <v-row justify="center">
            <VuetifyLogoMobile />
          </v-row>
        </div>
        <v-row
          justify="center"
          align="center"
        >
          <h1 class="mb-4 display-2 text-center">Primer Lifestyle Mall de Tijuana</h1>
        </v-row>

        <div>
          <v-row
            justify="center"
            align="center"
          >
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

    </v-card>

  </div>
</template>
<script>
import VuetifyLogoMobile from "~/components/VuetifyLogoMobile.vue";
import VideoDialog from "~/components/VideoDialog.vue";
export default {
  components: {
    VuetifyLogoMobile,
    VideoDialog
  },
  data: () => ({
    justify: ["center"]
  })
};
</script>
