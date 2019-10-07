<template>
  <div>
    <div class="product">
      <h3 class="product__title">{{ product.title }} <strong>{{index}}</strong></h3>
      <p class="product__text">Product price: {{product.price}} <br> 
        Product quantity: {{ product.quantity }}
      </p>
      <button class="btn btn-info" @click="getDetailsClicked">Details</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }, 
    index: Number
  },
  methods: {
    getDetailsClicked() {
      this.$emit("getDetails", this.product.id)
    }
  }
}
</script>

<style>
  .product {
    border: 2px solid tomato;
    margin: 20px;
    text-align: center;
    width: 400px;
    padding: 15px;
  }
</style>