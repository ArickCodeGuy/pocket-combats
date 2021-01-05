<template>
  <div class="location-description">
    <div class="location-description__title"> {{ Location.title }} </div>
    <div class="location-description__description"> {{ Location.description }} </div>
  </div>
</template>

<script>
  export default {
    name: 'LocationDescriptionCompo',

    data () {
      return {
        Location: {
          title: 'Location name',
          description: 'Lorem ipsum ...',
        },
      }
    },
  }
</script>

<style lang="scss">
  @import 'assets/css/index.scss';
  .location-description {
    border-radius: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, .2);
    padding: 10px 20px;
    &__title {
      font-size: 1.2rem;
      margin-bottom: .2em;
      font-weight: 600;
      color: $primary-color;
    }
    &__description {
      font-size: .9rem;
    }
  }
</style>