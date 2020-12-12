<template>
  <div class="canvas">
    <Pixel
      isInCanvas
      v-for="(color, index) in pixels"
      :color="color"
      :key="index"
      :index="index"
    />
  </div>
</template>

<script lang="ts">
import Pixel from "./Pixel.vue"

export default {
  name: "Canvas",
  components: {
    Pixel
  },
  props: {
    pixels: Array
  }
}
</script>

<style scoped>
.canvas {
  display: flex;
  flex-wrap: wrap;
  max-width: 900px;
}
</style>
