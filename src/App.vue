<template>
  <div id="app">
    <Links />
  </div>
</template>

<script>
import Links from './components/Links.vue'

export default {
  name: 'App',
  components: {
    Links
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 20px;
}
</style>
