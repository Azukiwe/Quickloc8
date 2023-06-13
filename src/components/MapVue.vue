<template>
    <div class="map"></div>
</template>

<script>
// import L from 'leaflet';
export default {
    mounted() {
//         let map = L.map('map').fitWorld();

// L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
//     maxZoom: 19,
//     attribution: '© OpenStreetMap'
// }).addTo(map);

// function onLocationFound(e) {
//     var radius = e.accuracy;

//     L.marker(e.latlng).addTo(map)
//         .bindPopup("You are within " + radius + " meters from this point").openPopup();

//     L.circle(e.latlng, radius).addTo(map);
// }

// map.on('locationfound', onLocationFound);
// function onLocationError(e) {
//     alert(e.message);
// }

// map.on('locationerror', onLocationError); 
    }
}
</script>
<style scoped>
#map{
    height: 100vh;
    width: 100%;
}
</style>