<template>
  <div>
    <v-app-bar
      app
      height="65px"
      dark
      v-scroll="onScroll"
      :color="!isScrolling ? '#4C4C4C' : '#404b87'"
      flat
    >
      <v-spacer />

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          :active-class="!isScrolling ? 'primary--text' : undefined"
          :to="item.to"
          text
        >
          <span v-text="item.text" />
        </v-btn>
      </v-toolbar-items>

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

    drawer: null
  }),
  computed: {
    items() {
      return [
        {
          to: "/",
          text: "Home"
        },
        {
          to: "/proyecto",
          text: "Proyecto"
        },

        {
          to: "/contacto",
          text: "Contacto"
        }
      ];
    }
  },

  methods: {
    ...mapMutations(["toggleDrawer"]),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 25;
    }
  }
};
</script>
