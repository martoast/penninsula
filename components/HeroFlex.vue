<template>
  <div>

    <v-card
      height="90vh"
      color="transparent"
      class="d-flex pb-12 justify-center"
      flat
      dark
    >
      <v-card
        class="align-self-center"
        color="transparent"
        flat
      >
        <div class="hidden-md-and-up">
          <v-row justify="center">
            <VuetifyLogoMobile />
          </v-row>
        </div>

        <h1 class="mb-4 display-2 text-center">Adios Garitas, ¡Hola Península!</h1>

        <div>
          <v-row
            justify="center"
            align="center"
          >
            <h2 class="title font-weight-light text-center pa-1">
              <strong>
                Centro Comercial de primer nivel

                <!-- <br class="hidden-md-and-up" />Apertura Primavera 2021 -->
              </strong>
            </h2>
          </v-row>
        </div>

        <v-row justify="center">
          <h3>
            <strong>Apertura Primavera 2021</strong>
          </h3>
        </v-row>

        <div class="py-4" />

        <v-row justify="center">
          <v-btn
            class="text--white my-2"
            color="#BF9B2A"
            x-large
            min-width="245"
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
