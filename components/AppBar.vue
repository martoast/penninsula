<template>
  <div>
    <v-toolbar
      height="55px"
      dark
      v-scroll="onScroll"
      color="transparent"
      flat
      class="mb-6"
    >

      <div class="hidden-md-and-down ma-12">
        <v-card
          class="pa-2"
          outlined
          tile
          color="transparent"
        >
          <div class="hidden-md-and-down">
            <VuetifyLogo />
          </div>
        </v-card>
      </div>
      <v-spacer />

      <v-toolbar-items class="hidden-sm-and-down ma-12">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          :active-class="!isScrolling ? 'primary--text' : undefined"
          text
          @click="$vuetify.goTo(item.scroll)"
        >
          <span v-text="item.text" />
        </v-btn>
      </v-toolbar-items>

    </v-toolbar>
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
          text: "Home",
          scroll: "#home"
        },
        {
          to: "/proyecto",
          text: "Proyecto",
          scroll: "#project"
        },

        {
          to: "/contacto",
          text: "Contacto",
          scroll: "#contact"
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
