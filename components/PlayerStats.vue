<template>
  <div class="player-stats">
    <div class="player-stats__item item">
      <div 
        class="item__icon"
        style="background-image: url('');"
      />
      <div class="item__right">
        <div class="item__value">{{ PlayerObj.health }}</div>
        <div class="item__current-value">{{ PlayerObj.health }}</div>
      </div>
    </div>
    <div class="player-stats__item item">
      <div 
        class="item__icon"
        style="background-image: url('');"
      />
      <div class="item__right">
        <div class="item__value">{{ PlayerObj.mana }}</div>
        <div class="item__current-value">{{ PlayerObj.currentMana }}</div>
      </div>
    </div>
    <div class="player-stats__item item">
      <div 
        class="item__icon"
        style="background-image: url('');"
      />
      <div class="item__right">
        <div class="item__value">{{ PlayerObj.inventory }}</div>
        <div class="item__current-value">{{ PlayerObj.inventory }}</div>
      </div>
    </div>
  </div>
</template>

<script>
  import { Player } from '@/helpers/Player.js';
  export default {
    name: 'PlayerStatsCompo',

    props: {},

    data () {
      return {
        PlayerObj: {},
      }
    },

    mounted () {
      this.PlayerObj = Object.assign({}, Player);
    },
  }
</script>

<style lang="scss">
  @import 'assets/css/index.scss';
  .player-stats {
    display: flex;
    align-items: center;
    margin-left: -5px;
    margin-right: -5px;
    .item {
      margin-left: 5px;
      margin-right: 5px;
      box-shadow: 0 0 10px rgba(0, 0, 0, .2);
      display: flex;
      padding: 5px 10px;
      border-radius: 20px;
      width: 100%;
      flex-shrink: 1;
      align-items: center;
      overflow: hidden;
      &__icon {
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        background-color: grey;
        flex-shrink: 0;
        width: 30px;
        height: 30px;
        margin-right: 5px;
      }
      &__right {

      }
      &__value {
        font-size: 16px;
        line-height: 1em;
        color: $primary-color;
      }
      &__current-value {
        font-size: 12px;
        line-height: 1em;
      }
    }
  }
</style>