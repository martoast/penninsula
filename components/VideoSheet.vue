<template>
  <div class="pt-12">
    <section class="grey lighten-3">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="5"
          >
            <div class="d-flex">

              <v-card
                class="align-self-center pa-2"
                outlined
                tile
              >

                <v-row justify="center">

                  <h2
                    :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
                    class="mb-4"
                  >
                    We use the best platforms around!<br />
                  </h2>

                  <p class="subtitle-1">
                    Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec
                    vitae orci sed dolor rutrum auctor. Proin pretium, leo ac
                    pellentesque mollis, felis nunc ultrices eros, sed gravida augue
                    augue mollis justo. Lorem ipsum dolor sit amet, consectetuer
                    adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy
                    id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu
                    pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum
                    ullamcorper mauris at ligula.
                  </p>

                  <v-btn
                    outlined
                    color="primary"
                    class="px-5"
                    x-large
                    to="/contact"
                  >
                    Contact Us
                  </v-btn>

                </v-row>

              </v-card>

            </div>
          </v-col>
          <v-col
            cols="12"
            md="5"
            offset-md="1"
          >

            <div align="center">
              <iframe
                style="top:55px; left:0; bottom:0; right:0; width:90vh; height: 400px; border:none; margin:0; padding:0; z-index:999999;"
                src="https://www.youtube.com/embed/UD7axQ9U9Wk"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>

          </v-col>
        </v-row>
      </v-container>
    </section>

  </div>
</template>
<script>
export default {
  data() {
    return {};
  }
};
</script>
