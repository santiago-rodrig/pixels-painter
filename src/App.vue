<template>
  <div id="app">
    <ColorPicker :color="color" />
    <Canvas :pixels="pixels" />
  </div>
</template>

<script lang="ts">
import Vue from "vue"
import Canvas from "./components/Canvas.vue"
import ColorPicker from "./components/ColorPicker.vue"

const defaultColor = "white"

export default Vue.extend({
  name: "App",
  components: {
    Canvas,
    ColorPicker
  },
  data() {
    return {
      color: defaultColor,
      pixels: Array(30 * 30)
        .fill("")
        .map(() => defaultColor)
    }
  },
  mounted() {
    this.$root.$on("updatecolor", (color: string) => {
      this.color = color
    })

    this.$root.$on("clickedpixel", (index: number) => {
      this.pixels.splice(index, 1, this.color)
    })
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
  background-color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>
