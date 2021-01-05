<template>
  <div class="transitions">
    <div class="transitions__title">Переходы</div>
    <div class="transitions__items items">
      <div class="items__item item">
        <div class="item__name"> {{ Location[1][1].name }} </div>
        <div class="item__time"> {{ Location[1][1].time }} сек </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { Locations } from '@/helpers/Locations.js';
  export default {
    name: 'TransitionsCompo',

    data () {
      return {
        LocationsObj: {},        
      }
    },

    mounted () {
      this.LocationsObj = Object.assign({}, Locations);
    },
  }
</script>

<style lang="scss">
  .transitions {
    &__title {
      margin-bottom: 0.5em;
    }
    .items {
      display: grid;
      &__item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 0;
        &:hover {
          background-color: rgba(0, 0, 0, .2);
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