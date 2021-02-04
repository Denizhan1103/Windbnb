<template>
    <div class="search-bar">
      <div class="search-bar__searching">
        <div class="search-bar__searching-loc">
          <div class="search-bar__searching-loc-title">Location</div>
          <div class="search-bar__searching-loc-add">Helsinki, Finland</div>
        </div>
        <div class="search-bar__searching-quest">
          <div class="search-bar__searching-quest-title">Guest</div>
          <div class="search-bar__searching-quest-add">Add guests</div>
        </div>
        <div class="search-bar__searching-button">Search</div>
      </div>
      <div class="search-bar__list">
          <div class="search-bar__list-location">
              <div class="search-bar__list-location-item">Helsinki, Finland</div>
              <div class="search-bar__list-location-item">Turku, Finland</div>
              <div class="search-bar__list-location-item">Oulu, Finland</div>
              <div class="search-bar__list-location-item">Vaasa, Finland</div>
          </div>
          <div class="search-bar__list-quest">
              <div class="adults">
                  <div class="adults__title">Adults</div>
                  <div class="adults__subtitle">Ages 13 or above</div>
                  <div class="adults__number">
                      <div class="adults__number-minus">-</div>
                      <div class="adults__number-data">0</div>
                      <div class="adults__number-plus"></div>
                  </div>
              </div>
              <div class="childrens">
                  <div class="childrens__title">Children</div>
                  <div class="childrens__subtitle">Ages 2-12</div>
                  <div class="childrens__number">
                      <div class="childrens__number-minus">-</div>
                      <div class="childrens__number-data">0</div>
                      <div class="childrens__number-plus"></div>
                  </div>
              </div>
          </div>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.search-bar {
    width: 100%;
    display: flex;
    flex-direction: column;

    &__searching {
      box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
      border-radius: 16px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      height: 40px;

      &-loc {
        flex: 1;
        filter: drop-shadow(0px 1px 6px rgba(0, 0, 0, 0.1));
        border-radius: 16px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 0 10px;
        margin-right: 10px;
        height: 100%;

        &-title {
          font-weight: 800;
          font-size: 10px;
          color: #333333;
          margin-bottom: 3px;
        }

        &-add {
          font-size: 14px;
          color: #BDBDBD;
        }

        &:hover {
            border: 1px solid #333333;
        }
      }

      &-quest {
        display: flex;
        flex-direction: column;
        height: 100%;
        justify-content: center;
        flex: 1;
        margin-right: 10px;
        padding: 0 10px;
        border-radius: 16px;

        &:hover {
            border: 1px solid #333333;
        }

        &-title {
          font-weight: 800;
          margin-bottom: 3px;
          font-size: 10px;
          color: #333333;
        }

        &-add {
          font-size: 14px;
          color: #BDBDBD;
        }
      }

      &-button {
        background: #EB5757;
        box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
        border-radius: 16px;
        height: 100%;
        max-width: 120px;
        color: #F2F2F2;
        font-weight: bold;
        font-size: 14px;
        flex: 1;
        display: grid;
        place-items: center;
      }
    }

    &__list {
        display: flex;
        width: 100%;

        &-location {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 20px 10px;

            &-item {
                font-size: 14px;
                color: #4F4F4F;
                flex: 1;
                margin-bottom: 30px;
            }
        }

        &-quest {
            flex: 1;
        }

    }
  }
</style>