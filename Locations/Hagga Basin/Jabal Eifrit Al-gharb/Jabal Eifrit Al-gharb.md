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
coordinates: [6099, 4670] # Modificar
defaultZoom: -2
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
```dataviewjs
const current = dv.current()

dv.table([
	'Unique', 'Location'
], dv.pages('#unique')
	.filter(page => page.file.inlinks.map(inlink => dv.page(inlink).region).includes(current.file.link))
	.map(page => {
		page.locais = page.file.inlinks
			.filter(inlink => dv.page(inlink).tags.includes('location'))
			.filter(inlink => dv.page(inlink).region == String(current.file.link))
		return page
	})
	.map(page => [
		page.file.link,
		page.locais.join(', ')
	])
)
```
# Resources
- [[Granite Stone]]
- [[Salvaged Metal]]
- [[Fuel Cell]]
- [[Carbon Ore]]
- [[Copper Ore]]
- [[Aluminum Ore]]
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
