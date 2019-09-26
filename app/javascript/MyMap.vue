<template>
  <div>
    <h1>Map</h1>
    <map-loader
      :map-config="mapConfig"
      apiKey=Rails.application.credentials.google_maps_api_key>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      message: "Hello Vue!"
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>