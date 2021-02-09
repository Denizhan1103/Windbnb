<template>
  <div class="search-bar" v-show="open">
    <div class="search-bar__content">
        <div class="search-bar__searching">
          <div class="search-bar__searching-loc" @click="type = 'location'">
            <div class="search-bar__searching-loc-title">Location</div>
            <div class="search-bar__searching-loc-add">Helsinki, Finland</div>
          </div>
          <div class="search-bar__searching-quest" @click="type = 'quest'">
            <div class="search-bar__searching-quest-title">Guest</div>
            <div class="search-bar__searching-quest-add">Add guests</div>
          </div>
          <div class="search-bar__searching-button">
            <i class="search-bar__searching-button--icon fas fa-search"></i>
            Search
          </div>
        </div>
        <div class="search-bar__list">
            <div class="search-bar__list-location" :class="{'search-bar__list--visible':type == 'location'}">
                <div class="search-bar__list-location-item">Helsinki, Finland</div>
                <div class="search-bar__list-location-item">Turku, Finland</div>
                <div class="search-bar__list-location-item">Oulu, Finland</div>
                <div class="search-bar__list-location-item">Vaasa, Finland</div>
            </div>
            <div class="search-bar__list-quest" :class="{'search-bar__list--visible':type == 'quest'}">
                <div class="adults">
                    <div class="adults__title">Adults</div>
                    <div class="adults__subtitle">Ages 13 or above</div>
                    <div class="adults__number">
                        <div class="adults__number-minus">-</div>
                        <div class="adults__number-data">0</div>
                        <div class="adults__number-plus">+</div>
                    </div>
                </div>
                <div class="adults">
                    <div class="adults__title">Children</div>
                    <div class="adults__subtitle">Ages 2-12</div>
                    <div class="adults__number">
                        <div class="adults__number-minus">-</div>
                        <div class="adults__number-data">0</div>
                        <div class="adults__number-plus">+</div>
                    </div>
                </div>
            </div>
            <div class="search-bar__list-empty"></div>
        </div>
        <div class="search-bar__mobile">
          <div class="search-bar__searching-button search-bar__mobile-button">
            <i class="search-bar__searching-button--icon fas fa-search"></i>
            Search
          </div>
        </div>
    </div>
    <div class="search-bar__shadow" @click="$emit('hide')"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {type : 'location'} 
  },
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

    &__searching {
      box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
      border-radius: 16px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      height: 40px;
      padding: 20px;
      z-index: 100;

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
        border: 1px solid transparent;

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
        border: 1px solid transparent;

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
        display: flex;
        justify-content: center;
        align-items: center;

        &--icon {
          margin-right: 8px;
          font-size: 14px;
        }
      }
    }
    &__list {
        display: flex;
        width: 100%;
        padding: 0 20px;
        z-index: 100;

        &-location {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 20px 10px;
            visibility: hidden;

            &-item {
                font-size: 14px;
                color: #4F4F4F;
                flex: 1;
                margin-bottom: 30px;
            }
        }

        &--visible {
          visibility: visible !important;
        }

        &-quest {
            flex: 1;
            visibility: hidden;
        }

        &-empty {
          width: 130px;
        }

    }
}

.adults{
  padding: 20px 0 0 0;

  &__title {
    font-weight: bold;
    font-size: 14px;
    color: #333333;
  }

  &__subtitle {
    font-size: 14px;
    color: #333333;
    margin-bottom: 10px;
  }

  &__number {
    display: flex;

    &-minus,
    &-plus {
      border: 1px solid #828282;
      box-sizing: border-box;
      border-radius: 4px;
      height: 24px;
      width: 24px;
      color: #828282;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
    }

    &-data {
      margin: 0 5px;
    }
  }
}

.search-bar__mobile {
  display: none !important;
}


@media (max-width: 576px) {
  .search-bar {

    &__content {
      height: 470px !important;
    }

    &__searching {
        flex-direction: column !important;
        height: auto;

        &-loc {
          margin-bottom: 20px;
        }

        &-button {
            display: none;
        }
    }

    &__list {
      min-height: 245px;

      &--visible {
        display: flex !important;
      }

      &-quest,
      &-location {
        display: none;
      }

      &-quest {
        flex-direction: column;
      }
    }

    &__mobile {
      display: flex !important;
      align-items: center;
      justify-content: center;
      height: 40px;

      &-button {
        display: flex !important;
        justify-content: center;
      }
    }
  }
}
</style>