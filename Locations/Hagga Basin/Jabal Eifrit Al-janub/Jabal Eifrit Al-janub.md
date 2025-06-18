---
tags:
  - region
---

# Map
```leaflet
id: hagga-basin
image: [[Hagga Basin.png]]
bounds:
  - [0,-625]
  - [3000, 1875]
coordinates: [1772.5938, 1007.0542] # Modificar
defaultZoom: 0
zoomDelta: 0.5
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
