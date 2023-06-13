<template>
  <div id="map"></div>
</template>

<script>
import L from 'leaflet';
export default {
    mounted() {
        let map = L.map('map').setView([-33.918861, 18.423300], 10);

L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '© OpenStreetMap'
}).addTo(map);
map.locate({setView: true, maxZoom: 16});
//street map
googleStreets = L.tileLayer('http://{s}.google.com/vt/lyrs=m&x={x}&y={y}&z={z}',{
    maxZoom: 16,
    subdomains:['mt0','mt1','mt2','mt3']
});
googleStreets.addTo(map)
// function onLocationFound(e) {
//     var radius = e.accuracy;

//     L.marker(e.latlng).addTo(map)
//         .bindPopup("You are within " + radius + " meters from this point").openPopup();

//     L.circle(e.latlng, radius).addTo(map);
// }
let Marker = L.marker([-34.040278, 18.677778]);
let Up = Marker.bindPopup('Your current location').openPopup()
Up.addTo(map)

map.on('locationfound', onLocationFound);
function onLocationError(e) {
    alert(e.message);
}

map.on('locationerror', onLocationError); 
    }
}
</script>
<style scoped>
#map{
    height: 100vh;
    width: 100%;
    position: absolute;
    justify-content: center;
}
</style>

