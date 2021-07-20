<template>
  <div id="app">
    <app-float-button @click="turnIt">Gira</app-float-button>
    <app-background :turned="turned" />
  </div>
</template>

<script>
import TheBackground from './components/TheBackground.vue'
import FloatButton from './components/FloatButton.vue'

export default {
  name: 'App',
  
  data () {
    return {
      turned: false
    }
  },

  methods: {
    turnIt () {
      this.turned = !this.turned
    }
  },

  components: {
    appBackground: TheBackground,
    appFloatButton: FloatButton
  }
}
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;

  box-sizing: inherit;
}

html {
  font-size: 62.5%;
}

body {
  box-sizing: content-box;
  background-color: #333;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100vh;
}
</style>
