---
tags:
  - area
---
# Map
```leaflet
id: hagga-basin
image: [[Hagga Basin.png]]
bounds:
  - [0,-625]
  - [3000, 1875]
coordinates: [1500, 625] # Modificar
defaultZoom: -2
minZoom: -2
maxZoom: 1
width: 95%
height: 900px
scale: 2.81
unit: meters
markerFolder: Locations
markerFolder: Representatives
```
# Regions
```dataview
table
from #region and -"zzz_templates"
```
# Star Chests
```dataview
table region
from #location and #star-chest 
sort region
```
# All Locations
```dataview
table region
from #location and "Locations/Hagga Basin"
sort region
```
