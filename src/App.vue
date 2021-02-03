<template>
  <Header/>
  <ProductList/>
  <Footer/>
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
