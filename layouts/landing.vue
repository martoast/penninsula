<template>
  <v-app>
    <v-app-bar
      :clipped-left="clipped"
      color="blue-grey"
      fixed
      app
    >
      <v-toolbar-title>Peninsula Version 0.7</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="item in menu"
          :key="item.icon"
          :to="item.link"
          text
        >{{ item.title }}</v-btn>
      </v-toolbar-items>

      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
        class="hidden-md-and-up"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>

    <div>

      <v-img
        src="https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/FashionValley_Hero_Mobile_m4_20191205151447.jpg?yocs=D_H_"
        height="800"
      >
        <v-row
          align="center"
          justify="center"
        >

          <div>
            <v-container pt-12>
              <netlify />

            </v-container>
          </div>

        </v-row>

      </v-img>

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
        >
          <v-list>
            <v-list-item @click.native="right = !right">

              <v-list-item-title>shit</v-list-item-title>
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
export default {
  components: { Footer, netlify },

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
