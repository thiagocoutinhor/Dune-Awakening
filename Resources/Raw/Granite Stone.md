---
tags:
  - resource
  - raw
tier: Salvage
---
# Found In
```dataview
table
from #location 
where contains(file.outlinks, this.file.link)
```
# Used In
```dataview
table
from #resource
where contains(file.outlinks, this.file.link)
```