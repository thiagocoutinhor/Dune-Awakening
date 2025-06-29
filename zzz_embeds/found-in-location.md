```dataview
table
from #location
where contains(file.outlinks, this.file.link)
```