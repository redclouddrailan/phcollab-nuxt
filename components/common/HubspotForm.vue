<script>
export default {
  mounted() {
    const script = document.createElement("script");
    script.src = "https://js.hsforms.net/forms/v2.js";
    document.body.appendChild(script);
    script.addEventListener("load", () => {
      if (window.hbspt) {
        window.hbspt.forms.create({
          portalId: "43352783",
          formId: "4858e820-e1fa-4902-9268-883dc2c69501",
          target: "#hubspotForm",
        });
      }
    });
  },
};
</script>
<template>
  <p class="text-purple-950 text-center font-bold text-3xl mb-8">
    Speak with Us!
  </p>
  <div id="hubspotForm" v-once></div>

</template>
