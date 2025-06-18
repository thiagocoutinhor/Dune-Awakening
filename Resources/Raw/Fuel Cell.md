---
tags:
  - resource
  - fuel
tier: Copper
---
# Found In
```dataview
table
from #region 
where contains(file.outlinks, this.file.link)
```
# Used In
```dataview
table
from #resource
where contains(file.outlinks, this.file.link)
```