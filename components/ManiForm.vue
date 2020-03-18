<template>
  <v-container fill-height>
    <div
      class="typeform-widget"
      data-url="https://manny957600.typeform.com/to/Osakva"
      data-transparency="50"
      data-hide-headers="true"
      data-hide-footer="true"
      style="width: 100%; height: 500px;"
    ></div>
    <script>
  (function() {
    var qs,
      js,
      q,
      s,
      d = document,
      gi = d.getElementById,
      ce = d.createElement,
      gt = d.getElementsByTagName,
      id = "typef_orm",
      b = "https://embed.typeform.com/";
    if (!gi.call(d, id)) {
      js = ce.call(d, "script");
      js.id = id;
      js.src = b + "embed.js";
      q = gt.call(d, "script")[0];
      q.parentNode.insertBefore(js, q);
    }
  })();
    </script>
    <v-row justify="center" class="pl-6">
      <div
        style="font-family: Sans-Serif;font-size: 12px;color: #999;opacity: 0.5; padding-top: 5px;"
      >
        powered by
        <a
          href="https://admin.typeform.com/signup?utm_campaign=Osakva&utm_source=typeform.com-01E3KE6N328852226FYJA6JATR-free&utm_medium=typeform&utm_content=typeform-embedded-poweredbytypeform&utm_term=ES"
          style="color: #999"
          target="_blank"
        >Typeform</a>
      </div>
    </v-row>
  </v-container>
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