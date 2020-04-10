<template>
  <section id="demo">

    <v-toolbar
      color="#404b87"
      dark
      max-height="50"
    >
      <v-container>
        <v-row justify="center">
          <h2 class="title font-weight-light text-center">

            Explora todo lo que ofrece Peninsula!
          </h2>

          <v-btn
            large
            height="25"
            color="white"
            @click="$vuetify.goTo('#contact')"
            light
            class="ml-12"
          >
            Solicitar Info
          </v-btn>

        </v-row>
      </v-container>

    </v-toolbar>

  </section>
</template>
