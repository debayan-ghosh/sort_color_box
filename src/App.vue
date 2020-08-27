<template>
  <div id="app">
    <NumberBox/>
  </div>
</template>

<script>
import NumberBox from './components/NumberBox.vue'

export default {
  name: 'App',
  components: {
    NumberBox
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
