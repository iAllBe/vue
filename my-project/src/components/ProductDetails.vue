<template>
  <div>
    <div @click="showToggle">{{ product.name }}</div>
    <div v-if="show">
      <div>{{ product.formattedPrice + product.price }}</div>
      <div v-if="product.available">Available</div>
      <div v-else>Out of stock</div>
    </div>
    <br />
  </div>
</template>

<script>
export default {
  name: "ProductDetails",
  props: ["product"],
  data() {
    return {
      show: false,
    };
  },

  mounted() {},

  methods: {
    showToggle() {
      this.show = !this.show;
    },
  },
};
</script>

<style lang="scss" scoped>
</style>