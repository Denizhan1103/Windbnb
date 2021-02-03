<template>
  <div class="container">
    <Header/>
    <ProductList/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import ProductList from "./components/ProductList.vue"

export default {
  components: {
      Header,
      Footer,
      ProductList
  }
}
</script>

<style lang="scss" scoped>
  .container {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  } 
</style>
