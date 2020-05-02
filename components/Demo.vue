<template>
  <section id="demo">

    <v-toolbar
      color="#404b87"
      dark
      max-height="63px"
    >
      <v-container>
        <v-row
          justify="center"
          align="center"
        >
          <h2 class="title font-weight-light text-center">

            ¡Todo lo que necesitas a 10 minutos de tu casa!
          </h2>

          <v-btn
            color="white"
            large
            height="40px"
            min-width="175"
            outlined
            rounded
            class="ml-6"
            @click="$vuetify.goTo('#contact')"
          >
            Solicitar Info
          </v-btn>

        </v-row>
      </v-container>

    </v-toolbar>

  </section>
</template>
