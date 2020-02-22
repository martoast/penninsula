<template>
  <v-form netlify>
    <v-container fill-height>
      <v-card max-width="400">
        <v-row>
          <v-col cols="12">

            <v-text-field
              label="Your Name*"
              for="name"
              type="text"
              name="name"
              outlined
              required
            />
          </v-col>
          <v-col cols="12">

            <v-text-field
              label="Your Email*"
              for="email"
              type="email"
              name="email"
              required
              outlined
            />
          </v-col>

          <v-col cols="12">

            <v-textarea
              label="Your Message*"
              for="message"
              name="message"
              required
              outlined
            />
          </v-col>

          <v-col text-center>
            <v-btn
              type="submit"
              value="Send message"
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
