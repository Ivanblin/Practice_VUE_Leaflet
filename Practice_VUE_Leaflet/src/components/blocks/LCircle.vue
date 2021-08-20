<template>
  <l-map style="height: 90%" className='className-l-map' :zoom="zoom" :center="center" :options="{zoomControl: false}">
    <l-tile-layer :url="url" ></l-tile-layer>
    <l-control-attribution position="topright" prefix="A custom prefix"></l-control-attribution>
    <l-control-zoom
      position="bottomleft"
      zoomInText='++'
      zoomOutText='--'
    ></l-control-zoom>
    <l-circle-marker
      :weight='1'
      :opacity='0.7'
      :fill='true'
      fillColor='#000'
      :lat-lng="circle.center"
      :radius="circle.radius"
      :color="circle.color"
      className='className-l-circle-marker'
    />
  </l-map>
</template>

<script>
import {LMap, LTileLayer, LCircleMarker, LControlAttribution, LControlZoom} from 'vue2-leaflet'

export default {
  components: {
    LMap,
    LTileLayer,
    LCircleMarker,
    LControlAttribution,
    LControlZoom
  },

  data () {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      zoom: 5,
      center: [47.313220, -1.319482],
      circle: {
        center: [47.413220, -1.0482],
        radius: 16,
        color: 'blue'
      }
    }
  }
}
</script>
