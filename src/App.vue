<template>
  <div id="app" class="container">
    <product-list @getDetailsProduct="getDetailsProduct"></product-list>
    <product-details :product="selectedProduct"></product-details>
  </div>
</template>

<script>
import ProductList from './components/ProductList'
import ProductDetails from './components/ProductDetails'

export default {
  data() {
    return {
      selectedProduct: {}
    }
  },
  components: {
    ProductList,
    ProductDetails
  },
  methods: {
    getDetailsProduct(product) {
      this.selectedProduct = product
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
  display: flex;
}
</style>
