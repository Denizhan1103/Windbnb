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
    width: 400px;
    margin-right: 30px;
    cursor: pointer;
    margin-bottom: 50px;
    display: flex;
    flex-direction: column;

    &__image {
      height: 275px;
      width: 100%;
      background-size: cover !important;
      border-radius: 24px;
      margin-bottom: 10px;
    }

    &__data {
      display: flex;
      flex-direction: column;
    }
  }

  .data__up {
    display: flex;
    justify-content: space-between;

      &-type {
        font-weight: bold;
        font-size: 16px;
        color: #4F4F4F;
        padding: 2px 10px;
        border: 1px solid #4F4F4F;
        border-radius: 12px;
      }

      &-construct {
        font-weight: 500;
        font-size: 14px;
        color: #828282;
      }

      &-star {
        font-weight: 500;
        font-size: 14px;
      }
  }

  .data__down {
    font-weight: 600;
    font-size: 16px;
    color: #333333;
  }
</style>