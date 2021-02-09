<template>
  <div class="product-item">
    <div class="product-item__image" :style="'background: url('+detail.image+')'"></div>
    <div class="product__item-data">
      <div class="data__up">
        <div class="data__up-type">
          <div class="data__up-type-item">{{detail.type}}</div>
          <div class="data__up-construct">{{detail.construct}}</div>
        </div>
        <div class="data__up-item">
          <i class="data__up-item-icon fas fa-star"></i>
          <div class="data__up-star">{{detail.star}}</div>
        </div>
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
    width: 100%;
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
      background-position: center;
    }

    &__data {
      display: flex;
      flex-direction: column;
    }
  }

  .data__up {
    display: flex;
    justify-content: space-between;
    align-items: center;

    &-item {
      display: flex;
      align-items: center;

      &-icon {
        font-size: 14px;
        margin-right: 3px;
        margin-bottom: 2px;
        color: #EB5757;
      }
    }

    &-type {
        display: flex;
        flex-direction: row;
        align-items: center;

        &-item {
          font-weight: bold;
          font-size: 16px;
          color: #4F4F4F;
          padding: 2px 10px;
          border: 1px solid #4F4F4F;
          border-radius: 12px;
          margin-right: 10px;
      }

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