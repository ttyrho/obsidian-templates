---
tags:
  - catalog/journal
aliases:
---

# <%tp.file.title%>

## Articles
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    authors AS Authors,
    date AS Date,
    volume AS Volume,
    issue AS Issue,
    language AS Language,
    keywords AS Keywords,
    classifiers AS Classifiers,
    collections AS Collections
FROM
    #reference/research/article
WHERE
    contains(conference, [[<%tp.file.title%>]])
SORT
    date DESCENDING,
    volume DESCENDING,
    issue DESCENDING
```
