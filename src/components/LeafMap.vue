<template>
  <div>
    <LMap
      ref="map"
      :min-zoom="data.minZoom"
      :zoom="data.zoom"
      :crs="data.crs"
       style="height: 600px; width: 600px;"
       :center="data.center"
    >
      <LImageOverlay 
      :url="data.url" 
      :bounds="data.bounds"
      ></LImageOverlay>
    </LMap>
  </div>
</template>

<script>
/* eslint-disable vue/no-unused-components */
// import Vue from 'vue';
import { CRS } from "leaflet";
import { LMap, LTileLayer, LMarker, LImageOverlay } from "vue2-leaflet";
import "leaflet/dist/leaflet.css";

export default {
  data() {
    return {
      data: {},
    };
  },

  mounted() {
    this.data = {
      minZoom:-1,
      crs: CRS.Simple,
      bounds: [
        [-26.5, -25],
        [1021.5, 1023],
      ],
      // url: '../assets/stadium.webp',
      // url: 'https://previews.123rf.com/images/nitinut380/nitinut3801803/nitinut380180301147/98479734-top-view-show-of-seats-map-at-the-football-stadium.jpg',
      url: "https://pngset.com/images/raiders-stadium-seating-chart-las-vegas-building-field-arena-football-field-transparent-png-517384.png",
      zoom: 1,
      center: [300, 500],
      options1: {
        name: "Qko",
        noWrap: true,
      },
    };
  },

  components: {
    LMap,
    LTileLayer,
    LImageOverlay,
    LMarker,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
