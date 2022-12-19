<template>
  <v-footer class="footer" dark padless>
    <v-card flat tile class="black lighten-1 white--text text-center">
      <v-card-text class="gray--text text-center">
        <v-row class="row-footer">
          <v-row class="text-left py-5" style="align-items: center; justify-content: center; display: flex">
            <v-spacer></v-spacer>
            <div>
              <img
                src="https://foschia.com.ar/static/img/logo-foschia-footer.webp?x=1607945337"
                alt="logo footer"
              />
            </div>
            <v-col style="height:190px; line-height: 20px">
              <a
                href="mailto:info@foschia.com.ar"
                class="white--text font-weight-light"
                ><v-icon size="small" left>mdi-email</v-icon
                >info@foschia.com.ar</a
              >
              <br />
              <a href="tel:116012-3758" class="white--text font-weight-light">
                <v-icon size="small" left>mdi-phone</v-icon>(011) 6012-3758</a>
              <p>
                <v-icon size="small" left>mdi-map-marker</v-icon>
                Colectora Este 30451, El Talar, Buenos aires
              </p>
              <v-icon left>mdi-instagram</v-icon>
              <v-icon left>mdi-facebook</v-icon>
            </v-col>

            <v-col style="height:190px; line-height: 10px">
              <p class="font-weight-bold">INSTITUCIONAL</p>
              <v-spacer></v-spacer>
              <p class="font-weight-light">Sobre Foschia</p>
              <p class="font-weight-light">Sucursales</p>
              <p class="font-weight-light">Información Legal</p>
            </v-col>

            <v-col style="height:190px; line-height: 10px">
              <p class="font-weight-bold">SERVICIO AL CLIENTE</p>
              <p class="font-weight-light">Políticas de Envío</p>
              <p class="font-weight-light">Políticas de Cambio</p>
              <p class="font-weight-light">Cláusulas de Venta</p>
              <p class="font-weight-light">Métodos de Pago</p>
            </v-col>

            <v-col style="height:190px; line-height: 10px">
              <p class="font-weight-bold">TUS FAVORITAS</p>
              <v-spacer></v-spacer>
              <p class="font-weight-light">Mejores Ofertas</p>
              <p class="font-weight-light">Hot Sale</p>
              <p class="font-weight-light">Cyber Monday</p>
            </v-col>

            <v-spacer></v-spacer>
          </v-row>
        </v-row>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="gray--text text-center">
        <v-row>
          <v-spacer></v-spacer>
          <v-col class="text-left" cols="4">
            <small>
              Copyright © 2020 Construdiseño S.A. El uso de este sitio web
              implica la aceptación de los Términos y Condiciones y de las
              Políticas de Privacidad de Construdiseño S.A. Las fotos son a modo
              ilustrativo. La venta de cualquiera de los productos publicados
              está sujeta a la verificación de stock. Los precios online para
              los productos presentados/publicados en www.foschia.com.ar son
              válidos exclusivamente para la compra vía internet en las páginas
              antes mencionadas. foschia.com.ar
            </small>
          </v-col>
          <v-col class="text-left" cols="4">
            <div class="mb-3"><h3 class="text-uppercase">Sellos</h3></div>
            <img
              style="width: 36.531px"
              src="https://foschia.com.ar/static/img/data-fiscal.webp?x=1607945237"
              alt="footer img"
            />
            <img
              class="mx-3"
              src="https://foschia.com.ar/static/img/datos-personales.webp?x=1607945238"
              alt="footer img"
            />
            <img
              src="https://foschia.com.ar/static/img/sello-cace.webp?x=1607945342"
              alt="footer img"
            />
          </v-col>
          <v-spacer></v-spacer>
        </v-row>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="gray--text">
        Diseñado y desarrollado por
        <a
          href="https://drubbit.com/"
          target="_blank"
          class="purple--text text-decoration-none"
          >drubbit.com</a
        >
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  // Por que The Footer y no solo Footer?
  // Esto sucede porque no gasté tiempo configurando el ESLINT, y pide que todos los componentes sean multiples palabras.. ups! 😇
  // ESLINT error: Component name 'Footer' should alyas be multi-word
  name: "TheFooter",
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>
