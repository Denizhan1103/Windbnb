<template>
  <div class="product-list">
    <div class="product-list__loc">
      <p class="product-list__loc-title">Stays in {{location}}</p>
      <p class="product-list__loc-number">{{stays}}+ stays</p>
    </div>
    <div class="product-list__item">
      <ProductItem v-for="(item,index) in list" :key="index" :detail="item"/>
    </div>
  </div>
</template>

<script>
import ProductItem from './ProductItem.vue'
export default {
  components: { ProductItem },
  data() {
    return {
      location: "Finland",
      stays: 12,
      locList: ["Helsinki","Turku","Oulu","Vaasa"],
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

<style lang="scss" scoped>
  .product-list {
    display: flex;
    width: 100%;
    justify-content: center;
    flex-wrap: wrap;

    &__loc {
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;

      &-title {
        font-weight: bold;
        font-size: 24px;
        color: #333333;
      }

      &-number {
        font-weight: 500;
        font-size: 14px;
        color: #4F4F4F;
      }
    }

    &__item {
      display: grid;
      width: 100%;
      place-items: center;
      gap: 10px 35px;
      //grid-template-areas: "list-item list-item list-item";
      grid-template-columns: repeat(3, minmax(300px, 1fr));
    }
  }

@media (max-width: 1220px) {
  .product-list__item {
    grid-template-columns: repeat(2, minmax(300px, 1fr));
  }
 }

@media (max-width: 820px) {
  .product-list__item {
    grid-template-columns: repeat(1, minmax(300px, 1fr));
  }
 }
</style>