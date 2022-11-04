<template>
  <div id="app">
    <Fullscreen />
  </div>
</template>

<script>
import Fullscreen from '@/components/fullscreen.vue'
export default {
  name: 'App',
  components: {
    Fullscreen
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
  padding: 0;
  margin: 0;
}
</style>
