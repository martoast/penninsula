<template>
  <v-app>
    <v-img
      :src="require('@/assets/arialrender.png')"
      height="100vh"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    >
      <v-row align="center" justify="center">
        <div>
          <v-container pt-12>
            <netlify />
          </v-container>
        </div>
      </v-row>
    </v-img>

    <div align="center" class="pt-12">
      <v-sheet>
        <iframe
          width="90%"
          height="720"
          src="https://www.youtube.com/embed/8MKyyGD9sys"
          frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </v-sheet>
    </div>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-img
      :src="require('@/assets/2.jpg')"
      height="100vh"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    ></v-img>

    <Footer />
  </v-app>
</template>

<script>
import Footer from "~/components/Footer.vue";
import netlify from "~/components/netlify-form.vue";
import AppBar from "~/components/AppBar.vue";
import Banner from "~/components/Banner.vue";
import Jumbrotron from "~/components/Jumbrotron.vue";
export default {
  components: { Footer, netlify, AppBar, Banner, Jumbrotron },

  data() {
    return {
      title: "",
      right: true,
      rightDrawer: false,
      fixed: false,
      clipped: false,

      drawer: null,
      menu: [
        { icon: "home", title: "Home", link: "/" },
        { icon: "info", title: "About", link: "/about" },
        { icon: "warning", title: "Contact", link: "/contact" }
      ],
      items: [
        { title: "home", icon: "mdi-view-dashboard", link: "/" },
        { title: "about", icon: "mdi-account", link: "/about" },
        { title: "contact", icon: "mdi-gavel", link: "/contact" }
      ]
    };
  },
  methods: {
    menuItems() {
      return this.menu;
    }
  }
};
</script>
