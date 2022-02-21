<script>
/* global mapboxgl */
export default {
  mounted: function () {
    mapboxgl.accessToken = process.env.VUE_APP_MAPBOX_ACCESS_TOKEN;
    const map = new mapboxgl.Map({
      container: "map", // container ID
      style: "mapbox://styles/mapbox/streets-v11", // style URL
      center: [-96.6989, 33.0198], // starting position [lng, lat]
      zoom: 11, // starting zoom
    });
    console.log(map);
  },
};
</script>

<template>
  <div class="map">
    <h2>Map!</h2>
    <div id="map"></div>
  </div>
</template>

<style>
#map {
  width: 100%;
  height: 700px;
}
</style>
