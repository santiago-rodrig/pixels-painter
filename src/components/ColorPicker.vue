<template>
  <div>
    <Pixel
      isInColorPicker
      v-for="n in 4"
      :key="n"
      :color="colors[n - 1]"
      :current="color == colors[n - 1] ? true : false"
    />
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
  },
  props: {
    color: String
  }
}
</script>
