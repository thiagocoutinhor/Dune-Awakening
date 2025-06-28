---
tags:
  - region
---
# Map
```leaflet
id: hagga-basin
image: [[HaggaBasinFull.webp]]
bounds:
  - [0, 0]
  - [8012, 8012]
coordinates: [3079, 6161] # Modificar
defaultZoom: -1.5
zoomDelta: 0.5
minZoom: -3.5
maxZoom: 1
width: 95%
height: 700px
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
- [[Iron Ore]]
- [[Flour Sand]]
# Locations
```dataview
table replace(join(tags), "location, ", "") as Tipo
where region = this.file.link
```
