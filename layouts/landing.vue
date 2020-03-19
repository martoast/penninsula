<template>
  <v-app>
    <AppBar />
    <div>
      <Hero />
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
import AppBar from "~/components/AppBar.vue";
import Banner from "~/components/Banner.vue";
import Jumbrotron from "~/components/Jumbrotron.vue";
import About2 from "~/components/About2.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import VideoDialog from "~/components/VideoDialog.vue";
import Hero from "~/components/Hero.vue";

export default {
  components: {
    Footer,
    netlify,
    AppBar,
    Banner,
    Jumbrotron,
    About2,
    SectionHeader,
    VideoDialog,
    Hero
  },

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
