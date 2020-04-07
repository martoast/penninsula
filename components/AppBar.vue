<template>
  <div>
    <v-toolbar
      height="55px"
      dark
      v-scroll="onScroll"
      :color="!isScrolling ? 'transparent' : '#404b87'"
      flat
    >

      <div class="hidden-md-and-down">
        <v-card
          class="pa-2 align-self-start"
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
