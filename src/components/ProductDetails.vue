<template>
  <div>
    <div class="product">
      <h3 class="product__title">Detail name</h3>
      <strong>Car: {{product.title}}</strong> <br>
      <strong>Price: {{product.price}}</strong> <br>
      <strong>Quantity: {{product.quantity}}</strong>
    </div>
  </div>
</template>

<script>
export default {
   props: {
    product: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>