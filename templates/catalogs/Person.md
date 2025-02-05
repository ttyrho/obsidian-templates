---
tags:
  - catalog/person
aliases:
birth:
dead:
---

# <%tp.file.title%>

## Biographies
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    date AS Date,
    language AS Language,
    keywords AS Keywords,
    collections as Collections
FROM
    #reference/book/biography
WHERE
    contains(subjects, [[<%tp.file.title%>]])
SORT
    date DESCENDING
```

## References
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    date AS Date,
    language AS Language,
    keywords AS Keywords,
    collections as Collections
FROM
    #reference
WHERE
    contains(authors, [[<%tp.file.title%>]])
SORT
    date DESCENDING
```
