<template>
  <div class="product-item">
    <div class="product-item__image"></div>
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
  prop: {
    detail: Object
  }
}
</script>

<style>

</style>