<template>
  <v-container id="contact-us">
    <form
      name="contactus"
      action="/thanks"
      method="post"
      netlify
      netlify-honeypot="bot-field"
    >
      <input
        type="hidden"
        name="form-name"
        value="contactus"
      />
      <v-container>
        <v-card
          color="transparent"
          flat
        >
          <!-- <SectionHeader subHeader="Contacto" /> -->
          <v-row>
            <v-col cols="12">
              <div>
                <v-text-field
                  label="Nombre*"
                  for="name"
                  type="text"
                  name="name"
                  outlined
                  required
                  color="#404b87"
                  rounded
                />
              </div>

              <div>
                <v-text-field
                  label="Email*"
                  for="email"
                  type="email"
                  name="email"
                  required
                  outlined
                  color="#404b87"
                  rounded
                />
              </div>

              <div>
                <v-text-field
                  label="Telefono*"
                  for="phone"
                  name="phone"
                  required
                  outlined
                  color="#404b87"
                  rounded
                />
              </div>

              <v-select
                :items="['Busco informacion general.', 'Me interesa un local.', ]"
                label="Motivo de contacto*"
                required
                outlined
                rounded
              ></v-select>

              <div>
                <v-textarea
                  label="Mensaje*"
                  for="message"
                  name="message"
                  required
                  outlined
                  color="#404b87"
                  rounded
                />
              </div>

              <div>
                <v-container>
                  <v-btn
                    type="submit"
                    value="Send message"
                    block
                    dark
                    x-large
                    rounded
                    height="75px"
                    class="alex"
                  >
                    <div class="headline">Agendar una cita</div>
                  </v-btn>
                </v-container>
              </div>

            </v-col>
          </v-row>

        </v-card>
      </v-container>
    </form>
  </v-container>
</template>
<script>
import SectionHeader from "~/components/SectionHeader";

export default {
  components: { SectionHeader },
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
<style scoped>
.alex {
  background-image: linear-gradient(
    to top right,
    #71a5d6 0%,
    #5660c9 51%,
    #343477 100%
  );
}
</style>
