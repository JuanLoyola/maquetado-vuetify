<template>
  <v-main v-if="showAlert">
    <v-container white class="newsletter-alert max-width-xs">
      <v-row>
        <v-img
          src="@/assets/logo-newsletter.png"
          aspect-ratio="1"
          class="newsletter-logo"
        >
        </v-img>
        <v-col class="ml-3">
          <h4 class="font-weight-bold">FOSCHIA</h4>
          <p>¿Quieres recibir notificaciones sobre ofertas y promociones?</p>
        </v-col>
      </v-row>

      <div class="row-alert">
        <span @click="closeAlert" primary class="blue--text" style="cursor:pointer;"> No, gracias </span>
        <v-btn @click="closeAlert" color="primary ml-5">SI</v-btn>
      </div>
    </v-container>
  </v-main>
</template>

<script>
export default {
  name: "NewsLetter",
  data() {
    return {
      showAlert: true,
    };
  },
  methods: {
    closeAlert() {
      this.showAlert = false;
    },
  },
};
</script>
