<template>
  <div class="canvas">
    <Pixel v-for="n in 30 * 30" :key="n" />
  </div>
</template>

<script lang="ts">
import Pixel from "./Pixel.vue"

export default {
  name: "Canvas",
  components: {
    Pixel
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
