---
tags:
  - area
link: Deserter Camp
---
# Map
```leaflet
id: hagga-basin
image: [[HaggaBasinFull.jpg]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [4006, 4006] # Modificar
defaultZoom: -3.5
zoomDelta: 0.5
minZoom: -3.5
maxZoom: 1
width: 95%
height: 700px
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
from #location and #star-chest and "Locations/Hagga Basin"
sort region
```
# All Locations
```dataview
table region
from #location and "Locations/Hagga Basin"
sort region
```
