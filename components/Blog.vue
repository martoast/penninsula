<template>
  <div>
    <v-container pt-12>
      <v-card class="mx-auto">

        <v-container
          fluid
          pt-6
        >
          <v-row dense>
            <v-col
              v-for="card in cards"
              :key="card.title"
              :cols="card.flex"
            >
              <v-card>
                <v-img
                  :src="card.src"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  max-height="550px"
                  min-height="300"
                >
                  <v-card-title v-text="card.title"></v-card-title>
                </v-img>

              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-card>

    </v-container>

  </div>

</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Best dining in town",
        src:
          "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/Spot-4_Mobile_m4_20191104111144.jpg?yocs=D_H_",
        flex: 12
      },
      {
        title: "New Styles",
        src:
          "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/LUXE_Spot-2_d4_20191029120312.jpg?yocs=D_H_",
        flex: 6
      },
      {
        title: "Exclusives",
        src:
          "https://cdn-us-ec.yottaa.net/555a305b2bb0ac71b9002d22/8da650303f06013513b1026173a6dedd.yottaa.net/v~4b.1a3.0.0/htmlcontent/NEW-NEXT-Spot-1_Mobile_m4_20191202142201.jpg?yocs=D_H_",
        flex: 6
      }
    ]
  })
};
</script>
