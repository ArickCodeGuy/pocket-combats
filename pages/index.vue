<template>
  <div class="container container-grid">
    <!-- <Logo /> -->
    <Header 
      :showAge="true"
      :age="age"
    />
    <PlayerStats />
    <LocationDescription />
  </div>
</template>

<script>
export default {
  name: 'InfoPage',

  data () {
    return {
      name: 'Anton',
      age: 18,
      plusAge: 10,
    }
  },

  computed: {

  },

  mounted () {},
}
</script>

<style>

</style>
