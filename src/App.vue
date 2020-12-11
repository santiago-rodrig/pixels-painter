<template>
  <div id="app">
    <ColorPicker />
    <Canvas />
  </div>
</template>

<script lang="ts">
import Vue from "vue"
import Canvas from "./components/Canvas.vue"
import ColorPicker from "./components/ColorPicker.vue"

export default Vue.extend({
  name: "App",
  components: {
    Canvas,
    ColorPicker
  }
})
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
