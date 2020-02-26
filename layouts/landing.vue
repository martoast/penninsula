<template>
  <v-app dark>

    <v-app-bar
      fixed
      app
      color="blue-grey"
    >
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn
          to="/"
          text
        >
          Home
        </v-btn>
        <v-btn
          to="/about"
          text
        >
          About
        </v-btn>

        <v-btn
          to="/contact"
          text
        >
          Contact
        </v-btn>

      </v-toolbar-items>

    </v-app-bar>
    <div>

      <!-- <v-parallax
        dark
        src="https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/FashionValley_Hero_Mobile_m4_20191205151447.jpg?yocs=D_H_"
        height="800"
      > -->
      <v-img
        src="https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/FashionValley_Hero_Mobile_m4_20191205151447.jpg?yocs=D_H_"
        height="800"
      >
        <v-row
          align="center"
          justify="end"
          class="`d-flex justify-space-around mb-6`"
        >
          <v-col
            class="text-center"
            cols="12"
          ></v-col>
          <div class="`d-flex justify-space-around mb-6`">
            <v-container pt-12>
              <v-row
                align="center"
                justify="center"
              >
                <v-col
                  class="text-center"
                  cols="12"
                >
                  <h1 class="display-1 font-weight-thin mb-4">Vuetify.js</h1>
                  <h4 class="subheading">Build your application today!</h4>
                </v-col>
              </v-row>
            </v-container>
          </div>
          <div>
            <v-container pt-12>
              <netlify />

            </v-container>
          </div>

        </v-row>

      </v-img>

      <!-- </v-parallax> -->
    </div>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <Footer />

  </v-app>
</template>

<script>
import Footer from "~/components/Footer.vue";
import netlify from "~/components/netlify-form.vue";
export default {
  components: { Footer, netlify },

  data() {
    return {
      title: ""
    };
  }
};
</script>
