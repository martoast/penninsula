<template>
  <v-app>
    <AppBar />

    <div>
      <!-- <Jumbrotron /> -->
      <v-img
        src="https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/FashionValley_Hero_Mobile_m4_20191205151447.jpg?yocs=D_H_"
        height="800"
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
    </div>
    <div>
      <Banner />
    </div>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <Footer />
    <div class="hidden-md-and-up">
      <v-container>
        <v-navigation-drawer
          v-model="rightDrawer"
          :right="right"
          temporary
          fixed
          dark
        >
          <v-list>
            <v-list-item
              v-for="item in items"
              :key="item.title"
              :to="item.link"
            >
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>
      </v-container>
    </div>
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
