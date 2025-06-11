# Copper
```dataview
table cost, replace(join(tags), ", unique", "") as tags, join(file.inlinks) as locations
from #unique 
where tier = "Copper"
```
# Iron
```dataview
table cost, replace(join(tags), ", unique", "") as tags, join(file.inlinks) as locations
from #unique 
where tier = "Iron"
```
# Duraluminium
```dataview
table cost, replace(join(tags), ", unique", "") as tags, join(file.inlinks) as locations
from #unique 
where tier = "Duraluminium"
```
