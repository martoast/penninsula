<template>
  <v-footer
    dark
    height="auto"
    padless
  >
    <v-col
      class="text-center blue-grey darken-4 pa-3"
      cols="12"
    >&copy; 2020 Peninsula — All Rights reserved.</v-col>

  </v-footer>
</template>

<script>
export default {
  data: () => ({
    categories: [
      "Exclusives",
      "Whats'new",
      "Testimonials",
      "Press Room",
      "Partners",
      "New in Tijuana",
      "Macarthy Equipment",
      "Elite Construction Management"
    ],
    company: ["Services", "Projects", "Our Team", "Commitment to the Community"]
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
