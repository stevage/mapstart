<template lang="pug">
#map.info-light3--bg(style="position:absolute;width:100%; height:100%")
</template>

<script>
import mapboxgl from "mapbox-gl";
import "mapbox-gl/dist/mapbox-gl.css";
import U from "map-gl-utils";
// import { EventBus } from "../EventBus";
export default {
  async mounted() {
    // replace this Mapbox access token with your own
    mapboxgl.accessToken =
      "pk.eyJ1Ijoic3RldmFnZSIsImEiOiJjazNmNGV5enAwMTF1M2tuejhtc2twcXo5In0.mLPrYIYJ2FiFZ3KMqVIj6w";
    const map = new mapboxgl.Map({
      container: "map",
      center: [144.96, -37.81],
      zoom: 14,
      style: "mapbox://styles/mapbox/light-v9",
    });
    console.log("yep");
    U.init(map, mapboxgl);
    window.map = map;
    window.app.Map = this;
  },
};
</script>

<style scoped></style>
