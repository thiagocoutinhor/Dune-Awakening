---
tags:
  - resource
  - raw
tier: Plastanium
---
# Found In
```dataview
table
from #region AND -"zzz_templates"
where contains(file.outlinks, this.file.link) 
```
# Used In
```dataview
table
from #resource
where contains(file.outlinks, this.file.link)
```