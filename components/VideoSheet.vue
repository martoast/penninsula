<template>
  <div>
    <div class="pt-8 pb-8">
      <SectionHeader
        subHeader="'El mall del futuro es menos retail, más estilo de vida y espacios de entretenimiento.'"
        text="-Ba"
      />
    </div>

    <section class="grey lighten-3">

      <v-container>

        <v-row
          align="center"
          justify="space-around"
        >
          <v-col
            cols="12"
            md="5"
            offset-xl="1"
          >

            <div class="ma-12">
              <v-row justify="center">

                <p class="subtitle-1">
                  Península es un desarrollo emergente el cual busca ser un espacio social y de estilo de vida que refleje la identidad única de una Tijuana Cosmopolita conservando el encanto propio de la ciudad.
                </p>

                <v-btn
                  outlined
                  color="#BF9B2A"
                  class="px-5"
                  x-large
                  @click="$vuetify.goTo('#contact')"
                >
                  Solicitar Info
                </v-btn>

              </v-row>

            </div>

          </v-col>

          <v-col
            cols="12"
            md="5"
          >
            <div>

              <v-img
                :src="require('@/assets/arialrender.png')"
                gradient="to top, rgba(64, 75, 135, 0.5), rgba(25, 25, 38, .85)"
              >
                <v-card
                  height="100%"
                  color="transparent"
                  class="d-flex pb-12 justify-center"
                >
                  <v-row
                    align="center"
                    justify="center"
                  >
                    <div>
                      <VideoDialog2 />
                    </div>

                  </v-row>

                </v-card>

              </v-img>

              <!-- <iframe
                  style="top:55px; left:0; bottom:0; right:0; height: 400px; border:none; margin:0; padding:0; z-index:999999;"
                  src="https://player.vimeo.com/video/408693447"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                  width="100%"
                ></iframe> -->

            </div>

          </v-col>
        </v-row>
      </v-container>
    </section>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
import VideoDialog2 from "~/components/VideoDialog2.vue";
export default {
  components: { SectionHeader, VideoDialog2 },
  data() {
    return {};
  }
};
</script>
<style scoped>
.videoParagraph {
  padding-right: 12px;
}
</style>
