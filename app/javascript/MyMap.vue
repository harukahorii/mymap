<template>
  <div>
    <h1>Map</h1>
    <map-loader
      :map-config="mapConfig"
      apiKey="Rails.application.credentials.google_maps_api_key"

      <template v-for="marker in markers">
        <child-marker :position="marker" />
      </template>
    </map-loader>
  </div>
</template>

<script>
import MapLoader from "./MapLoader.vue"
import ChildMarker from './ChildMarker'

export default {
  props: {
    markers: Array
  },
  data() {
    return {
      mapConfig:{
      zoom: 12,
      center: this.markers[0]
    }
    }
  },
  components: {
    MapLoader,
    ChildMarker
  }
}
</script>
