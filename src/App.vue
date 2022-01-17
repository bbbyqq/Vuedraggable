<template>
  <div id="app">
    <Vuedraggable />
  </div>
</template>

<script>
import Vuedraggable from './components/Vuedraggable.vue'

export default {
  name: 'app',
  components: {
    Vuedraggable
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
  margin-top: 60px;
}
</style>
