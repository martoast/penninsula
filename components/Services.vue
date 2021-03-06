<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-tabs
          background-color="transparent"
          centered
          class="mb-5"
          show-arrows
        >
          <v-tab
            v-for="(category, i) in categories"
            :key="i"
            @click="select(category)"
          >
            <span v-text="category.text" />
          </v-tab>
        </v-tabs>

        <v-responsive min-height="700">
          <v-container>

            <v-item-group>
              <v-container>
                <v-row>
                  <v-col
                    v-for="project in computedProjects"
                    :key="project.img"
                    class="gallery-card"
                    cols="12"
                    md="4"
                  >
                    <v-hover>
                      <template v-slot="{ hover }">
                        <v-card
                          class="white--text overflow-hidden"
                          dark
                          height="300"
                          hover
                          @click="overlay = project.img"
                        >
                          <v-img
                            src="https://picsum.photos/510/300?random"
                            height="100%"
                          >

                          </v-img>
                          <v-fade-transition>
                            <v-overlay
                              v-if="hover"
                              absolute
                            >
                              <v-icon large>
                                mdi-magnify
                              </v-icon>
                            </v-overlay>
                          </v-fade-transition>
                          <v-slide-y-reverse-transition>
                            <v-footer
                              v-if="hover"
                              absolute
                              class="justify-center"
                              height="75"
                            >
                              <div class="heading">
                                {{ project.name }}
                              </div>
                            </v-footer>
                          </v-slide-y-reverse-transition>
                        </v-card>
                      </template>
                    </v-hover>
                  </v-col>
                </v-row>
              </v-container>
            </v-item-group>

          </v-container>
        </v-responsive>

        <v-fade-transition mode="out-in">
          <v-overlay
            v-if="overlay"
            fixed
            opacity=".9"
          >
            <v-btn
              color="transparent"
              depressed
              fab
              fixed
              large
              right
              top
              @click="overlay = false"
            >
              <v-icon large>
                mdi-close
              </v-icon>
            </v-btn>

            <v-img
              src="https://picsum.photos/510/300?random"
              width="800"
              max-width="90vw"
            />
          </v-overlay>
        </v-fade-transition>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    category: null,
    categories: [
      {
        text: "All Services",
        filter: null
      },
      {
        text: "Skyscrapers",
        filter: 1
      },
      {
        text: "Government",
        filter: 2
      },
      {
        text: "Customized",
        filter: 3
      }
    ],
    overlay: false,
    projects: [
      {
        name: "Project 1",
        img: "project1.png",
        categories: [1, 3]
      },
      {
        name: "Project 2",
        img: "project2.png",
        categories: [2, 3]
      },
      {
        name: "Project 3",
        img: "project3.png",
        categories: [4, 3]
      },
      {
        name: "Project 4",
        img: "project4.png",
        categories: [1, 2]
      },
      {
        name: "Project 5",
        img: "project5.png",
        categories: [2, 4]
      },
      {
        name: "Project 6",
        img: "project6.png",
        categories: [1, 4]
      }
    ]
  }),

  computed: {
    computedProjects() {
      return !this.category
        ? this.projects
        : this.projects.filter(p => p.categories.includes(this.category));
    }
  },

  methods: {
    select(category) {
      this.category = category.filter;
    }
  }
};
</script>

<style scoped>
.gallery-card {
  transform-origin: center center 0;
  transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1);
}

.fade-transition-leave,
.fade-transition-leave-active,
.fade-transition-leave-to {
  display: none;
}
</style>
