<template>
  <section id="demo">
    <v-sheet
      color="primary darken-2"
      dark
      max-height="50"
    >
      <v-container>
        <v-row
          align="center"
          class="text-md-left text-center"
          justify="center"
        >
          <h3 class="headline font-weight-light ">

            Explora todo o que ofrece Peninsula!
          </h3>

          <v-spacer class="hidden-sm-and-down" />

          <v-btn
            large
            height="35"
            rel="noopener"
            rounded
            target="_blank"
            color="white"
            @click="$vuetify.goTo('#contact-us')"
            light
          >
            Solicitar Info
          </v-btn>
        </v-row>
      </v-container>
    </v-sheet>

  </section>
</template>
