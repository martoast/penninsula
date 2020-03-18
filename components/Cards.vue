<template>

  <v-container fluid>
    <v-row dense>
      <v-col
        v-for="card in cards"
        :key="card.title"
        :cols="card.flex"
      >
        <v-card class="mx-auto">
          <v-img
            :src="card.src"
            class="white--text align-end"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            min-height="200px"
            max-height="300px"
          >
            <!-- <v-card-title v-text="card.title"></v-card-title> -->
          </v-img>

        </v-card>
      </v-col>
    </v-row>
  </v-container>

</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Favorite road trips",
        src: require("@/assets/arialrender.png"),
        flex: 12
      },
      {
        title: "Pre-fab homes",
        src: require("@/assets/COMINGSOON.jpg"),
        flex: 12
      }
    ]
  })
};
</script>
