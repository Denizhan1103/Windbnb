<template>
  <div class="search-bar" v-show="open">
    <div class="search-bar__content"></div>
    <div class="search-bar__shadow" @click="$emit('hide')"></div>
  </div>
</template>

<script>
export default {
  data: () => ({
    location: 'type'
  }),
  props: {
    open: Boolean
  },
}
</script>

<style lang="scss" scoped>
.search-bar {
  position: fixed;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;

  &__content {
    position: absolute;
    top: 0;
    left: 0;
    height: 400px;
    width: 100%;
    background: #fff
  }

  &__shadow {
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.4);
  }
}
</style>