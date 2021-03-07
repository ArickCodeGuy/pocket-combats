<template>
  <div class="player-list menu-switcher-container">
    <div class="component-title menu-switcher">Игроки</div>
    <div class="menu-switchable player-list__items items">
      <div class="items__item item">
        <a href="#" class="item__msg"></a>
        <div class="item__player-icon"></div>
        <div class="item__player-name">Barett[lvl]</div>
        <a href="#" class="item__link"></a>
      </div>
    </div>
  </div>
</template>

<script>
  
</script>

<style lang="scss">
  @import "assets/css/index.scss";
  .player-list {
    .items {
      .item {
        display: flex;
        align-items: center;
        &__msg {
          width: 20px;
          height: 20px;
          display: inline-block;
          background-size: contain;
          background-repeat: no-repeat;
          background-position: center;
          background-color: lightgrey;
          margin-right: 10px;
        }
        &__player-icon {
          width: 20px;
          height: 20px;
          background-size: contain;
          background-repeat: no-repeat;
          background-position: center;
          background-color: lightgrey;
          margin-right: 10px;
        }
        &__player-name {
          color: var(--primary-color);
          margin-right: 10px;
          font-weight: bold;
        }
        &__link {
          width: 20px;
          height: 20px;
          display: inline-block;
          background-size: contain;
          background-repeat: no-repeat;
          background-position: center;
          background-color: lightgrey;
        }
      }
    }
  }
</style>