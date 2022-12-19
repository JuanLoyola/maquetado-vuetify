<template>
  <v-container>
    <v-row justify="space-around">
      <v-card  class="product-card">
        <v-img height="200px" :src="imageLink">
          <v-app-bar flat color="rgba(0, 0, 0, 0)">
            <v-spacer></v-spacer>

            <v-btn color="gray" icon>
              <v-icon>mdi-heart</v-icon>
            </v-btn>
          </v-app-bar>
        </v-img>

        <v-card-text>
          <div
            class="font-weight-medium mb-2 text-decoration-line-through gray--text"
          >
            ${{ discount }}
          </div>

          <div>
            <span style="font-size: 1rem" class="font-weight-bold black--text">
              ${{ price }}
            </span>
            <span>
              <small class="gray--text font-weight-semibold">{{
                percent
              }}</small></span
            >
          </div>

          <div>
            <small class="purple--text">
              {{ cuotas }}
            </small>
          </div>

          <div>
            <p>
              {{ productInfo }}
            </p>
          </div>

          <div class="text-center">
            <v-btn small>
              <v-icon small>mdi-cart</v-icon>
              Comprar
            </v-btn>
          </div>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    imageLink: {
      type: String,
    },
    discount: {
      type: String,
    },
    price: {
      type: String,
    },
    percent: {
      type: String,
    },
    cuotas: {
      type: String,
    },
    productInfo: {
      type: String,
    }
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
