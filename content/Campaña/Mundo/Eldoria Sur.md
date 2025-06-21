---
title: Mapa Interactivo
---

<div id="map" style="height: 800px; border: 2px solid #ccc;"></div>

<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
/>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
  document.addEventListener("DOMContentLoaded", () => {
    const bounds = [[0, 0], [3224, 4961]];
    const map = L.map("map", {
      crs: L.CRS.Simple,
      minZoom: -3,
    });
    const image = L.imageOverlay("/assets/mapa.jpg", bounds).addTo(map);
    map.fitBounds(bounds);
  
    map.on("click", function (e) {
      console.log("Coordenadas:", e.latlng);
    });

</script>
