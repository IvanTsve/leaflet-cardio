<template>
  <div id="app">
    <LeafMap> </LeafMap>
  </div>
</template>

<script>
import LeafMap from './components/LeafMap.vue'

export default {
  name: 'App',
  components: {
    LeafMap
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
