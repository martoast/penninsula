<template>
  <div>
    <v-app-bar
      :clipped-left="clipped"
      color="transparent"
      app
      flat
      hide-on-scroll
      scroll-off-screen
      height="100px"
      dark
    >
      <VuetifyLogo />

    </v-app-bar>

  </div>
</template>

<script>
// Utilities
import { mapMutations } from "vuex";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    VuetifyLogo
  },
  data: () => ({
    isScrolling: false,
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
  }),

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
