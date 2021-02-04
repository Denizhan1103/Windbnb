<template>
  <div id="app">
    <div class="container">
      <Search/>
      <Header/>
      <ProductList/>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import ProductList from "./components/ProductList.vue"
import Search from "./components/Search.vue"

export default {
  components: {
      Header,
      Footer,
      ProductList,
      Search
  }
}
</script>

<style lang="scss" scoped>
  .container {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 1400px !important;
  } 

  #app {
    display: flex;
    justify-content: center;
  }
</style>
