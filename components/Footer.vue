<template>
  <div>
    <div>

      <v-footer
        dark
        height="auto"
        padless
        color="#404b87"
      >
        <v-card
          flat
          tile
          class="white--text text-center"
          color="#404b87"
          width="100%"
        >
          <v-card-text>
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-4 white--text"
              icon
            >
              <v-icon size="24px">{{ icon }}</v-icon>
            </v-btn>
          </v-card-text>

        </v-card>
        <v-card
          class="flex"
          flat
          tile
          color="#404b87"
        >
          <v-card-title>

            <ul class="body-1 pl-0">
              <li
                v-for="(c, i) in company"
                :key="i"
                class="mb-3"
              >
                <a
                  class="transition-swing"
                  v-text="c.title"
                  :href="c.link"
                />
              </li>
            </ul>

            <v-spacer></v-spacer>

            <v-col
              v-for="([icon, info1, info2], i) in details"
              :key="i"
              cols="12"
              md="3"
            >
              <div class="hidden-md-and-down">
                <div class="text-center">
                  <v-icon
                    size="64"
                    class="mb-3"
                    v-text="icon"
                  />
                  <div
                    class="mb-2 headline"
                    v-text="info1"
                  />
                  <div v-text="info2" />
                </div>

              </div>

            </v-col>

          </v-card-title>

        </v-card>

      </v-footer>
    </div>

  </div>
</template>

<script>
export default {
  data: () => ({
    categories: [
      { title: "SEO Services", link: "/seo" },
      { title: "Web Development", link: "/web-development" },
      { title: "E-Commerce", link: "/ecommerce" },
      { title: "Digital Marketing", link: "/payperclick" }
    ],
    company: [
      { title: "Home", link: "/" },
      { title: "Proyecto", link: "/proyecto" },
      { title: "Contacto", link: "/case-studies" },
      { title: "Aviso de Privacidad", link: "/aviso-de-privacidad" },
      { title: "Terminos y Condiciones", link: "/terminos&codiciones" }
    ],
    icons: [
      "mdi-facebook",
      "mdi-twitter",
      "mdi-google-plus",
      "mdi-linkedin",
      "mdi-instagram"
    ],
    details: [
      [
        "mdi-crosshairs-gps",
        "Vía Rápida Oriente 15000",
        "Tijuana, Baja California"
      ],
      ["mdi-email", "", "info@peninsulatijuana.com"],
      ["mdi-phone", "+52 (664) 684 85 40", ""]
    ]
  })
};
</script>

<style lang="sass">
.v-application .v-footer
  ul
    list-style-type: none

    a
      color: white
      text-decoration: none

      &:hover
        color: grey
</style>
