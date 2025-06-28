---
tags:
  - area
link: Deserter Camp
---
# Map
```meta-bind-js-view
{link} as link
---
const link = context.bound.link;
const location0 = `\`INPUT[number:${link}#location[0]]\``;
const location1 = `\`INPUT[number:${link}#location[1]]\``;
const location = location0 + " " + location1 + " " + `\`VIEW[{${link}#tags}]\``
return engine.markdown.create(location);
```
`INPUT[suggester(optionQuery("Locations"), useLinks(false)):link]` `VIEW[{link}][link]`

1,945.3391, 1,439.222

```leaflet
id: hagga-basin
image: [[HaggaBasinFull.webp]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [4006, 4006] # Modificar
defaultZoom: -3
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
from #location and #star-chest
sort region
```
# All Locations
```dataview
table region
from #location and "Locations/Hagga Basin"
sort region
```
