<template>
  <div class="product-list">
    <ProductItem v-for="(item,index) in list" :key="index" :detail="item"/>
  </div>
</template>

<script>
import ProductItem from './ProductItem.vue'
export default {
  components: { ProductItem },
  data() {
    return {
      list: [ 
        {
          name: 'Stylist apartment in center of the city',
          construct: 'Entire apartments. 2 beds',
          star: '4.40',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel1.jpg')
        },
        {
          name: 'Cozy, peaceful and private room with...',
          construct: 'Private room',
          star: '4.25',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel2.jpg')
        },
        {
          name: 'Modern house in a remote area',
          construct: 'Entire house',
          star: '4.96',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel3.jpg')
        },
        {
          name: 'Stylist room in design district',
          construct: 'Entire apartments. 2 beds',
          star: '4.85',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel4.jpg')
        },
        {
          name: 'Modern apartment close to nature',
          construct: 'Private room',
          star: '4.54',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel5.jpg')
        },
        {
          name: 'House in a remote area',
          construct: 'Entire house',
          star: '4.64',
          properties: ['super', 'normal'],
          type: 'SUPER HOST',
          image: require('../assets/hotel6.jpg')
        }
      ]
    }
  }
}
</script>

<style>

</style>