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
        <v-row class="ma-0">
          <v-col
            class="py-5 white--text"
            cols="12"
            md="3"
          >
            <h3 class="headline mb-3">Boost Media Inc</h3>
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
          </v-col>
          <v-col
            class="white--text pa-5"
            cols="12"
            md="9"
          >
            <v-row
              class="hidden-sm-and-down"
              justify="end"
            >
              <v-col
                v-for="(category, i) in categories"
                :key="i"
                cols="12"
                md="6"
              >
                <v-btn
                  text
                  v-text="category.title"
                  :to="category.link"
                ></v-btn>
              </v-col>
            </v-row>
          </v-col>

          <v-col
            class="text-center black white--text pa-3"
            cols="12"
          >&copy; 2020 Boost Media Inc — All Rights reserved.</v-col>
        </v-row>
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
