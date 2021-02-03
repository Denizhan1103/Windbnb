<template>
  <div class="product-item">
    <div class="product-item__image" :style="'background: url('+detail.image+')'"></div>
    <div class="product__item-data">
      <div class="data__up">
        <div class="data__up-type">{{detail.type}}</div>
        <div class="data__up-construct">{{detail.construct}}</div>
        <div class="data__up-star">{{detail.star}}</div>
      </div>
      <p class="data__down">{{detail.name}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    detail: Object
  }
}
</script>

<style lang="scss" scoped>
  .product-item {
    width: 270px;
    margin-right: 30px;
    margin-bottom: 50px;
    display: flex;
    flex-direction: column;

    &__image {
      height: 395px;
      width: 100%;
    }

    &__data {
      display: flex;
      flex-direction: column;

      .data__up {
        display: flex;
        justify-content: space-between;
      }
    }
  }
</style>