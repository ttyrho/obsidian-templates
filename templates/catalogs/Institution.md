---
tags:
  - catalog/institution
aliases:
---

# <% tp.file.title %>

## Subjects
```dataview
TABLE WITHOUT ID
	link(file.path, aliases[0]) AS "Title",
	program AS "Program",
	course AS "Course",
	period AS "Period",
	passed AS "Passed",
	keywords AS "Keywords"
FROM
	#catalog/collection/subject
WHERE
	contains(institution, [[<%tp.file.title%>]])
SORT
	program ASCENDING,
	course ASCENDING,
	period ASCENDING
```
