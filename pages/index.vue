<template>
  <div>
    <section>
      <div>
        <v-parallax
          dark
          src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
          height="800"
        >
          <v-row align="center" justify="end">
            <v-col class="text-center" cols="12"></v-col>
            <v-row align="center" justify="center">
              <v-col class="text-center" cols="12">
                <h1 class="display-1 font-weight-thin mb-4">Vuetify.js</h1>
                <h4 class="subheading">Build your application today!</h4>
              </v-col>
            </v-row>
            <v-card>
              <netlify />
            </v-card>
          </v-row>
        </v-parallax>
      </div>
    </section>
    <section>
      <div>
        <iframe
          allowfullscreen="true"
          title="panorama"
          scrolling="no"
          width="100%"
          height="700"
          src="https://kuula.co/share/7lcgK/collection/7fyMs"
          style="border: 0px;"
        ></iframe>
      </div>
    </section>

    <contact />

    <div>
      <Services />
    </div>
  </div>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";
import Services from "~/components/Services.vue";
import Footer from "~/components/Footer.vue";
import netlify from "~/components/netlify-form.vue";
import contact from "~/components/contact.vue";

export default {
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(10) },
    email: { required, email },
    select: { required },
    checkbox: {
      checked(val) {
        return val;
      }
    }
  },
  components: { Services, Footer, netlify, contact },

  data: () => ({
    name: null,
    email: null,
    phone: null,
    select: null,
    items: ["Media", "Store Information", "General Info", "Business"],
    checkbox: false
  }),

  computed: {
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      return errors;
    },
    selectErrors() {
      const errors = [];
      if (!this.$v.select.$dirty) return errors;
      !this.$v.select.required && errors.push("Item is required");
      return errors;
    },
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 10 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    }
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.select = null;
      this.checkbox = false;
    }
  }
};
</script>
