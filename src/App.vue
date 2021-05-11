<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Day1 title="Welcome to Your Vue.js App"/>
</template>

<script>
import Day1 from './components/Day1.vue'

export default {
  name: 'App',
  components: {
    Day1
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
