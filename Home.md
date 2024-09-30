
# Assignments
```dataview
table due_date as "Due Date", assignment as "Assignment"
from "Assignments"
sort due_date asc
```
# Class Notes

```dataview 
table file.folder as "Subject"
from "/"
where file.name != "Home"
where file.folder != "Templates"
sort file.folder
```
