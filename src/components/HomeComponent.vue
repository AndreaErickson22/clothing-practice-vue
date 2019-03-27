<template>
  <div class="hello">
    <h1>{{clothingName}} : {{total}}</h1>
    <div v-if="total >= 0" class="display"></div>
    <button @click="total--" type="button" class="btn btn-secondary btn-outline-dark">BUY</button>
    <img class="ShirtImage" v-bind:src="shirtImage" alt>
  </div>
</template>

<script>
export default {
  name: "HomeComponent",
  data() {
    return {
      clothingName: "Andrea's Shirts",
      shirtImage:
        "https://cdn.shopify.com/s/files/1/1306/0683/products/javascript_has_no_class_shirt_5588b00f-b860-4a34-bf56-9c995d54f9d6_1024x1024.jpeg?v=1473326265",
      total: 10
    };
  },
  methods: {
    buy() {
      this.total--;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ShirtImage {
  max-height: 100px;
  max-width: auto;
  border: 1px solid #000;
}
</style>
