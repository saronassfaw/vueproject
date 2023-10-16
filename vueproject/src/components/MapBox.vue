<template>
  <div ref="mapContainer" class="map-container">
    
  </div>
</template>

<script>
import mapboxgl from 'mapbox-gl'

export default {
  data() {
    return {
      map: null,
      feature: null,
      popup: null
    };
  },
  mounted() {
    mapboxgl.accessToken = import.meta.env.VITE_MAPBOX_MY_API_KEY;
    const map = new mapboxgl.Map({
      container: this.$refs.mapContainer,
      style: 'mapbox://styles/saronassfaww/clnkjx1u1002001pg1wb70rpe',
      center: [138.2529, 36.2048],
      zoom: 5
    });

    this.map = map;

    this.map.on('click', (event) => {
      const features = this.map.queryRenderedFeatures(event.point, {
        layers: ['japan']
      });
      if (!features.length) {
        return;
      }
      const feature = features[0];
      this.feature = feature;

      const popup = new mapboxgl.Popup({ offset: [0, -15] })
        .setLngLat(this.feature.geometry.coordinates)
        .setHTML(
          `<h3>${this.feature.properties.title}</h3><p>${this.feature.properties.description}</p>`
        )
        .addTo(this.map);

      this.popup = popup;
    });
  }
}
</script>

<style scoped>
.map-container {
  flex: 1;
  margin-top: 100px;
  margin-right: 10px;
  width: 30%;
  border-radius: 110px;
}
.map-container:hover {
  cursor: grab;
}

</style>
