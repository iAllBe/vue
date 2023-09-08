<template>
  <div>
    <ProductDetails
      :product="product"
      v-for="product in products"
      :key="product.id"
    >
    </ProductDetails>
  </div>
</template>

<script>
import ProductDetails from "./ProductDetails.vue";

export default {
  name: "ProductList",
  components: {
    ProductDetails,
  },

  data() {
    return {
      products: [
        {
          name: "Название1",
          price: 33,
          available: true,
          formattedPrice: "$",
        },
        {
          name: "Название2",
          price: 44,
          available: false,
          formattedPrice: "руб.",
        },
        {
          name: "Название3",
          price: 55,
          available: false,
          formattedPrice: "€",
        },
        {
          name: "Название4",
          price: 66,
          available: true,
          formattedPrice: "¥",
        },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
</style>