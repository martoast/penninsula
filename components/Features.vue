<template>
  <div>

    <v-container class="text-center">

      <v-row>
        <v-col
          v-for="({ icon, title, text }, i) in features"
          :key="i"
          cols="12"
          md="4"
        >
          <v-card
            class="py-12 px-4"
            flat
          >
            <v-theme-provider dark>
              <div>
                <v-avatar
                  color="#71A5D6"
                  size="88"
                >
                  <v-icon
                    large
                    v-text="icon"
                  ></v-icon>
                </v-avatar>
              </div>
            </v-theme-provider>

            <v-card-title
              class="justify-center font-weight-black text-uppercase"
              v-text="title"
            ></v-card-title>

            <v-card-text
              class="subtitle-1"
              v-text="text"
            >
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

  </div>
</template>
<script>
export default {
  data() {
    return {
      features: [
        {
          icon: "mdi-account",
          title: "Nivel Socio Economico",
          text: "A / B"
        },
        {
          icon: "mdi-account-group-outline",
          title: "Afluencia Promedio",
          text: "10 millones de personas al año 27,000 persona al día."
        },
        {
          icon: "mdi-account",
          title: "Amenidades",
          text:
            "Estacionamiento 3,400 cajones 45,000 m2 de áreas comunes 3 parques"
        },
        {
          icon: "mdi-movie",
          title: "Entretenimiento",
          text:
            "Cinepolis 15 salas (incluye VIP), arcadias, boliche, pista de patinaje, gimnasio, centro acquatico, spa, y mucho más."
        },

        {
          icon: "mdi-shopping",
          title: "Area de Shopping",
          text: "64,000 m2 de fast fashion 21,000 m2 de Liverpool"
        },
        {
          icon: "mdi-home-modern",
          title: "Hotel",
          text: "de 180 habitaciones"
        },
        {
          icon: "mdi-food",
          title: "Destino Gastronomico",
          text:
            "Sed ut elementum justo. Suspendisse non justo enim. Vestibulum cursus mauris dui, a luctus ex blandit. Lorem ipsum dolor sit amet consectetur adipisicing elit. qui ipsum eveniet facilis obcaecati corrupti consectetur adipisicing elit."
        },
        {
          icon: "mdi-home-modern",
          title: "Oficinas y  Departamentos",
          text: "Torre oficina 10,000+ m2 y 180+ departamentos"
        },
        {
          icon: " mdi-football",
          title: "Vida Activa",
          text:
            "Cinepolis 15 salas (incluye VIP), arcadias, boliche, pista de patinaje, gimnasio, centro acquatico, spa, y mucho más."
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
