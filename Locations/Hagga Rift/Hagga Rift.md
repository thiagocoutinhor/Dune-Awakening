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
  - [2000, 1875]
coordinates: [1552.7813, 1605.521] # Modificar
defaultZoom: 0
minZoom: -2
maxZoom: 1
width: 95%
height: 600px
scale: 2.81
unit: meters
markerFolder: Locations
```

# Uniques
```dataviewjs
const current = dv.current()

dv.table([
	'Unique'
], dv.pages('#unique')
	.filter(page => page.file.inlinks.map(inlink => dv.page(inlink).region).includes(current.file.link))
	.map(page => [page.file.link])
)
```
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
