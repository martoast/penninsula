<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="660"
    >
      <template v-slot:activator="{ on }">
        <v-btn
          color="white"
          large
          min-width="175"
          outlined
          rounded
          v-on="on"
        >Ver Video</v-btn>
      </template>

      <div>
        <div align="center">
          <iframe
            width="100%"
            height="415"
            src="https://www.youtube.com/embed/UD7axQ9U9Wk"
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
