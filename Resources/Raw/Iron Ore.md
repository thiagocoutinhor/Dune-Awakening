---
tags:
  - resource
  - raw
tier: Iron
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