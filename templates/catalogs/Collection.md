---
tags:
  - catalog/collection
type: Collection
aliases: 
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
