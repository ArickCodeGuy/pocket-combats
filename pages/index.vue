<template>
  <div class="container">
    <Logo />
    <Header :showAge="true" :age="age" />

    Name: {{ name }}
    <br>
    Age: {{ age }}
    <br>
    After {{ plusAge }} years i will be: {{ futureAge }}
    <br>
    <br>
    <b-button
      :title="`My age is: ${age}`"
      variant="outline-primary"
      @click="buttonHandler"
    >Makes me older</b-button>

    <br>

    <b-button
      :title="`My age is: ${age}`"
      variant="outline-primary"
      v-on:click="makesMeYounger"
    >Makes me younger</b-button>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
  </div>
</template>

<script>
export default {
  name: 'InfoPage',

  data () {
    return {
      name: 'Anton',
      age: 18,
      plusAge: 10
    }
  },

  computed: {
    futureAge () {
      return this.age + this.plusAge
    }
  },

  mounted () {},

  methods: {
    buttonHandler () {
      this.age = this.age + 1
    },

    makesMeYounger () {
      this.age -= 5
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
