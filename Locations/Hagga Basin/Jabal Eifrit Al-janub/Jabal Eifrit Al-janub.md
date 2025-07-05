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
coordinates: [5014, 6027] # Modificar
defaultZoom: -1.5
zoomDelta: 0.5
minZoom: -3.5
maxZoom: 1
width: 95%
height: 600px
scale: 2.81
unit: meters
markerFolder: Locations
markerFolder: Representatives
```
# Uniques
```meta-bind-embed
[[uniques-region]]
```
# Resources
- [[Granite Stone]]
- [[Salvaged Metal]]
- [[Fuel Cell]]
- [[Copper Ore]]
- [[Flour Sand]]
- [[Carbon Ore]]
- [[Erythrite Crystal]]
- [[Aluminum Ore]]
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
