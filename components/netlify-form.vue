<template>
  <v-form netlify>
    <v-container fill-height>
      <v-card max-width="400">
        <v-row>
          <v-col cols="12">
            <v-text-field outlined label="Your Name*" type="text" name="name" v-model="form.name" />
          </v-col>
          <v-col cols="12">
            <v-text-field
              outlined
              label="Your Email*"
              type="email"
              name="email"
              v-model="form.email"
            />
          </v-col>

          <v-col cols="12">
            <v-textarea outlined label="Your Message" v-model="form.message" />
          </v-col>

          <v-col text-center>
            <v-btn
              type="submit"
              @click.prevent="handleSubmit"
              :block="$vuetify.breakpoint.smAndDown"
              class="px-5 text-capitalize"
              color="secondary"
              large
            >Send</v-btn>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </v-form>
</template>


<script>
export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: ""
      }
    };
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join("&");
    },
    handleSubmit() {
      fetch("/", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body: this.encode({ "form-name": "contact", ...this.form })
      })
        .then(() => alert("Success!"))
        .catch(error => alert(error));
    }
  }
};
</script>