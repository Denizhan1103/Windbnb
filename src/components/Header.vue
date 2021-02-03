<template>
  <div class="header">
      <div class="header__logo">
            <img src="../assets/logo.png" alt="Windbnb Logo" class="header__logo-image">
            <p class="header__logo-title">Windbnb</p>
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
        max-width: 1600px;

        &__logo {
            display: flex;
            align-items: center;
            flex: 1;

            &-image {
                height: 20px;
                width: 20px;
                margin-right: 3px;
            }

            &-title {
                font-family: Poppins;
                font-style: normal;
                font-weight: bold;
                font-size: 16px;
                line-height: 21px;
                color: #EB5757;
            }
        }

        &__search {
            flex: 5;
            display: flex;
            justify-content: flex-end;
        }
    }
</style>