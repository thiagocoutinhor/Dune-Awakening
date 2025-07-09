# Copper
```dataview
table 
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique
where tier = "Copper"
sort tags, type
```
# Iron
```dataview
table
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique 
where tier = "Iron"
sort tags, type
```
# Steel
```dataview
table
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique 
where tier = "Steel"
sort tags, type
```
# Aluminum
```dataview
table
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique 
where tier = "Aluminum"
sort tags, type
```
# Duraluminum
```dataview
table
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique 
where tier = "Duraluminum"
sort tags, type
```
# Plastanium
```dataview
table
	cost, 
	replace(join(tags), ", unique", "") as tags, 
	type,
	join(file.inlinks) as locations
from #unique 
where tier = "Plastanium"
sort tags, type
```
