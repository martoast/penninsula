<template>
  <v-app>
    <v-img
      :src="require('@/assets/arialrender.png')"
      height="100vh"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    >
      <v-row align="center" justify="center">
        <div class="pt-12">
          <v-container pt-12>
            <v-row justify="center" class="pt-12">
              <v-img :src="require('@/assets/penlogo.png')" max-height="225px" max-width="225px"></v-img>
            </v-row>

            <!-- <netlify /> -->
          </v-container>
        </div>
      </v-row>
      <div>
        <VideoDialog />
      </div>
    </v-img>

    <!-- <div align="center">
      <v-sheet color="#404b87" height="800">
        <br />
        <div align="center" class="pt-12">
          <iframe
            width="90%"
            height="600"
            src="https://www.youtube.com/embed/UD7axQ9U9Wk"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </v-sheet>
    </div>-->

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
export default {
  components: {
    Footer,
    netlify,
    AppBar,
    Banner,
    Jumbrotron,
    About2,
    SectionHeader,
    VideoDialog
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
