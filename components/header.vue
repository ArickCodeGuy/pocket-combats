<template>
  <div class="header">
    <ul>
      <li
        v-for="(link, index) in links"
        :key="index"
      >
        {{ link }}
      </li>
      <li v-if="showAge">
        Age {{ age }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HeaderCompo',

  props: {
    age: {
      type: Number, // String, Array, Object, Boolean
      default: 0
    },
    showAge: {
      type: Boolean,
      default: false
    }
  },

  data () {
    return {
      links: [
        'link 1',
        'link 10',
        'link 100'
      ]
    }
  }
}
</script>
