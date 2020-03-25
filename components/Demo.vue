<template>
  <section id="demo">

    <v-toolbar
      color="primary darken-2"
      dark
      max-height="50"
    >
      <v-container>
        <v-row>
          <h2 class="title font-weight-light text-center">

            Explora todo lo que ofrece Peninsula!
          </h2>

          <v-spacer />

          <v-btn
            large
            height="25"
            rounded
            color="white"
            @click="$vuetify.goTo('#contact-us')"
            light
          >
            Solicitar Info
          </v-btn>

        </v-row>
      </v-container>

    </v-toolbar>

  </section>
</template>
