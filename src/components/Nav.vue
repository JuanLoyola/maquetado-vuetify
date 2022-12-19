<template>
  <v-app-bar app color="primary" dark>
    <img class="logo" src="@/assets/logo.jpg" alt="Logo Foschia" />

    <v-row>
      <v-icon dark left> mdi-arrow-down </v-icon>
      <small>Menú</small>
    </v-row>

    <v-spacer></v-spacer>

    <v-text-field
      class="input-search"
      style="height: 100%, width: 40px !important"
      append-icon="mdi-magnify"
      placeholder="Buscar productos, marcas y más"
      v-model="text"
    ></v-text-field>

    <v-spacer></v-spacer>

    <div class="column" style="margin-right: 2rem">
      <small>Atención al cliente</small>
      <small><v-icon dark left> mdi-whatsapp </v-icon> 11 6011 6413</small>
    </div>

    <v-row>
      <v-icon dark left> mdi-account </v-icon>
      <small>Ingresar</small>
    </v-row>

    <v-icon dark left> mdi-cart </v-icon>
  </v-app-bar>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      text: "",
    };
  },
};
</script>
