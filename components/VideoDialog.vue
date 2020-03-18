<template>
  <div class="text-center">
    <v-dialog v-model="dialog" width="660">
      <template v-slot:activator="{ on }">
        <v-btn color="#404b87" dark v-on="on">Click Me</v-btn>
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