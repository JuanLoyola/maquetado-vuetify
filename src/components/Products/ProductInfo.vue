<template>
  <v-card class="productCard">
    <v-container white class="product-container">
      <!-- top section -->
      <v-col>
        <v-row class="product-row">
          <!-- products thumbnail -->
          <div class="product-columns">
            <v-col v-for="(image, index) in images" :key="index">
              <v-img
                @click="changeMainImage(image)"
                :src="image"
                class="grey lighten-2 productImage"
              >
              </v-img>
            </v-col>
          </div>

          <!-- product main image -->
          <div class="img-box">
            <img
              class="product-img"
              :src="imgMain"
              alt="Product image"
              @click="showMainImage"
            />
          </div>

          <!-- product info section -->
          <v-col>
            <div class="text-left">
              <v-row>
                <v-breadcrumbs :items="itemsPath">
                  <template v-slot:divider>
                    <v-icon>mdi-chevron-right</v-icon>
                  </template>
                </v-breadcrumbs>
                <v-icon>mdi-heart</v-icon>
              </v-row>
            </div>

            <v-col class="text-left">
              <h3
                >Griferia De Cocina Ultragrif Jack Steel
                Monocomando</h3
              >
              <h4 class="text-left gray--text font-weight-regular">FOS-141574</h4>
            </v-col>

            <v-col>
              <small class="gray text-decoration-line-through">$ 16.008</small>
              <p class="price">
                $13,127 <small class="discount">18% OFF</small>
              </p>
            </v-col>

            <v-col>
              <p><v-icon>mdi-check</v-icon> Stock disponible</p>
              <p><v-icon>mdi-credit-card</v-icon> Planes ahora 3, 6, 12, 18</p>
              <p>
                <v-icon>mdi-information</v-icon> Disponible para
                <a
                  class="font-weight-bold text-decoration-none"
                  href="https://foschia.com.ar/acopio"
                  target="_blank"
                  rel="noopener noreferrer"
                  >Acopio en depósito</a
                >
              </p>
            </v-col>

            <div class="my-3 row">
              <div class="text-center mt-3">
                <div>
                  <v-btn @click="decreaseQuantity" outlined color="primary">
                    <v-icon> mdi-minus </v-icon>
                  </v-btn>
                  <input
                    class="counter text-center mx-3 font-weight-bold"
                    v-model="quantity"
                  />
                  <v-btn @click="increaseQuantity" outlined color="primary">
                    <v-icon> mdi-plus </v-icon>
                  </v-btn>
                </div>
                <small class="text-">71 disponibles</small>
              </div>
            </div>

						<div class="text-center">
							<v-btn color="primary">
                <v-icon> mdi-cart </v-icon> Comprar ahora
              </v-btn>
						</div>
          </v-col>
        </v-row>
      </v-col>

			<v-col class="details">
				<h3>
					Caracteristicas
				</h3>
				<div class="row">
          <v-col cols="3">
						<div class="blue--text font-weight-bold"><small>TIPO DE LIMPIEZA</small> </div>
						<div class="">No utilizar abrasivos</div>
          </v-col>
          <v-col cols="3">
            <div class="blue--text font-weight-bold"><small>GARANTÍA</small></div>
						<div class="">5 años</div>
          </v-col>
          <v-col cols="3">
            <div class="blue--text font-weight-bold"><small>MARCA</small></div>
						<div class="">Ultragrif</div>
          </v-col>
					<v-col cols="3">
            <div class="blue--text font-weight-bold"><small>LÍNEA</small></div>
						<div class="">Jack</div>
          </v-col>
        </div>

				<div class="row details">
          <v-col cols="3">
						<div class="blue--text font-weight-bold"><small>CON SALIDA</small> </div>
						<div class="">De mesada</div>
          </v-col>
          <v-col cols="3">
            <div class="blue--text font-weight-bold"><small>CUADRO DE DUCHA</small></div>
						<div class="">Monocomando</div>
          </v-col>
          <v-col cols="3">
            <div class="blue--text font-weight-bold"><small>TIPO DE INSTALACIÓN</small></div>
						<div class="">Movil</div>
          </v-col>
					<v-col cols="3">
            <div class="blue--text font-weight-bold"><small>IMPERMEABLE</small></div>
						<div class="">Argentina</div>
          </v-col>
        </div>
			</v-col>

			<v-col class="details information" cols="12">
				<h3>
					Más información
				</h3>
          <v-col cols="12">
						<div class="blue--text font-weight-bold"><small>DESCRIPCIÓN MARCA</small> </div>
						<div >ULTRAGRIF es una empresa Argentina con amplia experiencia y trayectoria. dedicada a la comercialización de griferías.</div>
          </v-col>
          <v-col cols="12">
            <div class="blue--text font-weight-bold"><small>TIPO DE PINTURA</small></div>
						<div class="">Apto para calefon y/o termotanque</div>
          </v-col>
			</v-col>
			
    </v-container>

    <!-- modal -->
    <v-container>
      <v-row>
        <v-col>
          <v-dialog
            v-model="showImageModal"
            style="display: flex; background-color: white; position: relative"
          >
            <v-carousel style="height: 100%; margin: auto">
              <v-row>
                <v-col style="display: flex">
                  <v-carousel-item
                    v-for="(image, index) in this.images"
                    :key="index"
                    :src="image"
                    style="width: 100%"
                  ></v-carousel-item>
                </v-col>
              </v-row>
            </v-carousel>
          </v-dialog>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: "ProductInfo",
  data() {
    return {
      itemsPath: [
        {
          text: "Griferías",
          disabled: false,
          href: "#",
        },
        {
          text: "Griferías Para Cocina",
          disabled: false,
          href: "#",
        },
        {
          text: "Monocomando",
          disabled: false,
          href: "#",
        },
      ],
      cards: null,
      items: null,
      quantity: 0,
      showImageModal: false,
      imgMain:
        "https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6Iqms6iJ-0a1aQfM2pz0gZIpYNCGMMqtNAKtGo8OC8fhn7N7lav_Id65_smsq.webp?x=1670858102",
      images: [
        "https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6Iqms6iJ-0a1aQfM2pz0gZIpYNCGMMqtNAKtGo8OC8fhn7N7lav_Id65_smsq.webp?x=1670858102",
        "https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6Iqms6iJ-0a1aWygguIlajR7Beheynis8iH3fi0O_zyYHd_gELeac0xz_smsq.webp?x=1670858103",
        "https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6Iqms6iJ-0a1aRkO5ROIPwTOuvtFzTcK-vsy-tGNHZ1vjxJl3O9nFMdM_smsq.webp?x=1670858103",
        "https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6Iqms6iJ-0a1aaV8lVpJ0gksKo9fEYzmCTeeVAlOjbXsiFMUSIB-9D_B_smsq.webp?x=1670858104",
      ],
    };
  },
  created() {},
  methods: {
    showMainImage() {
      this.showImageModal = true;
    },
    changeMainImage(image) {
      this.imgMain = image;
    },
    increaseQuantity() {
      this.quantity++;
    },
    decreaseQuantity() {
      if (this.quantity > 0) this.quantity--;
    },
  },
};
</script>
