```meta-bind-js-view
{location} as location
---
const x = context.bound.location[0]
const y = context.bound.location[1]
const map = `\`\`\`leaflet
id: hagga-basin
image: [[HaggaBasinFull.jpg]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [${x}, ${y}]
defaultZoom: 0
zoomDelta: 0.5
minZoom: -2
maxZoom: 1
width: 250px
height: 250px
scale: 2.81
unit: meters
markerFolder: Locations
noUI: true
\`\`\``
return engine.markdown.create(map)
```
