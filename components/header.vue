<template>
  <div class="header">
    <div class="header__burger">
      <span />
      <span />
      <span />
    </div>
    <div class="header__title">
      {{ title }}
    </div>
    <div class="header__nav" style="display: none;">
      <ul>
        <li><a href="#">item 1</a></li>
        <li><a href="#">item 2</a></li>
        <li><a href="#">item 3</a></li>
        <li><a href="#">item 4</a></li>
      </ul>
    </div>
    <!-- <ul>
      <li
        v-for="(link, index) in links"
        :key="index"
      >
        {{ link }}
      </li>
      <li v-if="showAge">
        Age {{ age }}
      </li>
    </ul> -->
  </div>
</template>

<script>
export default {
  name: 'HeaderCompo',

  props: {
    age: {
      type: Number, // String, Array, Object, Boolean
      default: 0,
    },
    showAge: {
      type: Boolean,
      default: false,
    },
    title: {
      type: String,
      default: 'Pocket combats',
    },
  },

  data () {
    return {
      links: [
        'link 1',
        'link 10',
        'link 100',
      ],
    }
  },
}
</script>
<style lang="scss">
  @import 'assets/css/index.scss';
  .header {
    display: flex;
    align-items: center;
    &__burger {
      position: relative;
      width: 26px;
      height: 16px;
      margin-right: 30px;
      cursor: pointer;
      span {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: black;
        transition: .3s;
        &:nth-child(1) {

        }
        &:nth-child(2){
          top: 50%;
          transform: translateY(-50%);
        }
        &:nth-child(3){
          top: 100%;
          transform: translateY(-100%);
        }
      }
    }
    &__title {
      font-size: 30px;
      color: $primary-color;
    }
  }
</style>