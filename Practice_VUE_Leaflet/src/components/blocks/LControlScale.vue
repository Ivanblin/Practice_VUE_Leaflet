<template>
  <l-map style="height: 90%" :zoom="zoom" :center="center">
    <l-tile-layer :url="url"></l-tile-layer>
    <l-control-scale
      :maxWidth='500'
      position="topright"
      :imperial="false"
      :metric="true"
    ></l-control-scale>
  </l-map>
</template>

<script>
import {LMap, LTileLayer, LControlScale} from 'vue2-leaflet';

export default {
  // name: 'LControlScale',
  components: {
    LMap,
    LTileLayer,
    LControlScale
  },
  data () {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      zoom: 8,
      center: [47.313220, -1.319482],
    };
  }
}
</script>
