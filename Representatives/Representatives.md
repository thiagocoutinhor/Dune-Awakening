# Map
```leaflet
id: representatives
image: [[HaggaBasinFull.jpg]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [4006, 4006] # Modificar
defaultZoom: -3
zoomDelta: 0.5
minZoom: -3.5
maxZoom: 1
width: 95%
height: 900px
scale: 2.81
unit: meters
markerFolder: Representatives
```

# Helped
```dataview
table
from #representative 
where helped
sort file.name
```
# Need Swatch
```dataview
table
from #representative 
where !swatch
sort file.name
```
# Locations
```dataview
table region, helped
from #representative
sort file.name
```