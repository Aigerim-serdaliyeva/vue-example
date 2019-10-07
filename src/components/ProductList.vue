<template>
  <div>
    <product-item v-for="(product, i) in products" 
      :key="product.id"
      :product="product"
      :index="(i+1)"
      @getDetails="getDetailsAll"
    ></product-item>
  </div>
</template>

<script>
import ProductItem from './ProductItem'
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          title: "Toyota",
          price: 6000000,
          quantity: 5
        },
        {
          id: 2,
          title: 'KIA',
          price: 4000000,
          quantity: 8
        },
        {
          id: 3,
          title: "Ford",
          price: 8000000,
          quantity: 3
        }
      ]
    }
  },
  methods: {
    getDetailsAll(id) {
      debugger;
      let toProduct = this.products.find((product) => product.id === id);
      if (toProduct) {
        this.$emit('getDetailsProduct', toProduct)
      }
    }
  },
  components: {
    ProductItem
  }
}
</script>

<style scoped>

</style>