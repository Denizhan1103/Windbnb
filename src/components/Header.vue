<template>
  <div class="header">
      <div class="header__logo">
            <img src="../assets/logo.png" alt="Windbnb Logo" class="header__logo-image">
      </div>
      <div class="header__search">
          <SearchBar/>
      </div>
  </div>
</template>

<script>
import SearchBar from './SearchBar.vue'

export default {
    components: {
        SearchBar
    }
}
</script>

<style lang="scss" scoped>
    .header {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 100px;
        width: 100%;

        &__logo {
            display: flex;
            align-items: center;
            flex: 1;

            &-image {
                height: 28px;
                width: 100px;
                margin-right: 3px;
            }
        }

        &__search {
            flex: 5;
            display: flex;
            justify-content: flex-end;
        }
    }
</style>