<template>
  <div class="transitions">
    <div class="component-title">Переходы</div>
    <div 
      class="transitions__items items"
    >
      <!-- item.time -->
      <a href="#" class="items__item item">
        <div class="item__name"> Location 1 </div>
        <div class="item__time"> 5 сек </div>
      </a>
      <a href="#" class="items__item item">
        <div class="item__name"> Location 2 </div>
        <div class="item__time"> 5 сек </div>
      </a>
      <a href="#" class="items__item item">
        <div class="item__name"> Location 3 </div>
        <div class="item__time"> 5 сек </div>
      </a>
    </div>
  </div>
</template>

<script>
  // import { Locations } from '@/helpers/Locations.js';
  export default {
    name: 'TransitionsCompo',

    data () {
      return {
        // LocationsObj: {},
      }
    },

    created () {
      // this.LocationsObj = Object.assign({}, Locations);
    },
  }
</script>

<style lang="scss">
  @import 'assets/css/index.scss';
  .transitions {
    .items {
      display: grid;
      margin-left: -15px;
      margin-right: -15px;
      &__item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 15px;
        transition: .3s;
        font-size: 1.2em;
        color: var(--primary-color);
        cursor: pointer;
        &:hover {
          background-color: rgba(0, 0, 0, .1);
          text-decoration: none;
        }
        &__name {

        }
        &__time {
          font-weight: 600;
        }
      }
    }
  }
</style>