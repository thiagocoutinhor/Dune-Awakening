---
tags:
  - region
---
# Map
```leaflet
id: hagga-basin
image: [[HaggaBasinFull.jpg]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [5011, 6135] # Modificar
defaultZoom: -2
zoomDelta: 0.5
minZoom: -3.5
maxZoom: 1
width: 95%
height: 900px
scale: 2.81
unit: meters
markerFolder: Locations
markerFolder: Representatives
```
# Uniques
```meta-bind-embed
[[uniques-region]]
```
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
