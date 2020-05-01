<template>
  <div>
    <div class="hidden-md-and-up">
      <v-list flat>
        <v-list-item-group>
          <v-list-item
            v-for="({ icon, title, text }, i) in FullFeatures"
            :key="i"
          >
            <v-list-item-icon>
              <v-theme-provider light>

                <v-icon large>mdi-checkbox-marked-circle-outline</v-icon>

              </v-theme-provider>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title
                class="font-weight-black headline"
                v-text="title"
              >

              </v-list-item-title>

              <v-list-item-action-text
                v-text="text"
                class="headline"
              ></v-list-item-action-text>

            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </div>

    <div class="hidden-md-and-down">

      <v-item-group multiple>
        <v-container>
          <v-row>
            <v-col
              v-for="n in FullFeatures"
              :key="n.title"
              cols="12"
              md="4"
            >
              <v-item>
                <v-card
                  color="transparent"
                  height="200"
                  flat
                >

                  <v-row justify="center">
                    <v-icon large>mdi-checkbox-marked-circle-outline</v-icon>

                  </v-row>

                  <v-card-title class="justify-center">{{n.title}}</v-card-title>
                  <v-card-text class="justify-center">{{n.text}}</v-card-text>

                </v-card>
              </v-item>
            </v-col>
          </v-row>
        </v-container>
      </v-item-group>

    </div>

  </div>
</template>
<script>
export default {
  data() {
    return {
      features: [
        {
          icon: "mdi-account-group-outline",
          title: "Afluencia Promedio",
          text: "10 millones de personas al año de nivel socioeconómico A/B"
        },
        {
          icon: "mdi-account",
          title: "Shopping",
          text: "64,000 m2 de fast fashion 21,000 m2 de Liverpool"
        },
        {
          icon: "mdi-home-modern",
          title: "Destino Gastronomico",
          text: "Mas de 20 restaurantes & bares foodhall y mercado gourmet"
        }
      ],
      features2: [
        {
          icon: "mdi-shopping",
          title: "Amenidades",
          text: " 3,400 cajones de estacionamiento y 45,000 m2 de áreas comunes"
        },
        {
          icon: "mdi-movie",
          title: "Hotel, Oficinas y  Departamentos",
          text:
            "180 habitaciones de hotel, 10,000 m2 de oficina y 180 departamentos."
        },

        {
          icon: "mdi-food",
          title: "Entretenimiento y Vida Activa",
          text:
            "Cinepolis 15 salas (incluye VIP), gimnasio, centro acquatico, spa,arcadias, boliche, y mucho más"
        }
      ],
      FullFeatures: [
        {
          icon: "mdi-account-group-outline",
          title: "Afluencia Promedio",
          text: "10 millones de personas al año de nivel socioeconómico A/B"
        },
        {
          icon: "mdi-account",
          title: "Shopping",
          text: "64,000 m2 de fast fashion 21,000 m2 de Liverpool"
        },
        {
          icon: "mdi-home-modern",
          title: "Destino Gastronomico",
          text: "Mas de 20 restaurantes & bares foodhall y mercado gourmet"
        },
        {
          icon: "mdi-shopping",
          title: "Amenidades",
          text: " 3,400 cajones de estacionamiento y 45,000 m2 de áreas comunes"
        },
        {
          icon: "mdi-movie",
          title: "Hotel, Oficinas y  Departamentos",
          text:
            "180 habitaciones de hotel, 10,000 m2 de oficina y 180 departamentos."
        },

        {
          icon: "mdi-food",
          title: "Entretenimiento y Vida Activa",
          text:
            "Cinepolis 15 salas (incluye VIP), gimnasio, centro acquatico, spa,arcadias, boliche, y mucho más"
        }
      ],
      stats: [
        ["24k", "Github Stars"],
        ["330+", "Releases"],
        ["1m", "Downloads/mo"],
        ["5m", "Total Downloads"]
      ]
    };
  }
};
</script>
