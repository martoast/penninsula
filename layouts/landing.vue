<template>
  <v-app>
    <v-img
      :src="require('@/assets/arialrender.png')"
      height="100vh"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    >
      <v-row
        align="center"
        justify="center"
      >
        <div>
          <v-container pt-12>
            <v-row justify="center">
              <v-img
                :src="require('@/assets/penlogo.png')"
                max-height="100px"
                max-width="100px"
              >
              </v-img>

            </v-row>

            <netlify />
          </v-container>
        </div>
      </v-row>
    </v-img>

    <div align="center">
      <v-img
        :src="require('@/assets/2.jpg')"
        height="100vh"
        gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
      >
        <div
          align="center"
          class="pt-12"
        ><iframe
            width="90%"
            height="600"
            src="https://www.youtube.com/embed/XHOmBV4js_E"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>

      </v-img>

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
export default {
  components: { Footer, netlify, AppBar, Banner, Jumbrotron, About2 },

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
