---
tags:
  - region
---
# Map
```leaflet
id: hagga-basin
image: [[Hagga Basin.png]]
bounds:
  - [0, -625]
  - [3000, 1875]
coordinates: [1040, 1219.5482] # Modificar
defaultZoom: 0
zoomDelta: 0.5
zoomDelta: 0.5
minZoom: -2
maxZoom: 1
width: 95%
height: 700px
scale: 2.81
unit: meters
markerFolder: Locations
```
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
