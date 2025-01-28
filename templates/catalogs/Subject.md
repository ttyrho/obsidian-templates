---
tags:
  - catalog/collection/subject
type: Subject
passed: false
institution:
program:
aliases:
course:
period:
kind:
credits:
keywords:
---

# <%tp.file.title%>

## References
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS "Title",
    authors as "Authors",
    date AS "Date",
    language AS "Language",
    keywords AS "Keywords"
FROM
    #reference
WHERE
    contains(collections, [[<%tp.file.title%>]])
SORT
    date DESCENDING
```

## Knowledge
```dataview
TABLE WITHOUT ID
    file.link AS "Title",
    keywords AS "Keywords"
FROM
    #knowledge
WHERE
    contains(collections, [[<%tp.file.title%>]])
```

## Exercises
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS "Title",
    reference AS "Reference",
    page AS "Page",
    solved AS "Solved?"
FROM
    #literature/exercise
WHERE
    contains(collections, [[<%tp.file.title%>]])
SORT
    page ASCENDING,
    order ASCENDING
```
