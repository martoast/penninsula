<template>
  <div>
    <v-dialog
      v-model="dialog"
      fullscreen
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="white"
          x-large
          min-width="175"
          outlined
          rounded
          v-on="on"
        >
          <v-icon
            class="pr-1"
            large
          >mdi-play-circle</v-icon> Ver Video
        </v-btn>
      </template>
      <v-toolbar
        dark
        color="#404b87"
      >
        <v-btn
          icon
          dark
          @click="dialog = false"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>

      </v-toolbar>

      <div>
        <div align="center">
          <iframe
            style="position:fixed; top:55px; left:0; bottom:0; right:0; width:100%; height:100vh; border:none; margin:0; padding:0; z-index:999999;"
            src="https://player.vimeo.com/video/408693447"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </v-dialog>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dialog: false
    };
  }
};
</script>
