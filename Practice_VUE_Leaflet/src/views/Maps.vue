<template>
  <div>
    <div class="map-block">
      <h1>LCircle & LControlAttribution & LControlZoom</h1>
      <l-circle></l-circle>
    </div>
    <div class="map-block">
      <h1>LControlLayers</h1>
      <l-control-scale></l-control-scale>
    </div>
    <br>
    <div class="map-block">
      <h1>LControlScale</h1>
      <l-control-layers></l-control-layers>
    </div>
    <br>
  </div>
</template>

<script>
import LCircle from '@/components/blocks/LCircle.vue'
import LControlLayers from '@/components/blocks/LControlLayers.vue'
import LControlScale from '@/components/blocks/LControlScale.vue'

export default {
  components: {
    LCircle,
    LControlLayers,
    LControlScale
  }
}
</script>

<style lang="scss" scoped>
  .map-block {
    height: 100vh;
  }
</style>
