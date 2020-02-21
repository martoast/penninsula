<template>
  <v-app dark>

    <v-app-bar
      :clipped-left="clipped"
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
export default {
  components: { Footer },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: ""
    };
  }
};
</script>
