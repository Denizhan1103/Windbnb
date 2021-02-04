<template>
  <Search :open="show" @hide="hideSearch" />
  <div class="search" @click="showSearch">
    <div class="search__loc">Helsinki, Finland</div>
    <div class="search__bar">Add quest</div>
  </div>
</template>

<script>
import Search from './Search.vue'

export default {
  components: {
    Search 
  },
  data() {
    return {
      show: false
    }
  },
  props: {
  },
  methods: {
    showSearch() {
      this.show = true
    },

    hideSearch() {
      this.show = false
    }
  }
}
</script>

<style lang="scss" scoped>
  .search-bar--open {
    display: flex;
  }
  .search {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 16px;
    width: 300px;
    height: 55px;
    box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
    border-radius: 16px;
    cursor: pointer;

    &__loc {
      font-size: 14px;
      color: #333333;
    }

    &__bar {
      font-size: 14px;
      color: #BDBDBD;
    }
  }
</style>