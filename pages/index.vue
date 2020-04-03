<template>
  <div>
    <v-sheet height="385px">
      <div>
        <v-row justify="center">
          <v-col cols="12">
            <div class="pt-7">
              <SectionHeader
                header="bienvenido a"
                subHeader="Un Destino de
              Experiencias Nuevas."
                text="Península es un desarrollo emergente el cual busca ser un espacio social y de estilo de vida que refleje la identidad única de una Tijuana Cosmopolita conservando el encanto propio de la ciudad."
              />
            </div>
          </v-col>
        </v-row>
      </div>
    </v-sheet>
    <section>
      <v-container>
        <div>
          <div>
            <v-row justify="center">
              <v-col cols="12">
                <div class="pt-7">
                  <SectionHeader subHeader="El mall del futuro es menos retail, más estilo de vida y espacios de entretenimiento." />
                </div>
              </v-col>
            </v-row>
          </div>
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
      </v-container>
    </section>
    <section>
      <About />
    </section>
    <section id="contact">
      <About2 />
    </section>
    <section>
      <div class="elfsight-app-3e870a85-1b3b-472a-abd7-51da13156a0f"></div>
    </section>

  </div>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";
import Services from "~/components/Services.vue";
import Blog from "~/components/Blog.vue";
import Blog2 from "~/components/Blog2.vue";
import Footer from "~/components/Footer.vue";
import SlideGroup from "~/components/SlideGroup.vue";
import Banner from "~/components/Banner.vue";
import SectionHeader from "~/components/SectionHeader.vue";
import SlideGroup2 from "~/components/SlideGroup2.vue";
import About from "~/components/About.vue";
import About2 from "~/components/About2.vue";

export default {
  head() {
    return {
      script: [
        {
          src: "https://apps.elfsight.com/p/platform.js"
        }
      ]
    };
  },
  layout: "landing",
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
  components: {
    Services,
    Footer,
    SlideGroup,
    Blog,
    Blog2,
    Banner,
    SectionHeader,
    SlideGroup2,
    About,
    About2
  },

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
