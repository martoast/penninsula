<template>
  <v-app dark>

    <v-app-bar
      fixed
      app
    >
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn to="/">
          Home
        </v-btn>
        <v-btn to="/about">
          About
        </v-btn>

        <v-btn to="/contact">
          Contact
        </v-btn>

      </v-toolbar-items>

    </v-app-bar>
    <div>
      <v-parallax
        dark
        src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
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
          </div>

          <netlify />

        </v-row>
      </v-parallax>
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
