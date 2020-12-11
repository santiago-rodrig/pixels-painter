<template>
  <div>
    <Pixel v-for="n in 4" :key="n" :color="colors[n - 1]" />
  </div>
</template>

<script lang="ts">
import Pixel from "./Pixel.vue"

export default {
  name: "ColorPicker",
  components: {
    Pixel
  },
  data() {
    return {
      colors: ["white", "lightblue", "blue", "darkblue"]
    }
  }
}
</script>
