---
tags:
  - catalog/classifier
aliases:
---

# <%tp.file.title%>

## References
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    authors AS Authors,
    date AS Date,
    language AS Language,
    keywords AS Keywords,
    collections AS Collections
FROM
    #reference
WHERE
    contains(classifiers, [[<%tp.file.title%>]])
SORT
    date DESCENDING
```
