<template>
  <div>
    <h1>I am a blog post {{id}}</h1>
    <div>
      <section>
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="6"
            >
              <h2
                :class="[$vuetify.breakpoint.mdAndUp ? 'display-1' : 'headline']"
                class="mb-4"
              >
                Bringing world class Shopping to Tijuana<br />
              </h2>

              <p class="subtitle-1">
                Etiam ultricies nisi vel augue. Nullam cursus lacinia erat. Donec
                vitae orci sed dolor rutrum auctor. Proin pretium, leo ac
                pellentesque mollis, felis nunc ultrices eros, sed gravida augue
                augue mollis justo. Lorem ipsum dolor sit amet, consectetuer
                adipiscing elit. Nullam nulla eros, ultricies sit amet, nonummy
                id, imperdiet feugiat, pede. Etiam rhoncus. Nullam dictum felis eu
                pede mollis pretium. Nullam accumsan lorem in dui. Vestibulum
                ullamcorper mauris at ligula.
              </p>
              <p class="mb-5">
                Praesent porttitor, nulla vitae posuere iaculis, arcu nisl
                dignissim dolor, a pretium mi sem ut ipsum. Donec mollis hendrerit
                risus. Donec vitae sapien ut libero venenatis faucibus. In hac
                habitasse platea dictumst. Donec quam felis, ultricies nec,
                pellentesque eu, pretium quis, sem.
              </p>

              <v-btn
                outlined
                color="primary"
                class="px-5"
                large
              >
                Read More
              </v-btn>
            </v-col>
            <v-col
              cols="12"
              md="5"
              offset-md="1"
            >
              <v-card>
                <v-img
                  :src="require('@/assets/arialrender.png')"
                  height="500"
                >
                </v-img>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </section>
      <section>
        <v-simple-table>
          <template v-slot:default>
            <thead>
              <tr>
                <th class="text-left">zipCode</th>
              </tr>
            </thead>
            <tbody>
              <tr
                v-for="zipCode in zipCodes"
                :key="zipCode"
              >
                <td>{{ zipCode }}</td>

              </tr>
            </tbody>
          </template>
        </v-simple-table>

      </section>
    </div>
  </div>
</template>
<script>
export default {
  created() {
    console.log(this.$route.params.id);
    this.id = this.$route.params.id;
  },
  data: () => ({
    id: null,
    zipCodes: [
      "92101",
      "92102",
      "92103",
      "92104",
      "92105",
      "92106",
      "92107",
      "92108",
      "92109",
      "92110",
      "92111",
      "92112",
      "92113",
      "92114",
      "92115",
      "92116",
      "92117",
      "92119",
      "92120",
      "92121",
      "92122",
      "92123",
      "92124",
      "92126",
      "92127",
      "92128",
      "92129",
      "92130",
      "92131",
      "92132",
      "92133",
      "92134",
      "92135",
      "92136",
      "92137",
      "92138",
      "92139",
      "92140",
      "92142",
      "92145",
      "92147",
      "92149",
      "92150",
      "92152",
      "92153",
      "92154",
      "92155",
      "92158",
      "92159",
      "92160",
      "92161",
      "92162",
      "92163",
      "92164",
      "92165",
      "92166",
      "92167",
      "92168",
      "92169",
      "92170",
      "92171",
      "92172",
      "92174",
      "92175",
      "92176",
      "92177",
      "92179",
      "92182",
      "92184",
      "92186",
      "92187",
      "92190",
      "92191",
      "92192",
      "92193",
      "92194",
      "92195",
      "92196",
      "92197",
      "92198",
      "92199",
      "92118",
      "92143",
      "92173",
      "92178"
    ]
  })
};
</script>
