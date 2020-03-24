<template>
  <section id="demo">
    <v-sheet
      color="primary darken-2"
      dark
      min-height="75"
    >
      <v-container>
        <v-row
          align="center"
          class="text-md-left text-center"
          justify="center"
        >
          <h3 class="headline font-weight-light ">
            Want to see for yourself? Checkout our vast component options!
          </h3>

          <v-spacer class="hidden-sm-and-down" />

          <v-btn
            large
            min-width="128"
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
