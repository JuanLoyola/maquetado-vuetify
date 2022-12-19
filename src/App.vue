<template>
  <v-app>
    <NavBar />
    <NewsLetter />
    <v-main>
      <v-container>
        <ProductInfo />
        <h2 class="my-7 font-weight-medium">Tambien te puede interesar</h2>
        <v-row class="products-list">
          <!-- Esto en realidad seria un v-for corriendo la lista de productos filtrados por el endpoint, pero por fines UI del test lo hago asi -->
          <!-- todo el contenido de las props vendria de back, por lo cual el componente seria mas limpio y sencillo de leer -->
          <ProductCard :imageLink="image1" :discount="'79.891'" :price="'47.935'" :percent="'18% OFF'" :cuotas="'hasta 18 cuotas'" :productInfo="'Griferia De Cocina Monocomando Vasser Lyra'"/>
          <ProductCard :imageLink="image2" :discount="'79.891'" :price="'47.935'" :percent="'18% OFF'" :cuotas="'hasta 18 cuotas'" :productInfo="'Griferia De Cocina Monocomando Vasser Lyra'"/>
          <ProductCard :imageLink="image3" :discount="'79.891'" :price="'47.935'" :percent="'18% OFF'" :cuotas="'hasta 18 cuotas'" :productInfo="'Griferia De Cocina Monocomando Vasser Lyra'"/>
          <ProductCard :imageLink="image4" :discount="'79.891'" :price="'47.935'" :percent="'18% OFF'" :cuotas="'hasta 18 cuotas'" :productInfo="'Griferia De Cocina Monocomando Vasser Lyra'"/>
        </v-row>
      </v-container>
    </v-main>
    <ChatButton />
    <TheFooter />
  </v-app>
</template>

<script>
import NavBar from '@/components/Nav.vue';
import ProductInfo from '@/components/Products/ProductInfo.vue';
import ProductCard from '@/components/Products/ProductCard.vue';
import ChatButton from '@/components/Utils/ChatButton.vue';
import NewsLetter from '@/components/Utils/NewsLetter.vue';
import TheFooter from '@/components/Footer.vue';

export default {
  name: "App",
  data() {
    return {
      // paso las imagenes aca para mantener limpio el template nada mas.
      image1: 'https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6IqSWOx8MXUAqJ3pnP1UU-sup9xfhGfOggrTdjTNA9hlM7zDYG4672Og_smsq.webp?x=1627203206',
      image2: 'https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6IplDG3XxdZhjj4vEUIu_YTjQClhOjgY6LrFxSZkW2O5tFDye_jzCnn__smsq.webp?x=1661796019',
      image3: 'https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6IpXbLka6qeAqf1bHf5NrZLOoz2sWMwi57-JFqpifyms0qnQwUH5K8nU_smsq.webp?x=1627203409',
      image4: 'https://foschia.com.ar/static/uploads/products/webp/imIqk4qF2eygJQUGAHuPjbIR38nb78HKnmToj-bn6IrN20O_LtMjGTCMU5TtOjf-O8AZFTXydFxOkBOrIBijElkeSY2Y-H3h_smsq.webp?x=1627201698'
    }
  },
  components: {
    NavBar,
    ProductInfo,
    ProductCard,
    ChatButton,
    NewsLetter,
    TheFooter
  },
  methods: {},
};
</script>
